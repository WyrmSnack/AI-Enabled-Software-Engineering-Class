# FastAPI Cheat Sheet

Quick reference for FastAPI.

## Basic App
```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def root():
    return {"message": "Hello World"}
```

## Path Parameters
```python
@app.get("/items/{item_id}")
async def get_item(item_id: int):
    return {"item_id": item_id}
```

## Query Parameters
```python
@app.get("/items")
async def list_items(skip: int = 0, limit: int = 100):
    return {"skip": skip, "limit": limit}
```

## Request Body
```python
from pydantic import BaseModel

class Item(BaseModel):
    name: str
    price: float

@app.post("/items")
async def create_item(item: Item):
    return item
```

## Response Models
```python
@app.get("/items", response_model=list[Item])
async def list_items():
    return items
```

## Status Codes
```python
from fastapi import status

@app.post("/items", status_code=status.HTTP_201_CREATED)
async def create_item(item: Item):
    return item
```

## Dependencies
```python
from fastapi import Depends

def get_db():
    db = SessionLocal()
    try:
        yield db
    finally:
        db.close()

@app.get("/items")
async def list_items(db: Session = Depends(get_db)):
    return db.query(Item).all()
```

## Error Handling
```python
from fastapi import HTTPException

@app.get("/items/{item_id}")
async def get_item(item_id: int):
    if item_id < 1:
        raise HTTPException(status_code=404, detail="Item not found")
    return {"item_id": item_id}
```

