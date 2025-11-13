# Code Review Best Practices

Comprehensive guide to reviewing code, especially AI-generated code.

## Principles of Good Code Review

### Focus on Code, Not People
- Critique the code, not the author
- Be constructive, not critical
- Assume good intentions
- Provide actionable feedback

### Review for Multiple Concerns
- **Correctness**: Does it work?
- **Security**: Any vulnerabilities?
- **Performance**: Any bottlenecks?
- **Maintainability**: Is it readable?
- **Testing**: Are tests adequate?

---

## Reviewing AI-Generated Code

### Special Considerations

#### 1. Verify Logic Correctness
AI can generate code that looks right but has logical errors.

**Check**:
- [ ] Does the logic match requirements?
- [ ] Are edge cases handled?
- [ ] Are error conditions considered?
- [ ] Does it actually solve the problem?

**Example**:
```python
# AI might generate:
def calculate_discount(price, discount_percent):
    return price * discount_percent  # Wrong: should be price * (discount_percent / 100)

# Review should catch: Missing division by 100
```

#### 2. Check for Security Issues
AI may not consider security implications.

**Check**:
- [ ] Input validation present?
- [ ] SQL injection prevented?
- [ ] XSS prevention?
- [ ] Authentication/authorization correct?
- [ ] Secrets not exposed?

**Example**:
```python
# AI might generate:
query = f"SELECT * FROM users WHERE email = '{email}'"  # SQL injection risk

# Review should catch: Use parameterized queries
```

#### 3. Verify Dependencies
AI may suggest unnecessary or outdated packages.

**Check**:
- [ ] Are dependencies necessary?
- [ ] Are versions appropriate?
- [ ] Any security vulnerabilities?
- [ ] License compatibility?

#### 4. Review Error Handling
AI often generates code without proper error handling.

**Check**:
- [ ] Try-except blocks where needed?
- [ ] Appropriate error messages?
- [ ] Error logging?
- [ ] Graceful degradation?

#### 5. Check Code Style and Patterns
AI may not follow your team's conventions.

**Check**:
- [ ] Follows style guide?
- [ ] Matches existing patterns?
- [ ] Consistent naming?
- [ ] Appropriate comments?

---

## What to Look For in PRs

### Functionality
- [ ] Code works as intended
- [ ] Requirements met
- [ ] Edge cases handled
- [ ] Error cases handled
- [ ] Performance acceptable

### Code Quality
- [ ] Readable and maintainable
- [ ] Well-structured
- [ ] No code duplication
- [ ] Appropriate abstractions
- [ ] Good naming

### Testing
- [ ] Tests present
- [ ] Tests cover happy paths
- [ ] Tests cover edge cases
- [ ] Tests cover error cases
- [ ] Test quality is good

### Documentation
- [ ] Code documented
- [ ] README updated (if needed)
- [ ] API documented (if applicable)
- [ ] Comments explain "why" not "what"

### Security
- [ ] No hardcoded secrets
- [ ] Input validation
- [ ] SQL injection prevented
- [ ] XSS prevention
- [ ] Authentication/authorization correct

### AI Usage
- [ ] AI usage documented
- [ ] Prompts included (if applicable)
- [ ] Code reviewed (not just accepted)
- [ ] Attribution clear

---

## Constructive Feedback Patterns

### Good Feedback Examples

#### ✅ Specific and Actionable
```
The error handling in this function is good, but consider adding a check for 
empty input. Currently, an empty list would cause an IndexError.

Suggestion:
if not items:
    raise ValueError("Items list cannot be empty")
```

#### ✅ Explains Why
```
Consider using a dictionary lookup here instead of a list comprehension. 
For large datasets, O(1) lookup will be much faster than O(n) iteration.

Current: [item for item in items if item.id == target_id][0]
Suggested: items_dict[target_id]
```

#### ✅ Offers Alternatives
```
This approach works, but you might consider using FastAPI's dependency 
injection for database sessions. It would make testing easier and follow 
FastAPI best practices.
```

#### ✅ Acknowledges Good Work
```
Great job on the error handling! The try-except blocks are well-placed and 
the error messages are clear. One small suggestion: consider logging the 
errors for debugging purposes.
```

### Poor Feedback Examples

#### ❌ Vague
```
This doesn't look right.
```

#### ❌ Too Critical
```
This is terrible. Rewrite it.
```

#### ❌ Doesn't Explain
```
Use a dictionary instead.
```

#### ❌ Personal Attack
```
You clearly don't understand how this works.
```

---

## Code Review Checklist

### Before Reviewing
- [ ] Understand the context
- [ ] Read the PR description
- [ ] Understand the requirements
- [ ] Check related issues/PRs

### During Review
- [ ] Read code carefully
- [ ] Test understanding mentally
- [ ] Check for common issues
- [ ] Verify tests
- [ ] Check documentation

### After Review
- [ ] Provide clear feedback
- [ ] Prioritize feedback (must-fix vs. nice-to-have)
- [ ] Be available for questions
- [ ] Approve when ready

---

## Common Issues to Watch For

### Logic Errors
- Off-by-one errors
- Incorrect conditions
- Missing edge cases
- Wrong assumptions

### Security Issues
- SQL injection
- XSS vulnerabilities
- Missing authentication
- Exposed secrets
- Insecure defaults

### Performance Issues
- N+1 queries
- Missing indexes
- Inefficient algorithms
- Memory leaks
- Unnecessary computations

### Code Quality Issues
- Code duplication
- Poor naming
- Too complex
- Missing comments
- Inconsistent style

### Testing Issues
- Missing tests
- Inadequate coverage
- Flaky tests
- Poor test quality
- Missing edge cases

---

## Using AI to Assist Code Review

### Generate Review Comments
**Prompt**:
```
Review this code for:
- Security issues
- Performance problems
- Code quality
- Best practices
- Potential bugs

[Code snippet]
```

### Check for Common Issues
**Prompt**:
```
Check this code for common issues:
- SQL injection
- XSS vulnerabilities
- Missing error handling
- Performance problems
- Code smells

[Code snippet]
```

### Suggest Improvements
**Prompt**:
```
Suggest improvements for this code:

[Code snippet]

Focus on:
- Readability
- Performance
- Maintainability
- Best practices
```

---

## Best Practices

### For Reviewers
- ✅ Review promptly
- ✅ Be constructive
- ✅ Explain reasoning
- ✅ Be respectful
- ✅ Focus on code
- ✅ Approve when ready

### For Authors
- ✅ Keep PRs small
- ✅ Write clear descriptions
- ✅ Respond to feedback
- ✅ Don't take it personally
- ✅ Ask questions if unclear
- ✅ Thank reviewers

---

## Resources

- [Google Code Review Guide](https://google.github.io/eng-practices/review/)
- [Atlassian Code Review Best Practices](https://www.atlassian.com/agile/software-development/code-reviews)
- [GitHub Code Review Guide](https://github.com/features/code-review)

