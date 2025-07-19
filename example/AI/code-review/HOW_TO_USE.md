# How to Use AI Code Review

Base rule: Check that you have completed all steps and mark them as done.

## 1. Generate Git Diff
**Command:**
```bash
git diff main -- '*.js' '*.html' '*.css' '*.md' >> AI/code-review/code-changes.txt
```

**Expected Output**: A file named `code-changes.txt` containing the differences between the current branch and `main` for specified file types.

**Common Issues**: Ensure you are on the correct branch and have the latest changes pulled from `main`.

## 2. Add Context to AI Tool
Load the following files into your AI assistant:
- `AI/code-review/code-changes.txt` (your changes)
- `AI/code-review/CODE_REVIEW_TEMPLATE.md` (review template)
- `AI/docs/main_context.md` (project context)
- `AI/rules/DEV_RULES.md` (development rules)

**Dependencies**: Ensure all files exist and are up-to-date.

## 3. Execute Review Prompt
Use this prompt:
```
Perform a comprehensive code review based on the provided template and development rules. 
Analyze the changes in code-changes.txt against project standards and best practices.
```

## 4. Save Review Results
Save the AI-generated review to: `AI/code-review/AI_REVIEW.md`

Include:
- Summary of changes
- Issues found (with severity levels)
- Suggestions for improvement
- Compliance with development rules
- Overall quality assessment

## 5. Review Validation Checklist
Mark as completed:
- [ ] Git diff generated successfully
- [ ] All context files loaded
- [ ] AI review completed
- [ ] Review saved to AI_REVIEW.md
- [ ] Personal review of AI suggestions done
- [ ] Action items identified and prioritized

## 6. Implementation of Feedback
Based on the AI review:
- Address critical and high-priority issues
- Consider medium-priority suggestions
- Document decisions on items not addressed
- Re-run review after significant changes

## 7. Pre-MR Submission Final Check
Before submitting your merge request:
- [ ] All critical issues resolved
- [ ] Tests updated if needed
- [ ] Documentation updated
- [ ] AI usage documented in MR description
- [ ] Self-review process completed

## Troubleshooting

### Common Issues:
1. **Empty code-changes.txt**: Check your git diff command and file paths
2. **AI context errors**: Verify all referenced files exist
3. **Incomplete review**: Ensure all code changes are covered
4. **Tool limitations**: Some complex changes may need manual review

### Getting Help:
- Check AI/rules/DEV_RULES.md for team standards
- Reference AI/docs/ for project context
- Ask team members for guidance on complex issues
- Use AI/prompts/ for additional prompt templates

## Feedback and Improvement
- Document issues with this process
- Suggest improvements to the team
- Share successful review patterns
- Update templates based on experience
