# Code Review Prompts

## Self-Review Process

### Pre-Review Checklist
**Prompt:**
```
# Self-Review Preparation

## Context Analysis
Load current changes: AI/code-review/code-changes.txt
Review against: AI/rules/DEV_RULES.md
Check patterns from: AI/docs/main_context.md

## Self-Review Questions
1. Does this code follow established patterns?
2. Are there any potential security vulnerabilities?
3. Is error handling comprehensive and appropriate?
4. Can this implementation be simplified?
5. Are there built-in alternatives to new dependencies?
6. Is the code well-documented and self-explanatory?
7. Are edge cases properly handled?

## Quality Gates
- [ ] All tests pass
- [ ] Linting rules satisfied
- [ ] No obvious performance issues
- [ ] Security considerations addressed
- [ ] Documentation updated if needed
```

### AI-Generated Code Review
**Prompt:**
```
# AI Code Review Analysis

## Code Review Context
Changes: [Git diff content]
Patterns: [Project coding patterns]
Rules: [Team development rules]

## Review Areas
Analyze the code changes for:
1. **Code Quality**
   - Readability and maintainability
   - Adherence to coding standards
   - Proper error handling
   - Performance implications

2. **Security Issues**
   - Input validation
   - SQL injection prevention
   - XSS protection
   - Authentication/authorization

3. **Architecture Compliance**
   - Following established patterns
   - Proper separation of concerns
   - Dependency management
   - Integration points

4. **Testing Coverage**
   - Unit test completeness
   - Integration test needs
   - Edge case coverage
   - Mock usage appropriateness

## Review Output Format
For each issue found:
- **Severity**: Critical/High/Medium/Low
- **Category**: [Security/Performance/Maintainability/Style]
- **Description**: Clear explanation of the issue
- **Suggestion**: Specific improvement recommendation
- **Example**: Code example if helpful
```

## Team Review Prompts

### MR Review Assistant
**Prompt:**
```
# Merge Request Review Assistant

## Review Preparation
MR Title: [Title]
Description: [MR description]
AI Usage: [Documented AI usage from author]
Changes: [Summary of changes]

## Review Focus Areas
1. **Business Logic Correctness**
   - Does the implementation meet requirements?
   - Are business rules properly enforced?
   - Is the user experience considered?

2. **Technical Implementation**
   - Code quality and maintainability
   - Performance and scalability
   - Error handling and edge cases
   - Testing adequacy

3. **AI Usage Validation**
   - Review documented AI usage
   - Verify AI-generated code quality
   - Check for over-reliance on AI
   - Validate human oversight

## Review Questions
- Is the implementation approach sound?
- Are there any missing requirements?
- What are the potential risks?
- How does this affect other components?
- Is the documentation sufficient?
```

### Code Review Feedback
**Prompt:**
```
# Constructive Review Feedback

## Feedback Guidelines
When providing code review feedback:
1. Be specific and actionable
2. Explain the "why" behind suggestions
3. Provide examples when helpful
4. Consider the author's experience level
5. Balance criticism with recognition

## Feedback Templates

### For Improvements:
"Consider [specific suggestion] because [reason]. This would improve [aspect] by [benefit]. Example: [code example if helpful]"

### For AI-Generated Code:
"This AI-generated section looks good overall. I'd suggest reviewing [specific area] for [reason] and consider [alternative approach]."

### For Learning Opportunities:
"This works, but there's a more idiomatic way to achieve this. Check out [pattern/resource] which would [benefit]."

## Review Completion
- [ ] All concerns addressed
- [ ] Suggestions are actionable
- [ ] Positive aspects acknowledged
- [ ] Learning opportunities highlighted
- [ ] Final approval criteria clear
```
