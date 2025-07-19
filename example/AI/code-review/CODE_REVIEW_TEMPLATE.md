# Code Review Template

## Review Summary
**Date:** [Current Date]
**Reviewer:** AI Assistant + [Your Name]
**Branch:** [Branch Name]
**Files Changed:** [Number of files]
**Lines Added/Removed:** [+X/-Y]

## Change Overview
Brief description of what was changed and why:
[Summary of changes]

## Review Categories

### 1. Code Quality (Critical)
**Score:** [1-5] (1=Poor, 5=Excellent)
**Issues Found:**
- [ ] **Critical:** [Description] - Line: [X] - Recommendation: [Fix]
- [ ] **High:** [Description] - Line: [X] - Recommendation: [Fix]
- [ ] **Medium:** [Description] - Line: [X] - Recommendation: [Fix]
- [ ] **Low:** [Description] - Line: [X] - Recommendation: [Fix]

**Positive Aspects:**
- [Good practices observed]
- [Well-implemented features]

### 2. Security Analysis (Critical)
**Score:** [1-5]
**Security Checklist:**
- [ ] Input validation implemented
- [ ] SQL injection prevention
- [ ] XSS protection measures
- [ ] Authentication/authorization checks
- [ ] Sensitive data handling
- [ ] Error information disclosure

**Issues Found:**
- [Security concerns with recommendations]

### 3. Performance Assessment (High)
**Score:** [1-5]
**Performance Checklist:**
- [ ] Efficient algorithms used
- [ ] Database queries optimized
- [ ] Caching implemented where appropriate
- [ ] Memory usage considerations
- [ ] Network request optimization

**Issues Found:**
- [Performance concerns with impact analysis]

### 4. Architecture Compliance (High)
**Score:** [1-5]
**Architecture Checklist:**
- [ ] Follows established patterns
- [ ] Proper separation of concerns
- [ ] Dependency injection used correctly
- [ ] Error handling consistency
- [ ] Logging implementation

**Issues Found:**
- [Architecture violations with suggestions]

### 5. Testing Coverage (High)
**Score:** [1-5]
**Testing Checklist:**
- [ ] Unit tests for new functionality
- [ ] Integration tests where needed
- [ ] Edge cases covered
- [ ] Mock usage appropriate
- [ ] Test readability and maintainability

**Issues Found:**
- [Testing gaps with recommendations]

### 6. Documentation (Medium)
**Score:** [1-5]
**Documentation Checklist:**
- [ ] Code comments where necessary
- [ ] API documentation updated
- [ ] README updated if needed
- [ ] AI usage documented
- [ ] Complex logic explained

**Issues Found:**
- [Documentation improvements needed]

### 7. AI Usage Review (Medium)
**AI-Generated Code Analysis:**
- [ ] AI usage properly documented
- [ ] Generated code reviewed by human
- [ ] AI suggestions validated
- [ ] Manual modifications documented
- [ ] Quality of AI-generated code acceptable

**AI Usage Issues:**
- [Concerns about AI-generated portions]

## Overall Assessment

### Summary Score: [Total Score]/35
- **Critical Issues:** [Count]
- **High Priority Issues:** [Count]
- **Medium Priority Issues:** [Count]
- **Low Priority Issues:** [Count]

### Recommendation:
- [ ] **Approve** - Ready for merge
- [ ] **Approve with Minor Changes** - Address low/medium issues
- [ ] **Needs Work** - Address high priority issues before merge
- [ ] **Reject** - Critical issues must be resolved

### Next Steps:
1. [Priority 1 action items]
2. [Priority 2 action items]
3. [Priority 3 action items]

### Positive Feedback:
[Acknowledge good practices and improvements]

### Learning Opportunities:
[Suggestions for future development]

## Review Checklist Completion
- [ ] All code changes analyzed
- [ ] Security implications considered
- [ ] Performance impact assessed
- [ ] Architecture compliance verified
- [ ] Testing adequacy evaluated
- [ ] Documentation completeness checked
- [ ] AI usage properly reviewed
- [ ] Actionable feedback provided
- [ ] Overall recommendation given
