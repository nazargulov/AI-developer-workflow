# Development Cycle Prompts

## Iterative Development Loop

### Core Development Cycle
```bash
# Continuous AI-Assisted Development
while [ $task_complete = false ]; do
  1. Write code with AI assistance
  2. Run automated tests: make test
  3. Check linting: make lint
  4. AI code review: AI/code-review/HOW_TO_USE.md
  5. Iterate based on feedback
done
```

## Code Generation Prompts

### Feature Implementation
**Prompt:**
```
# Feature Implementation

## Context
Current task: [Subtask from planning phase]
Files to modify: [Specific files identified]
Existing patterns: [Reference to similar implementations]

## Implementation Request
1. Generate code following existing patterns
2. Include proper error handling
3. Add appropriate logging
4. Write corresponding tests
5. Update documentation if needed

## Quality Requirements
- Follow project coding standards
- Use established architectural patterns
- Include input validation
- Handle edge cases appropriately
- Maintain backward compatibility
```

### Bug Fix Implementation
**Prompt:**
```
# Bug Fix Implementation

## Issue Analysis
Bug description: [Description from ticket]
Affected components: [List of affected areas]
Root cause hypothesis: [Initial analysis]

## Fix Strategy
1. Reproduce the issue locally
2. Write a failing test that captures the bug
3. Implement minimal fix
4. Verify fix with tests
5. Check for similar issues elsewhere

## Validation Steps
- [ ] Bug is reproducible
- [ ] Test fails before fix
- [ ] Test passes after fix
- [ ] No regression in existing functionality
- [ ] Edge cases are handled
```

## Testing Prompts

### Test Generation
**Prompt:**
```
# Test Case Generation

## Context
Component under test: [Component name]
Functionality: [What it should do]
Edge cases: [Known edge cases]

## Test Requirements
Generate comprehensive tests covering:
1. Happy path scenarios
2. Error conditions
3. Edge cases and boundary conditions
4. Integration points
5. Performance considerations

## Test Structure
- Unit tests for individual functions
- Integration tests for component interactions
- Mock external dependencies appropriately
- Use descriptive test names
- Include setup and teardown as needed
```

## Refactoring Prompts

### Code Improvement
**Prompt:**
```
# Code Refactoring

## Refactoring Target
Component: [Component to refactor]
Issues: [Performance, maintainability, complexity]
Goals: [What to improve]

## Refactoring Guidelines
1. Maintain existing functionality
2. Improve code readability
3. Reduce complexity where possible
4. Follow DRY principles
5. Enhance testability

## Safety Measures
- [ ] Comprehensive test coverage exists
- [ ] All tests pass before refactoring
- [ ] Incremental changes with frequent testing
- [ ] Performance benchmarks if applicable
- [ ] Backward compatibility maintained
```

## Debugging Prompts

### Issue Investigation
**Prompt:**
```
# Debugging Investigation

## Problem Description
Issue: [Specific problem observed]
Environment: [Where it occurs]
Steps to reproduce: [How to trigger the issue]
Expected vs actual behavior: [What should happen vs what happens]

## Investigation Steps
1. Analyze error logs and stack traces
2. Check recent changes that might be related
3. Isolate the problem to specific components
4. Create minimal reproduction case
5. Propose and test potential solutions

## Analysis Request
- Review relevant code sections
- Identify potential root causes
- Suggest debugging approaches
- Recommend fixes with risk assessment
```

## Performance Optimization Prompts

### Performance Analysis
**Prompt:**
```
# Performance Optimization

## Performance Context
Component: [Component with performance issues]
Metrics: [Current performance measurements]
Goals: [Target performance improvements]
Constraints: [Memory, CPU, response time limits]

## Optimization Strategy
1. Profile current performance
2. Identify bottlenecks
3. Propose optimization techniques
4. Implement changes incrementally
5. Measure and validate improvements

## Optimization Areas
- Database query optimization
- Caching strategies
- Algorithm improvements
- Resource usage reduction
- Asynchronous processing opportunities
```
