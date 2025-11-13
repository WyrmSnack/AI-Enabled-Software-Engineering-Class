# Database Design Patterns

Essential patterns for designing relational databases.

## Normalization

### First Normal Form (1NF)
- Each column contains atomic values
- No repeating groups
- Each row is unique

### Second Normal Form (2NF)
- Meets 1NF
- All non-key columns depend on entire primary key

### Third Normal Form (3NF)
- Meets 2NF
- No transitive dependencies

### When to Denormalize
- Performance critical queries
- Read-heavy workloads
- Reporting/analytics
- Trade-off: Data consistency

---

## Relationship Patterns

### One-to-One
```python
class User(Base):
    id = Column(Integer, primary_key=True)
    profile = relationship("Profile", back_populates="user", uselist=False)

class Profile(Base):
    id = Column(Integer, primary_key=True)
    user_id = Column(Integer, ForeignKey("users.id"), unique=True)
    user = relationship("User", back_populates="profile")
```

### One-to-Many
```python
class User(Base):
    id = Column(Integer, primary_key=True)
    tasks = relationship("Task", back_populates="owner")

class Task(Base):
    id = Column(Integer, primary_key=True)
    user_id = Column(Integer, ForeignKey("users.id"))
    owner = relationship("User", back_populates="tasks")
```

### Many-to-Many
```python
# Association table
user_roles = Table(
    'user_roles',
    Base.metadata,
    Column('user_id', Integer, ForeignKey('users.id')),
    Column('role_id', Integer, ForeignKey('roles.id'))
)

class User(Base):
    id = Column(Integer, primary_key=True)
    roles = relationship("Role", secondary=user_roles, back_populates="users")

class Role(Base):
    id = Column(Integer, primary_key=True)
    users = relationship("User", secondary=user_roles, back_populates="roles")
```

---

## Indexing Strategies

### Primary Key Index
- Automatically created
- Unique and not null

### Foreign Key Index
- Improves join performance
- Usually automatically indexed

### Composite Index
```python
Index('idx_user_status', User.status, User.created_at)
```

### When to Index
- Frequently queried columns
- Foreign keys
- Columns in WHERE clauses
- Columns in JOIN conditions
- Columns in ORDER BY

### When Not to Index
- Rarely queried columns
- Frequently updated columns
- Small tables
- Columns with low cardinality

---

## Common Patterns

### Soft Delete
```python
class User(Base):
    id = Column(Integer, primary_key=True)
    deleted_at = Column(DateTime, nullable=True)
    
    @property
    def is_deleted(self):
        return self.deleted_at is not None
```

### Timestamps
```python
class BaseModel(Base):
    __abstract__ = True
    created_at = Column(DateTime, default=datetime.utcnow)
    updated_at = Column(DateTime, default=datetime.utcnow, onupdate=datetime.utcnow)
```

### UUID Primary Keys
```python
import uuid

class User(Base):
    id = Column(String, primary_key=True, default=lambda: str(uuid.uuid4()))
```

---

## Using AI for Database Design

### Generate Schema
**Prompt**:
```
Design a database schema for [application description].

Include:
- All necessary tables
- Relationships between tables
- Primary and foreign keys
- Indexes for performance
- Constraints (unique, not null, etc.)
- Appropriate data types
```

### Generate Migrations
**Prompt**:
```
Create Alembic migration for this schema change:

[Schema description]

Include:
- Up migration
- Down migration
- Data migrations if needed
```

---

## Resources

- [Database Design Tutorial](https://www.lucidchart.com/pages/database-diagram/database-design)
- [SQLAlchemy Documentation](https://docs.sqlalchemy.org/)
- [Alembic Documentation](https://alembic.sqlalchemy.org/)

