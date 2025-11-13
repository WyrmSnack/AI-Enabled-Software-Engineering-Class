# Week 3, Day 12 Worksheet: External Tools Integration

**Estimated Time**: 4–5 hours (90 min lecture + 3–4 hr lab)  
**Focus**: Copilot Agent, MCP servers, agent workflows, PR reviews with AI

---

## Learning Objectives

By the end of Day 12, you will be able to:
- Understand and configure Copilot Agent workflows
- Set up MCP server support for GitHub Copilot
- Assign issues to agents and configure testing environments
- Use AI for PR reviews
- Understand governance and best practices for autonomous agents

---

## Pre-Activity: Understanding Autonomous Agents

**What are agents?**
- AI systems that can perform multi-step tasks autonomously
- Can read code, make changes, run tests
- Work with issues, PRs, and workflows
- Need proper governance and oversight

**Think about**:
- What tasks would benefit from automation?
- What should agents be allowed to do?
- How do you ensure quality with autonomous agents?

**Your thoughts**:
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 1: Understanding Copilot Agent

### Agent Capabilities

**What agents can do**:
- Read and understand code
- Make code changes
- Run tests
- Create PRs
- Respond to issues
- Follow workflows

**What agents need**:
- Clear instructions
- Proper context
- Testing environment
- Governance rules

### Activity: Explore Agent Features

**Research Copilot Agent**:
- Read: [Copilot Chat/Agents Documentation](https://docs.github.com/en/copilot/using-github-copilot/copilot-chat)

**Key features**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________

**How agents differ from chat**:
_______________________________________________________________________

---

## Activity 2: Configure Agent Workflow

### Activity: Set Up Agent for Issue Assignment

**Step 1: Create a Test Issue**

**In your GitHub repository**:
- Create an issue: "Add user authentication endpoint"
- Include acceptance criteria
- Label appropriately

**Issue created?** [ ] Yes  
**Issue URL**: _______________________________________________________________________

**Step 2: Configure Agent Workflow**

**Prompt** (if using Agent mode):
```
Set up a workflow where the Copilot Agent can:
- Read GitHub issues
- Understand requirements
- Create a branch
- Implement the feature
- Run tests
- Create a PR

Configure this for issue: [your issue number]
```

**Or manually configure** (if Agent setup is different):

**Configuration steps**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________

**Agent configured?** [ ] Yes

### Activity: Assign Issue to Agent

**Test assignment**:
- Assign issue to agent (if feature available)
- Or simulate: Create a detailed prompt for agent

**Prompt for agent**:
```
Work on GitHub issue #[issue number]: [issue title]

Requirements:
- [Requirement 1]
- [Requirement 2]
- [Requirement 3]

Steps:
1. Create a feature branch
2. Implement the feature
3. Add tests
4. Ensure all tests pass
5. Create a PR

Follow the project's coding standards and patterns.
```

**Agent response/work**:
_______________________________________________________________________
_______________________________________________________________________

**Review agent's work**:
- [ ] Code quality acceptable?
- [ ] Tests included?
- [ ] Follows patterns?
- [ ] PR created?

---

## Activity 3: Set Up Unit Testing Environment for Agent

### Activity: Configure Testing for Agents

**Agents need**:
- Clear test structure
- Test commands defined
- Success criteria
- Failure handling

**Prompt**:
```
Configure a testing environment for AI agents working on this project.

Requirements:
- Agents should run `pytest` before committing
- Tests must pass for PR to be created
- Clear error messages if tests fail
- Test coverage should be maintained
- Use GitHub Actions for CI

Create configuration and documentation.
```

**AI Configuration**:
_______________________________________________________________________
_______________________________________________________________________

**Configuration created?** [ ] Yes

**Test it**:
- Create a test issue
- Assign to agent (or simulate)
- Verify tests run

**Tests run automatically?** [ ] Yes

---

## Activity 4: PR Review with AI

### Understanding AI-Powered PR Reviews

**AI can review**:
- Code quality
- Test coverage
- Security issues
- Performance concerns
- Style consistency
- Best practices

### Activity: Generate PR Review

**Step 1: Create a PR**

**Create a PR with some code changes** (can be from previous work)

**PR URL**: _______________________________________________________________________

**Step 2: Use AI to Review PR**

**Prompt** (with PR context):
```
Review this pull request: [PR description/context]

Check for:
- Code quality and readability
- Test coverage
- Security vulnerabilities
- Performance issues
- Adherence to coding standards
- Missing error handling
- Documentation
- Breaking changes

Provide:
- Overall assessment
- Specific issues found
- Suggestions for improvement
- Approval recommendation
```

**AI Review**:
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

**Issues found**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________

**Address issues**: [ ] Done

### Activity: Automated PR Review Workflow

**Prompt**:
```
Create a GitHub Actions workflow for automated PR reviews using AI.

The workflow should:
- Trigger on PR creation/updates
- Analyze code changes
- Check for common issues
- Comment on the PR with findings
- Block merge if critical issues found
- Use appropriate AI tools/services
```

**AI-Generated Workflow**:
```yaml
[Paste workflow]
```

**Workflow created?** [ ] Yes  
**Tested?** [ ] Yes

---

## Activity 5: MCP Server Support

### Understanding MCP (Model Context Protocol)

**MCP** = Protocol for connecting AI to external tools and data

**Benefits**:
- Access to databases
- Integration with external APIs
- Custom tooling
- Enhanced context

### Activity: Research MCP

**Read**: [Model Context Protocol](https://modelcontextprotocol.io/)

**Key concepts**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________

**How MCP helps**:
_______________________________________________________________________

### Activity: Set Up MCP Server (If Available)

**If MCP is available in your environment**:

**Configuration steps**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________

**MCP configured?** [ ] Yes [ ] Not available

**What MCP server would be useful for your project?**
_______________________________________________________________________

---

## Activity 6: Agent Governance

### Understanding Governance

**Why governance matters**:
- Agents make autonomous decisions
- Need boundaries and rules
- Quality must be maintained
- Security concerns

### Activity: Create Agent Governance Policy

**Prompt**:
```
Create an agent governance policy for AI agents working on this codebase.

Include:
- What agents are allowed to do
- What requires human approval
- Code quality requirements
- Testing requirements
- Security restrictions
- Review process
- Rollback procedures
- Monitoring and logging

Format as a clear policy document.
```

**AI-Generated Policy**:
_______________________________________________________________________
_______________________________________________________________________

**Your customized policy**:
_______________________________________________________________________

**Policy file**: `docs/agent-governance.md`

**Policy created?** [ ] Yes

---

## Activity 7: Build a Copilot Extension (Optional)

### Understanding Extensions

**Extensions** = Custom tools that enhance Copilot

**Use cases**:
- Custom code analysis
- Integration with internal tools
- Domain-specific helpers
- Custom workflows

### Activity: Design Extension (Even if Not Built)

**Prompt**:
```
Design a GitHub Copilot extension for: [your use case]

Include:
- Purpose and use cases
- How it integrates with Copilot
- What it does
- Configuration needed
- Benefits for developers

Create a design document.
```

**Your extension idea**:
_______________________________________________________________________

**AI Design**:
_______________________________________________________________________
_______________________________________________________________________

**Design documented?** [ ] Yes

---

## Activity 8: Create Deliverables

### Deliverable 1: Configured Agent Workflow

**What you configured**:
_______________________________________________________________________

**Files created**:
- _______________________________________________________________________

**Agent workflow working?** [ ] Yes

### Deliverable 2: Sample PR Review

**PR reviewed**: _______________________________________________________________________

**Review findings documented?** [ ] Yes

**File**: `week3/day12/pr-review-sample.md`

### Deliverable 3: Agent Governance Policy

**Policy file**: `docs/agent-governance.md`

**Policy created?** [ ] Yes

### Deliverable 4: AI Usage Log

**File**: `week3/day12/AI-Usage-Log.md`

**Document**:
- Agent configuration prompts
- PR review prompts
- MCP research/configuration
- Governance policy creation
- What worked
- What didn't work

**AI Usage Log created?** [ ] Yes

---

## Deliverable Checklist

- [ ] Researched Copilot Agent capabilities
- [ ] Configured agent workflow
- [ ] Set up testing environment for agents
- [ ] Tested issue assignment (or simulated)
- [ ] Performed AI-powered PR review
- [ ] Created automated PR review workflow (optional)
- [ ] Researched MCP protocol
- [ ] Created agent governance policy
- [ ] Designed extension (optional)
- [ ] Documented all AI usage
- [ ] Committed to repository
- [ ] Created PR with agent setup

---

## Reflection Questions

1. **What are the benefits and risks of autonomous agents?**
   _______________________________________________________________________
   _______________________________________________________________________

2. **How would you use agents in your workflow?**
   _______________________________________________________________________

3. **What governance is needed for agents?**
   _______________________________________________________________________

4. **How did AI help with PR reviews?**
   _______________________________________________________________________

---

## Key Takeaways

**Remember**:
- ✅ Agents can automate repetitive tasks
- ✅ Governance is essential for agents
- ✅ Testing must be automated for agents
- ✅ PR reviews benefit from AI assistance
- ✅ MCP extends AI capabilities
- ✅ Always review agent work

**Best practices**:
- Start with simple agent tasks
- Define clear success criteria
- Require tests for all agent work
- Review agent PRs carefully
- Monitor agent behavior
- Have rollback plans

---

## Additional Resources

- [Copilot Chat/Agents Overview](https://docs.github.com/en/copilot/using-github-copilot/copilot-chat)
- [Copilot Extensions](https://docs.github.com/en/copilot/extensions)
- [Model Context Protocol](https://modelcontextprotocol.io/)
- [AI Agent Best Practices](https://docs.github.com/en/copilot/managing-copilot/managing-copilot-for-your-enterprise)

---

## Next Steps

**Days 13-15: Capstone Project!**

You're ready to build your full-stack application using all the skills you've learned!

**Make sure you**:
- Understand agent capabilities
- Have governance in place
- Are ready to apply everything
- Have your project plan ready

**Let's build something amazing!** 🚀

