# Day 0.6 Worksheet: Introduction to GenAI Tools

**Estimated Time**: 1–2 hours  
**Focus**: Understanding Large Language Models (LLMs), prompting, and AI coding assistants

---

## Learning Objectives

By the end of this session, you will be able to:
- Understand what Large Language Models (LLMs) are
- Learn how prompting guides AI behavior
- Practice crafting clear, effective prompts
- Use AI coding tools (Copilot, Cursor, etc.) for basic tasks

---

## Pre-Activity: What is AI?

**Think about AI in your daily life**:

- [ ] Voice assistants (Siri, Alexa)
- [ ] Recommendation systems (Netflix, Spotify)
- [ ] Chatbots (customer service)
- [ ] Image recognition (photo apps)
- [ ] Language translation
- [ ] Code completion (autocomplete)

**What do you think a "Large Language Model" is?**
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 1: Understanding LLMs

**Resource**: [OpenAI Prompt Engineering Guide](https://platform.openai.com/docs/guides/prompt-engineering)

**Read the introduction and key concepts section, then answer**:

1. **What is a Large Language Model (LLM)?**
   _______________________________________________________________________
   _______________________________________________________________________

2. **How do LLMs work?** (In simple terms)
   _______________________________________________________________________
   _______________________________________________________________________

3. **What is "prompting"?**
   _______________________________________________________________________
   _______________________________________________________________________

4. **Why is prompt quality important?**
   _______________________________________________________________________
   _______________________________________________________________________

---

## Activity 2: Prompt Engineering Basics

**Key Principles**:

1. **Be Clear and Specific**: Vague prompts → vague results
2. **Provide Context**: Give the AI enough information
3. **Use Examples**: Show what you want (few-shot learning)
4. **Iterate**: Refine your prompts based on results

**Example Comparison**:

❌ **Bad Prompt**: "Write code"
✅ **Good Prompt**: "Write a Python function that takes a list of numbers and returns the sum"

**Why is the second one better?**
_______________________________________________________________________

---

## Activity 3: Three Prompt Styles

**You'll practice three different prompt styles**:

### Style 1: Instructional Prompts

**Purpose**: Directly tell the AI what to do

**Example**: "Write a Python function that returns the square of a number"

**Your turn**: Write an instructional prompt for:
- Creating a function that calculates the area of a rectangle

**Your prompt**:
_______________________________________________________________________

**AI Response** (paste here):
_______________________________________________________________________
_______________________________________________________________________

**Evaluation**: 
- [ ] Did the AI understand your request?
- [ ] Was the code correct?
- [ ] Would you use this code?

---

### Style 2: Exploratory Prompts

**Purpose**: Ask the AI to explain or explore concepts

**Example**: "Explain what an API is using a cooking analogy"

**Your turn**: Write an exploratory prompt that asks the AI to:
- Explain a programming concept using an analogy

**Your prompt**:
_______________________________________________________________________

**AI Response** (paste here):
_______________________________________________________________________
_______________________________________________________________________

**Evaluation**:
- [ ] Was the explanation clear?
- [ ] Did the analogy help you understand?
- [ ] What did you learn?

---

### Style 3: Iterative Prompts

**Purpose**: Improve or refine something step by step

**Example**: 
1. Initial: "Improve the readability of this paragraph: [your text]"
2. Follow-up: "Make it more concise"
3. Follow-up: "Add a call-to-action at the end"

**Your turn**: 
1. Write a paragraph about why you're learning software engineering
2. Ask the AI to improve it
3. Then ask for a specific refinement

**Your original text**:
_______________________________________________________________________
_______________________________________________________________________

**First prompt** (improve readability):
_______________________________________________________________________

**AI Response** (paste here):
_______________________________________________________________________
_______________________________________________________________________

**Second prompt** (specific refinement):
_______________________________________________________________________

**AI Response** (paste here):
_______________________________________________________________________
_______________________________________________________________________

**Evaluation**:
- [ ] Did iterative prompting improve the result?
- [ ] How did the second prompt change the output?

---

## Activity 4: Prompting for Code Generation

**Practice generating code with AI**:

**Exercise 1: Simple Function**
- Prompt: "Write a Python function that checks if a number is even"
- Copy the generated code here:

```python

```

- Test it: Does it work? [ ] Yes [ ] No
- What would you improve?

**Exercise 2: With Context**
- Prompt: "Write a Python function that takes a list of student names and returns a dictionary with names as keys and their lengths as values"
- Copy the generated code here:

```python

```

- Test it: Does it work? [ ] Yes [ ] No
- How did providing more context help?

**Exercise 3: With Constraints**
- Prompt: "Write a Python function that finds the maximum number in a list, but handle the case where the list is empty by returning None"
- Copy the generated code here:

```python

```

- Test it: Does it work? [ ] Yes [ ] No
- Did the AI handle the edge case?

---

## Activity 5: Using AI Coding Assistants

**If you have access to GitHub Copilot, Cursor, or similar**:

### GitHub Copilot Setup (VS Code)

1. Install the GitHub Copilot extension
2. Sign in with your GitHub account
3. Enable Copilot Chat (if available)

**Try these Copilot features**:

**Feature 1: Inline Suggestions**
- Type a comment: `# Function to calculate factorial`
- Let Copilot suggest code
- Accept or modify the suggestion

**Feature 2: Copilot Chat**
- Open Copilot Chat (Ctrl+Shift+I or Cmd+Shift+I)
- Ask: "Explain what this code does: [paste some code]"
- Try: "Refactor this function to be more readable"

**Feature 3: Generate Tests**
- Write a function
- Ask Copilot: "Generate unit tests for this function"

**What did you try?** _______________________________________________________________________

**What worked well?** _______________________________________________________________________

**What was challenging?** _______________________________________________________________________

---

## Activity 6: Prompt Patterns for Software Engineering

**Common patterns you'll use in this course**:

### Pattern 1: Code Generation
```
"Write a [language] function that [does something]. 
It should [requirements]. 
Handle [edge cases]."
```

**Your example**:
_______________________________________________________________________

### Pattern 2: Code Explanation
```
"Explain what this code does:
[code block]

Focus on [specific aspect]."
```

**Your example**:
_______________________________________________________________________

### Pattern 3: Code Refactoring
```
"Refactor this code to [improvement]:
[code block]

Make it [specific changes]."
```

**Your example**:
_______________________________________________________________________

### Pattern 4: Debugging
```
"This code has an error:
[code block]

The error is: [error message]
Help me fix it."
```

**Your example**:
_______________________________________________________________________

---

## Activity 7: Evaluating AI Output

**Not all AI output is perfect**. Learn to evaluate:

**Checklist for AI-Generated Code**:
- [ ] Does it solve the problem?
- [ ] Is it readable and well-structured?
- [ ] Are edge cases handled?
- [ ] Does it follow best practices?
- [ ] Is it secure? (no obvious vulnerabilities)
- [ ] Does it have proper error handling?

**Practice**: Get AI to generate code, then evaluate it:

**Prompt**: "Write a function that divides two numbers"

**AI Code**:
```python

```

**Evaluation**:
- [ ] Solves the problem?
- [ ] Handles division by zero?
- [ ] Has proper error handling?
- [ ] Would you use this in production?

**If not perfect, what would you improve?**
_______________________________________________________________________

---

## Deliverable Checklist

- [ ] Read OpenAI Prompt Engineering Guide
- [ ] Created 3 instructional prompts and got responses
- [ ] Created 3 exploratory prompts and got responses
- [ ] Created 3 iterative prompts and refined output
- [ ] Generated code using AI and tested it
- [ ] (If available) Set up Copilot/Cursor and tried features
- [ ] Practiced evaluating AI output
- [ ] Created a markdown file with all prompts and responses
- [ ] Saved as `Day0.6-Prompts.md` in Week0 folder

---

## Creating Your Deliverable

**Create a file called `Day0.6-Prompts.md` with this structure**:

```markdown
# Day 0.6: Prompt Engineering Practice

## Instructional Prompts

### Prompt 1: [Your prompt]
**Response**: [AI response]

### Prompt 2: [Your prompt]
**Response**: [AI response]

### Prompt 3: [Your prompt]
**Response**: [AI response]

## Exploratory Prompts

### Prompt 1: [Your prompt]
**Response**: [AI response]

### Prompt 2: [Your prompt]
**Response**: [AI response]

### Prompt 3: [Your prompt]
**Response**: [AI response]

## Iterative Prompts

### Original Text: [Your text]
### Iteration 1: [First improvement prompt]
**Response**: [AI response]
### Iteration 2: [Second refinement prompt]
**Response**: [AI response]

## Code Generation Examples

### Example 1: [Description]
**Prompt**: [Your prompt]
**Code**: [Generated code]
**Evaluation**: [Your thoughts]

## Reflections

[Your reflections on prompt engineering]
```

---

## Reflection Questions

1. **What makes a good prompt?**
   _______________________________________________________________________
   _______________________________________________________________________

2. **How did different prompt styles produce different results?**
   _______________________________________________________________________

3. **What challenges did you face when using AI tools?**
   _______________________________________________________________________

4. **How will you use AI tools in this course?**
   _______________________________________________________________________

---

## Prompt Engineering Tips

**DO**:
- ✅ Be specific and clear
- ✅ Provide context and examples
- ✅ Break complex tasks into steps
- ✅ Iterate and refine
- ✅ Review and test AI output

**DON'T**:
- ❌ Be vague or ambiguous
- ❌ Assume the AI knows your context
- ❌ Accept output without reviewing
- ❌ Use AI for security-critical code without review
- ❌ Forget to cite AI-generated content

---

## Additional Resources (Optional)

- [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering)
- [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
- [Cursor Documentation](https://docs.cursor.com/)
- [Prompt Engineering Guide (Learn Prompting)](https://learnprompting.org/)

---

## Troubleshooting

**Common Issues**:

- **"AI doesn't understand my prompt"**: Try being more specific, add examples
- **"Code doesn't work"**: Test it, debug, ask AI to fix it
- **"Output is too generic"**: Provide more context, use few-shot examples
- **"Copilot not working"**: Check you're signed in, extension is enabled

**Issue you encountered?** Note it here:
_______________________________________________________________________
_______________________________________________________________________

---

## Next Steps

Tomorrow (Day 0.7), you'll synthesize everything you've learned and complete a readiness check. Make sure you have all your deliverables ready to upload!

