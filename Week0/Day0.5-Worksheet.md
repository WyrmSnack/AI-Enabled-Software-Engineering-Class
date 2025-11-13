# Day 0.5 Worksheet: Web Foundations & APIs

**Estimated Time**: 1–2 hours  
**Focus**: Understanding how front-end and back-end communicate; APIs, JSON, and HTTP requests

---

## Learning Objectives

By the end of this session, you will be able to:
- Understand how front-end and back-end communicate
- Learn what APIs are and how requests work
- Practice using Python to fetch data from an API
- Understand JSON data format

---

## Pre-Activity: The Web Architecture

**Think about how websites work**:

When you visit a website like `github.com`:
1. Your **browser** (client) sends a request
2. The **server** processes the request
3. The **server** sends back HTML, CSS, JavaScript
4. Your **browser** displays the page

**Client-Server Model**:
```
[Your Browser]  ←→  [GitHub Server]
   (Client)            (Server)
```

**Questions**:
- What is the **client**? _______________________________________________________________________
- What is the **server**? _______________________________________________________________________

---

## Activity 1: Understanding APIs

**Resource**: [What is an API? by Postman](https://www.postman.com/api-what-is-an-api/)

**Read the article and answer**:

1. **What does API stand for?** _______________________________________________________________________

2. **In simple terms, what is an API?**
   _______________________________________________________________________
   _______________________________________________________________________

3. **Real-world analogy**: An API is like a _________________________
   (e.g., a restaurant menu, a waiter, a translator)

4. **Why do developers use APIs?**
   _______________________________________________________________________
   _______________________________________________________________________

---

## Activity 2: HTTP Basics

**HTTP Methods** (what you can do with an API):

| Method | What It Does | Example |
|--------|--------------|---------|
| GET | Retrieve data | Get a list of users |
| POST | Create data | Create a new user |
| PUT | Update data | Update user information |
| DELETE | Remove data | Delete a user |

**HTTP Status Codes**:

| Code | Meaning | Example |
|------|---------|---------|
| 200 | Success | Request worked |
| 404 | Not Found | Page/resource doesn't exist |
| 500 | Server Error | Something went wrong on server |

**Practice**: Match the scenario to the HTTP method:
- [ ] GET — Viewing a user profile
- [ ] POST — Creating a new account
- [ ] PUT — Updating your email address
- [ ] DELETE — Removing a comment

---

## Activity 3: Understanding JSON

**JSON** (JavaScript Object Notation) is how APIs send and receive data.

**Example JSON**:
```json
{
  "name": "Alice",
  "age": 30,
  "email": "alice@example.com",
  "skills": ["Python", "SQL", "JavaScript"]
}
```

**Key points**:
- Uses `{}` for objects (like a dictionary in Python)
- Uses `[]` for arrays/lists
- Keys and strings use double quotes `"`
- Numbers and booleans don't need quotes

**Practice**: Identify the data types:

```json
{
  "id": 1,                    // Type: _______
  "name": "Bob",              // Type: _______
  "is_active": true,          // Type: _______
  "scores": [85, 90, 78],     // Type: _______
  "address": {                // Type: _______
    "street": "123 Main St",
    "city": "San Francisco"
  }
}
```

---

## Activity 4: Making Your First API Request

**Setup**: Install the `requests` library

```bash
pip install requests
# OR
pip3 install requests
```

**Test the installation**:
```python
import requests
print("Requests library installed successfully!")
```

**Your first API call**:

```python
import requests

# Make a GET request to GitHub's API
response = requests.get("https://api.github.com")

# Check the status code
print(f"Status Code: {response.status_code}")

# Get the JSON data
data = response.json()

# Print the data
print(data)
```

**Run this code and observe**:
1. What is the status code? _______
2. What type of data did you get back? _______________________________________________________________________

**Output** (paste a sample here):
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 5: Exploring the GitHub API

**GitHub provides a public API**. Let's explore it:

**Example 1: Get information about a repository**

```python
import requests

# Get info about a public repository
response = requests.get("https://api.github.com/repos/octocat/Hello-World")
data = response.json()

print(f"Repository: {data['name']}")
print(f"Description: {data.get('description', 'No description')}")
print(f"Stars: {data['stargazers_count']}")
print(f"Language: {data.get('language', 'N/A')}")
```

**Try it**: Replace `octocat/Hello-World` with another repository (e.g., `microsoft/vscode`)

**Your output**:
_______________________________________________________________________
_______________________________________________________________________

**Example 2: Get a user's public information**

```python
import requests

# Get info about a GitHub user
username = "octocat"  # Try your own username!
response = requests.get(f"https://api.github.com/users/{username}")
data = response.json()

print(f"Username: {data['login']}")
print(f"Name: {data.get('name', 'N/A')}")
print(f"Bio: {data.get('bio', 'No bio')}")
print(f"Public Repos: {data['public_repos']}")
```

**Try it with your GitHub username**:
_______________________________________________________________________

---

## Activity 6: Working with JSON Data

**Practice parsing JSON**:

```python
import requests
import json

# Get data from an API
response = requests.get("https://api.github.com")

# Method 1: Use .json() method (recommended)
data = response.json()
print(type(data))  # What type is this?

# Method 2: Use json module
text = response.text
data2 = json.loads(text)  # Convert string to Python dict

# Pretty print JSON
print(json.dumps(data, indent=2))
```

**Exercise**: Write code that:
1. Fetches data from `https://api.github.com/users/octocat`
2. Extracts and prints:
   - The user's name
   - Number of followers
   - Number of public repositories

**Your code**:
```python

```

---

## Activity 7: Error Handling

**APIs can fail**. Let's handle errors gracefully:

```python
import requests

try:
    response = requests.get("https://api.github.com/users/nonexistentuser12345")
    
    # Check if request was successful
    if response.status_code == 200:
        data = response.json()
        print(f"User: {data['login']}")
    elif response.status_code == 404:
        print("User not found!")
    else:
        print(f"Error: Status code {response.status_code}")
        
except requests.exceptions.RequestException as e:
    print(f"Request failed: {e}")
```

**Practice**: Modify the code above to handle:
- 200 (success)
- 404 (not found)
- 403 (forbidden/rate limited)
- Other errors

**Your improved code**:
```python

```

---

## Activity 8: Exploring Other Public APIs

**Try these free, no-auth APIs**:

**1. JSONPlaceholder (fake data for testing)**:
```python
import requests

# Get a list of posts
response = requests.get("https://jsonplaceholder.typicode.com/posts/1")
data = response.json()
print(f"Title: {data['title']}")
print(f"Body: {data['body']}")
```

**2. Dog API (random dog images)**:
```python
import requests

response = requests.get("https://dog.ceo/api/breeds/image/random")
data = response.json()
print(f"Dog image URL: {data['message']}")
```

**3. Weather API (requires free API key, optional)**:
- Sign up at [OpenWeatherMap](https://openweathermap.org/api)
- Get your API key
- Make a request: `https://api.openweathermap.org/data/2.5/weather?q=London&appid=YOUR_API_KEY`

**Which API did you try?** _______________________________________________________________________

**What data did you get?** _______________________________________________________________________

---

## Deliverable Checklist

- [ ] Read "What is an API?" article
- [ ] Installed `requests` library
- [ ] Made first API call to `https://api.github.com`
- [ ] Explored GitHub API (repository or user info)
- [ ] Parsed and displayed JSON data
- [ ] (Optional) Tried other public APIs
- [ ] Pasted sample JSON output
- [ ] Saved JSON output sample in `Day0.5-API-Output.txt` or similar in Week0 folder

---

## Reflection Questions

1. **How do APIs differ from regular web pages?**
   _______________________________________________________________________
   _______________________________________________________________________

2. **What is the relationship between JSON and Python dictionaries?**
   _______________________________________________________________________

3. **Why is error handling important when working with APIs?**
   _______________________________________________________________________

4. **What real-world application could you build using APIs?**
   _______________________________________________________________________

---

## API Concepts Cheat Sheet

**Making Requests**:
```python
import requests

# GET request
response = requests.get("https://api.example.com/data")

# POST request (with data)
response = requests.post("https://api.example.com/data", json={"key": "value"})

# Check status
if response.status_code == 200:
    data = response.json()
```

**Working with JSON**:
```python
import json

# Parse JSON string to Python dict
data = json.loads(json_string)

# Convert Python dict to JSON string
json_string = json.dumps(data, indent=2)

# Or use response.json() directly
data = response.json()
```

**Error Handling**:
```python
try:
    response = requests.get(url, timeout=5)
    response.raise_for_status()  # Raises exception for bad status codes
    data = response.json()
except requests.exceptions.RequestException as e:
    print(f"Error: {e}")
```

---

## Additional Resources (Optional)

- [Postman Learning Center](https://learning.postman.com/docs/getting-started/introduction/)
- [HTTP Status Codes Reference](https://httpstatuses.com/)
- [JSON.org](https://www.json.org/json-en.html)
- [Public APIs List](https://github.com/public-apis/public-apis)

---

## Troubleshooting

**Common Issues**:

- **"ModuleNotFoundError: No module named 'requests'"**: Run `pip install requests`
- **"SSL Certificate Error"**: Usually means you're behind a proxy; may need to configure requests
- **"404 Not Found"**: Check the API endpoint URL
- **"Rate Limited"**: Too many requests; wait a bit and try again

**Error you encountered?** Note it here:
_______________________________________________________________________
_______________________________________________________________________

---

## Next Steps

Tomorrow (Day 0.6), you'll learn about GenAI tools and prompt engineering. No special setup needed—just access to an AI tool (Copilot, ChatGPT, Claude, etc.)!

