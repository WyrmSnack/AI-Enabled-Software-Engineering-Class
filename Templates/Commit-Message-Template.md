# Commit Message Guidelines

## Format

```
<type>: <subject>

<body>

<footer>
```

## Types

- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks
- `perf`: Performance improvements
- `ci`: CI/CD changes

## Examples

### Simple Commit
```
feat: add user authentication endpoint
```

### Detailed Commit
```
feat: add user authentication endpoint

- Implement JWT token generation
- Add password hashing with bcrypt
- Create login and register endpoints
- Add authentication middleware

Closes #123
```

### Bug Fix
```
fix: resolve login error with special characters

The login endpoint was failing when passwords contained
special characters. Updated password validation to handle
all valid password characters.

Fixes #456
```

### Documentation
```
docs: update API documentation for user endpoints

Added examples and detailed descriptions for all user
management endpoints.
```

## Guidelines

1. **Use imperative mood**: "add" not "added" or "adds"
2. **Capitalize first letter**: "Add" not "add"
3. **No period at end**: "Add feature" not "Add feature."
4. **Keep subject under 50 characters**
5. **Separate subject and body with blank line**
6. **Wrap body at 72 characters**
7. **Reference issues in footer**

## Bad Examples

❌ `fixed stuff`
❌ `update`
❌ `changes`
❌ `WIP`
❌ `asdf`

## Good Examples

✅ `feat: add user registration endpoint`
✅ `fix: resolve database connection timeout`
✅ `docs: update setup instructions`
✅ `test: add tests for authentication`

## AI-Assisted Commits

When using AI to generate commit messages:

1. Review the generated message
2. Ensure it follows the format
3. Add context if needed
4. Verify it accurately describes changes

Example prompt:
```
Generate a commit message for these changes:
[Paste git diff]

Follow conventional commit format.
```

