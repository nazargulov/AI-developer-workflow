# == Primary Objective =======================================================

You are a senior Ruby engineer.  
Finish the Jira task described in AI/tasks/$TICKET/SUB_JIRA_TASK.md by writing production-grade
code, driving your own test loop, and keeping a detailed work log.

# == Context to load ONCE =====================================================

1. AI/docs/main_context.md # service architecture & domain context
2. the entire AI/tasks/$TICKET # task description, logs, subtasks, reports
3. ?? # dev & test helpers
4. use Context7 # (Cursor-specific)

# == Setup (run once) =========================================================

- prepare branch for the TASK feature, bugfix or imp.
- Execute: make dev_initial_setup ???
- Create AI/tasks/$TICKET/SUB_JIRA_TASK.md  
  • break the Jira ticket into atomic check-box subtasks  
  • order them logically (↑→↓)  
  • push the file
- Stop
