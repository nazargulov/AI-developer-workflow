# Development Rules for AI Usage

## Core Principles

### 🔍 **Review Responsibility**
- **YOU MUST** review every line of code thoughtfully before MR submission
- **YOU MUST** understand what the AI-generated code does
- **YOU MUST** take ownership of all code, regardless of how it was created
- **Remember:** Git blame will show your name

### 📝 **Documentation Requirements**
- **Document AI usage** in MR descriptions (1-2 sentences about what AI generated)
- **Update documentation** when adding new features or changing behavior
- **Comment complex logic** especially if AI-generated and modified
- **Maintain README** and API documentation current

### 🛡️ **Quality Gates**
- **Use self-review** with AI before team review (AI/code-review/HOW_TO_USE.md)
- **Run all tests** before submitting MR (`make test`)
- **Check linting** and fix issues (`make lint`)
- **Verify functionality** manually when appropriate

## AI Usage Guidelines

### ✅ **Best Practices**
1. **Choose the right workflow pattern:**
   - Complex features → Explore → Plan → Code → Review
   - Experimental work → Prototype → Rewrite → Improve
   - Automation tasks → Build → Integrate → Delegate → Iterate

2. **Context Engineering:**
   - Use AI/docs for sufficient, not excess context
   - Load relevant domain context files
   - Provide clear, specific prompts

3. **Incremental Development:**
   - Break tasks into small, testable pieces
   - Commit logical, atomic changes
   - Test each increment before moving forward

### ❌ **What to Avoid**
- **Don't** blindly trust AI suggestions
- **Don't** add unnecessary dependencies without checking built-in alternatives
- **Don't** submit unreviewed AI-generated code
- **Don't** use AI for security-critical code without extra validation
- **Don't** rely on AI for complex business logic without human verification

### 🔄 **Process Requirements**
1. **Discuss controversial AI advice** in MR comments
2. **Share findings and learnings** in team chat channels
3. **Document critical prompts** in AI/prompts/ for reuse
4. **Report AI tool issues** to help improve team practices

## Code Quality Standards

### 🏗️ **Architecture**
- Follow established patterns in the codebase
- Maintain separation of concerns
- Use dependency injection appropriately
- Implement proper error handling
- Add comprehensive logging

### 🧪 **Testing**
- Write tests for all new functionality
- Maintain or improve test coverage
- Include edge case testing
- Use appropriate mocking strategies
- Ensure tests are readable and maintainable

### 🚀 **Performance**
- Consider performance implications of changes
- Use efficient algorithms and data structures
- Implement caching where appropriate
- Monitor memory usage in resource-intensive operations
- Profile critical paths when needed

### 🔒 **Security**
- Validate all inputs
- Sanitize outputs to prevent XSS
- Use parameterized queries to prevent SQL injection
- Implement proper authentication and authorization
- Handle sensitive data appropriately
- Don't expose internal errors to users

## AI Tool Specific Guidelines

### 💬 **Prompt Engineering**
- Be specific about requirements and constraints
- Provide relevant context from AI/docs
- Ask for explanations of complex generated code
- Request multiple approaches for comparison
- Validate AI responses against project standards

### 🔧 **Tool Integration**
- Use Cursor for code completion and generation
- Use ChatGPT for complex problem solving and planning
- Use GitHub Copilot for routine code patterns
- Use Diff Critic for automated MR reviews
- Document which tools work best for which tasks

### 📊 **Quality Monitoring**
- Track AI usage and effectiveness
- Monitor code quality metrics
- Assess time savings vs. quality trade-offs
- Share successful prompting strategies
- Report tools and techniques that don't work well

## Team Collaboration

### 🗣️ **Communication**
- **Discuss AI suggestions** that seem questionable
- **Share successful patterns** and prompting strategies
- **Ask for help** when AI suggestions are unclear
- **Provide feedback** on team AI practices
- **Mentor others** in effective AI usage

### 📚 **Knowledge Sharing**
- Update AI/prompts with effective prompts
- Document lessons learned in AI/tasks
- Share workflow improvements with the team
- Contribute to AI/docs when domain knowledge grows
- Participate in AI practice discussions

### 🎯 **Continuous Improvement**
- Regularly assess AI integration effectiveness
- Experiment with new tools and techniques
- Provide feedback on team processes
- Suggest improvements to AI workflows
- Measure and report on productivity gains

## Violation Consequences

### ⚠️ **Minor Violations**
- Undocumented AI usage → Document in follow-up commit
- Missing self-review → Complete review before approval
- Inadequate testing → Add tests before merge

### 🚨 **Major Violations**
- Unreviewed AI-generated code → MR rejection, mandatory re-review
- Security issues → Immediate fix required, security review
- Broken functionality → Rollback, root cause analysis

### 🔄 **Learning Opportunities**
- Use violations as teaching moments
- Update processes based on common issues
- Share learnings with the team
- Improve AI/rules based on experience

## Regular Reviews

- **Monthly team review** of AI practices and effectiveness
- **Quarterly assessment** of AI tool ROI and satisfaction
- **Continuous updates** to rules based on new tools and learnings
- **Annual strategy review** for AI integration roadmap
