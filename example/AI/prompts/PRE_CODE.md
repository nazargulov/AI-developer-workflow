# Pre-Coding Task Analysis Prompt

## Context Loading
Load and analyze the following context files:
- AI/docs/main_context.md (always include)
- AI/docs/[domain]_context.md (if applicable to the task)
- AI/tasks/AI-Friendly Repository Structure looks wrong.md

## Task Analysis Workflow: Explore → Plan → Code → Review

### Step 1: Explore
**Prompt:**
```
# Task Exploration

## Context
Project: [Project Name]
Ticket ID: [TICKET-XXXXX]
Description: [Ticket Description]

## Repository Context
Please analyze the following:
- Technology stack and architecture
- Existing patterns and conventions
- Related components and dependencies
- Recent changes that might affect this task

## Analysis Request
1. Understand the business requirement
2. Identify affected system components
3. Map dependencies and integration points
4. Assess complexity and potential risks
5. Suggest the appropriate workflow pattern
```

### Step 2: Plan
**Prompt:**
```
# Development Planning

Based on the exploration above:

## Task Breakdown
Break this task into subtasks that can be 20-30% automated:
- [ ] Subtask 1: [Description with automation potential]
- [ ] Subtask 2: [Description with automation potential]
- [ ] Subtask 3: [Description with automation potential]

## Implementation Strategy
- Architecture approach: [How to fit into existing system]
- Key components to modify: [List of files/modules]
- Testing strategy: [Unit, integration, manual tests needed]
- Risk mitigation: [Potential issues and solutions]

## Development Environment Setup
- [ ] Create feature branch from main
- [ ] Set up Docker environment: `make setup`
- [ ] Run initial tests: `make test`
- [ ] Verify linting: `make lint`
```

### Step 3: Code Preparation
**Prompt:**
```
# Code Implementation Guidance

## Implementation Guidelines
- Follow existing patterns in the codebase
- Use established architectural conventions
- Implement proper error handling
- Add comprehensive logging
- Write tests alongside implementation

## Quality Checks
Before starting implementation:
- [ ] Environment is properly set up
- [ ] All tests are passing
- [ ] Linting rules are satisfied
- [ ] Dependencies are up to date

## Implementation Notes
- Start with the simplest subtask
- Test each component as you build
- Commit small, logical changes
- Document any deviations from the plan
```

### Step 4: Review Preparation
**Prompt:**
```
# Self-Review Checklist

Before submitting for team review:
- [ ] All planned subtasks completed
- [ ] Tests are passing (make test)
- [ ] Code follows linting rules (make lint)
- [ ] AI-generated portions are documented
- [ ] Performance implications considered
- [ ] Security considerations addressed
- [ ] Documentation updated if needed

## AI Usage Documentation
Document in your MR description:
- Which parts were AI-generated (1-2 sentences)
- What prompts or patterns were used
- Any manual modifications needed
- Lessons learned for future tasks
```

## Expected Outputs
- Clear task breakdown with realistic scope
- Ready-to-use development environment
- Implementation roadmap with checkpoints
- Self-review preparation

## Workflow Pattern Selection Guide
- **Complex features** → Explore → Plan → Code → Review
- **Experimental work** → Prototype → Rewrite → Improve  
- **Automation tasks** → Build → Integrate → Delegate → Iterate
