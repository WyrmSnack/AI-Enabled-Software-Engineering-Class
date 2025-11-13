# React Cheat Sheet

Quick reference for React.

## Component
```jsx
function Component() {
  return <div>Hello</div>;
}
```

## Props
```jsx
function Greeting({ name }) {
  return <h1>Hello, {name}!</h1>;
}
```

## State
```jsx
import { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);
  return (
    <div>
      <p>{count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```

## useEffect
```jsx
import { useEffect } from 'react';

function Component() {
  useEffect(() => {
    // Side effect
    return () => {
      // Cleanup
    };
  }, [dependencies]);
}
```

## Conditional Rendering
```jsx
{isLoggedIn ? <Dashboard /> : <Login />}
{items.length > 0 && <ItemList items={items} />}
```

## Lists
```jsx
{items.map(item => (
  <div key={item.id}>{item.name}</div>
))}
```

## Event Handlers
```jsx
function handleClick() {
  console.log('Clicked');
}

<button onClick={handleClick}>Click</button>
```

## Fetching Data
```jsx
useEffect(() => {
  fetch('/api/data')
    .then(res => res.json())
    .then(data => setData(data));
}, []);
```

