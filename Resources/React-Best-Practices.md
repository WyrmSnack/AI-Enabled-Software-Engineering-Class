# React Best Practices

Essential practices for building React applications.

## Component Structure

### Functional Components
```jsx
function UserCard({ user }) {
  return (
    <div className="user-card">
      <h3>{user.name}</h3>
      <p>{user.email}</p>
    </div>
  );
}
```

### Component Organization
```
components/
  UserCard/
    UserCard.jsx
    UserCard.css
    index.js
```

---

## State Management

### useState Hook
```jsx
function Counter() {
  const [count, setCount] = useState(0);
  
  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```

### useEffect Hook
```jsx
function UserProfile({ userId }) {
  const [user, setUser] = useState(null);
  
  useEffect(() => {
    fetchUser(userId).then(setUser);
  }, [userId]);  // Dependency array
  
  return user ? <div>{user.name}</div> : <div>Loading...</div>;
}
```

---

## Props and PropTypes

### Props
```jsx
function Button({ label, onClick, disabled = false }) {
  return (
    <button onClick={onClick} disabled={disabled}>
      {label}
    </button>
  );
}
```

### Default Props
```jsx
Button.defaultProps = {
  disabled: false,
  variant: 'primary'
};
```

---

## Performance Optimization

### useMemo
```jsx
const expensiveValue = useMemo(() => {
  return computeExpensiveValue(a, b);
}, [a, b]);
```

### useCallback
```jsx
const handleClick = useCallback(() => {
  doSomething(id);
}, [id]);
```

### React.memo
```jsx
const UserCard = React.memo(function UserCard({ user }) {
  return <div>{user.name}</div>;
});
```

---

## Error Handling

### Error Boundaries
```jsx
class ErrorBoundary extends React.Component {
  state = { hasError: false };
  
  static getDerivedStateFromError(error) {
    return { hasError: true };
  }
  
  render() {
    if (this.state.hasError) {
      return <h2>Something went wrong.</h2>;
    }
    return this.props.children;
  }
}
```

### Try-Catch in Effects
```jsx
useEffect(() => {
  async function fetchData() {
    try {
      const data = await fetchUser();
      setUser(data);
    } catch (error) {
      setError(error.message);
    }
  }
  fetchData();
}, []);
```

---

## Best Practices

### Do's
✅ Use functional components
✅ Keep components small
✅ Use meaningful names
✅ Extract reusable logic
✅ Handle errors
✅ Optimize performance
✅ Use TypeScript (if possible)

### Don'ts
❌ Mutate state directly
❌ Create components in render
❌ Use index as key
❌ Ignore warnings
❌ Skip error handling
❌ Over-optimize prematurely

---

## Using AI for React Development

### Generate Components
**Prompt**:
```
Create a React component for [description].

Include:
- Props interface
- State management
- Event handlers
- Error handling
- Loading states
```

### Review Components
**Prompt**:
```
Review this React component for:
- Best practices
- Performance issues
- Error handling
- Code quality

[Component code]
```

---

## Resources

- [React Documentation](https://react.dev/)
- [React Hooks](https://react.dev/reference/react)
- [React Patterns](https://reactpatterns.com/)

