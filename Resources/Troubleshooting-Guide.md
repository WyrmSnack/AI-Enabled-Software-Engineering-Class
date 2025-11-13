# Troubleshooting Guide

## Common Issues and Solutions

### Python & Environment Issues

#### "Python not found" or "command not recognized"
**Solution**:
- Windows: Add Python to PATH during installation, or use full path
- Mac/Linux: Use `python3` instead of `python`
- Verify: `python --version` or `python3 --version`

#### "Module not found" errors
**Solution**:
- Ensure virtual environment is activated
- Install package: `pip install [package-name]`
- Upgrade pip: `python -m pip install --upgrade pip`
- Check you're in the correct directory

#### Virtual environment not activating
**Solution**:
- Windows: `venv\Scripts\activate`
- Mac/Linux: `source venv/bin/activate`
- If still fails, recreate: `python -m venv venv`

---

### FastAPI Issues

#### "Cannot import FastAPI"
**Solution**:
- Install: `pip install fastapi uvicorn`
- Verify: `python -c "import fastapi; print('OK')"`
- Check virtual environment is activated

#### Server won't start
**Solution**:
- Check port isn't in use: `lsof -i :8000` (Mac/Linux) or `netstat -ano | findstr :8000` (Windows)
- Try different port: `uvicorn main:app --port 8001`
- Check for syntax errors in main.py

#### CORS errors in browser
**Solution**:
- Add CORS middleware in main.py:
```python
from fastapi.middleware.cors import CORSMiddleware
app.add_middleware(CORSMiddleware, allow_origins=["*"])
```

---

### Database Issues

#### SQLite database locked
**Solution**:
- Close all connections
- Check for other processes using the database
- Restart your application

#### PostgreSQL connection failed
**Solution**:
- Verify PostgreSQL is running: `pg_isready`
- Check connection string in .env
- Verify database exists: `psql -l`
- Check firewall/network settings

#### Migration errors
**Solution**:
- Check Alembic is installed: `pip install alembic`
- Verify database URL in alembic.ini
- Try: `alembic upgrade head --sql` to see SQL
- Check for syntax errors in migration files

---

### Git & GitHub Issues

#### "Permission denied" when pushing
**Solution**:
- Set up SSH keys, or
- Use HTTPS with personal access token
- Check repository permissions

#### "Repository not found"
**Solution**:
- Verify you're logged into correct GitHub account
- Check repository URL is correct
- Verify you have access to the repository

#### Merge conflicts
**Solution**:
- Pull latest: `git pull origin main`
- Resolve conflicts in files
- Stage resolved files: `git add .`
- Complete merge: `git commit`

---

### AI Tool Issues

#### Copilot not suggesting code
**Solution**:
- Verify Copilot is enabled in IDE settings
- Check you're signed in to GitHub
- Restart IDE
- Check internet connection

#### AI-generated code has errors
**Solution**:
- This is normal! Always review AI code
- Ask AI to fix: "This code has an error: [error]. Fix it."
- Test the code
- Iterate with more specific prompts

#### Prompts not giving good results
**Solution**:
- Be more specific
- Provide more context
- Use examples
- Break complex tasks into steps
- Try different prompt patterns

---

### Testing Issues

#### Tests not running
**Solution**:
- Verify pytest installed: `pip install pytest`
- Run: `pytest` (not `python pytest`)
- Check test file names start with `test_`
- Verify test functions start with `test_`

#### Coverage not working
**Solution**:
- Install: `pip install pytest-cov`
- Run: `pytest --cov=. --cov-report=html`
- Check coverage.py is installed

#### Tests failing
**Solution**:
- Read error messages carefully
- Check test data/fixtures
- Verify database is set up correctly
- Run tests individually: `pytest tests/test_file.py::test_function`

---

### Frontend Issues

#### React app won't start
**Solution**:
- Install dependencies: `npm install`
- Check Node.js version: `node --version` (should be 16+)
- Clear cache: `rm -rf node_modules package-lock.json && npm install`
- Check for port conflicts

#### API calls failing
**Solution**:
- Verify backend is running
- Check CORS configuration
- Verify API URL is correct
- Check browser console for errors
- Verify network tab in dev tools

#### Build errors
**Solution**:
- Check for syntax errors
- Verify all imports are correct
- Check TypeScript errors (if using TS)
- Clear build cache: `rm -rf dist build`

---

### CI/CD Issues

#### GitHub Actions failing
**Solution**:
- Check workflow YAML syntax
- Verify all required secrets are set
- Check Python version matches
- Review action logs for specific errors
- Test workflow locally first

#### Tests failing in CI but passing locally
**Solution**:
- Check environment differences
- Verify test data is available in CI
- Check database setup in CI
- Review CI logs for specific errors

---

### General Debugging Tips

1. **Read error messages carefully** - They usually tell you what's wrong
2. **Check the logs** - Application logs, CI logs, browser console
3. **Test incrementally** - Don't change everything at once
4. **Use print statements** - Simple debugging tool
5. **Ask AI for help** - "This error means: [error]. How do I fix it?"
6. **Search for solutions** - Error messages often have solutions online
7. **Take breaks** - Fresh eyes see things differently

---

### Getting More Help

1. **Check worksheet troubleshooting sections** - Each worksheet has specific troubleshooting
2. **Review Resources/ folder** - Quick references and guides
3. **Ask in course forums** - Other students may have same issue
4. **Contact instructor** - For persistent issues
5. **Use AI tools** - Describe your problem and ask for solutions

---

### Prevention Tips

- **Use virtual environments** - Isolate dependencies
- **Commit frequently** - Easy to roll back
- **Test as you go** - Catch issues early
- **Read documentation** - Understand tools before using
- **Keep dependencies updated** - But test after updates
- **Use version control** - Track all changes

---

**Remember**: Most issues have solutions. Take a deep breath, read the error message, and work through it systematically! 💪

