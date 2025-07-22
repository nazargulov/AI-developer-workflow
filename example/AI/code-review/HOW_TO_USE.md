Base rule: Check that you have completed all steps and mark them as done.

1. git diff:

   - git diff development -- '_.js' '_.html' '_.css' '_.yml' >> AI/code-review/code-changes.txt

   Expected Output: A file named code-changes.txt containing the differences between the current branch and development for specified file types.

   Common Issues: Ensure you are on the correct branch and have the latest changes pulled from development.

2. Add to context:

   - AI/code-review/code-changes.txt
   - AI/code-review/CODE_REVIEW_TEMPLATE.md

   Dependencies: Ensure both files exist and are up-to-date.

3. Prompt:
   Perform a code review based on the given template

4. Save your review to the file AI_REVIEW.md

5. Check that you have completed all steps and mark them as done.

Checklist:

- [ ] Generate git diff
- [ ] Add files to context
- [ ] Perform code review
- [ ] Save review to AI_REVIEW.md
- [ ] Verify all steps are completed

Feedback Loop:

- Provide feedback on these instructions to improve the process.
