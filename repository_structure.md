# AI-Friendly Repository Structure Guide

## Complete Repository Structure

```
app/
├── AI/                           # Central AI workspace
│   ├── docs/                     # AI-optimized context documentation
│   │   ├── main_context.md      # Primary project context for AI
│   │   ├── payment_context.md   # Payment domain specific context
│   │   ├── business_context.md  # Business logic context
│   │   ├── user_context.md      # User management context
│   │   └── security_context.md  # Security and compliance context
│   ├── code-review/              # Self-review tools and templates
│   │   ├── HOW_TO_USE.md        # Step-by-step review process
│   │   ├── CODE_REVIEW_TEMPLATE.md # Review checklist template
│   │   ├── AI_REVIEW.md         # Generated review results
│   │   └── code-changes.txt     # Git diff output for analysis
│   ├── prompts/                  # Critical prompts collection
│   │   ├── PRE_CODE.md          # Pre-development planning
│   │   ├── CODE.md              # Development cycle prompts
│   │   ├── EXPLORE.md           # Codebase exploration
│   │   └── TICKET_SUMMARY.md    # Task analysis templates
│   ├── rules/                    # Team AI guidelines
│   │   ├── DEV_RULES.md         # Development best practices
│   │   └── AI_USAGE_POLICY.md   # AI usage guidelines
│   ├── tasks/                    # Example solutions
│   │   ├── completed/           # Successfully solved tasks
│   │   └── patterns/            # Common solution patterns
│   └── presentation/             # Knowledge sharing materials
├── Makefile                      # Automated development workflows
├── Dockerfile                    # Consistent development environment
├── docker-compose.yml           # Service orchestration
├── README.md                    # Human-readable project overview
└── [standard project structure]
```

## Key Files Explanation

### AI/docs/ Directory - AI Context Documentation

**Purpose:** Provide structured, AI-optimized project context
**Benefits:**

- Replaces generic README with targeted AI documentation
- Multiple context files for different domains/scenarios
- Significantly improves AI understanding and suggestion quality

#### AI/docs/main_context.md

**Purpose:** Primary project context for all AI interactions
**Content:**

- Project overview and technology stack
- Key business domains and critical paths
- Development patterns and architectural decisions
- Security, performance, and compliance requirements

### AI/code-review/HOW_TO_USE.md

**Purpose:** Step-by-step self-review process
**Usage:** Before submitting any MR
**Workflow:**

1. Generate git diff
2. Add context files
3. Run AI review
4. Save results
5. Verify completion

### AI/prompts/ Directory

**Purpose:** Store and version control effective prompts
**Examples:**

- Pre-coding task analysis
- Development cycle automation
- Code review templates
- Exploration and discovery

### Makefile Integration

**Purpose:** Standardized commands for AI workflows
**Example commands:**

```bash
make ai-review     # Run self-review process
make ai-setup      # Prepare development environment
make ai-test       # AI-assisted testing cycle
```

## AI Context Optimization

### README.md Structure for AI

```markdown
# Project Name

## Quick Start for AI

- Technology stack: Ruby on Rails, PostgreSQL, Redis
- Key patterns: Service objects, Interactors, Decorators
- Testing: RSpec, FactoryBot
- Code style: Rubocop with custom rules

## AI-Relevant Information

- Business domain: Online platform
- Critical paths: Payment processing, core business integration
- Security considerations: PCI compliance, fraud prevention
- Performance requirements: High availability, low latency

## Development Workflow

1. Use AI/prompts for task preparation
2. Follow AI/rules for code quality
3. Apply AI/code-review before submission
```

### Dockerfile for AI Development

```dockerfile
# AI-friendly development environment
FROM ruby:3.1

# Install AI-helpful tools
RUN apt-get update && apt-get install -y \
    git \
    make \
    curl \
    jq

# Set up consistent environment
WORKDIR /app
COPY Gemfile* ./
RUN bundle install

# Prepare AI workspace
RUN mkdir -p AI/code-review
RUN mkdir -p AI/prompts
RUN mkdir -p AI/rules

# Development setup
COPY . .
RUN make setup-ai-tools

EXPOSE 3000
CMD ["rails", "server", "-b", "0.0.0.0"]
```

## Effective Prompting Examples

### Pre-Coding Prompt Template

```markdown
# Task Analysis Prompt

## Context

Project: #{project_name}
Ticket: #{ticket_id}
Description: #{ticket_description}

## Repository Context

Technology Stack: #{tech_stack}
Key Patterns: #{patterns}
Recent Changes: #{recent_commits}

## Analysis Request

1. Break down this task into subtasks (max 30% AI automation)
2. Identify affected files and components
3. Suggest implementation approach
4. Create development checklist
5. Flag potential risks or dependencies

## Expected Output Format

- [ ] Subtask 1: [description]
- [ ] Subtask 2: [description]
- Risk: [potential issues]
- Dependencies: [required components]
```

### Development Cycle Prompt

```markdown
# Iterative Development Prompt

## Current State

Branch: #{branch_name}
Last commit: #{commit_hash}
Failing tests: #{test_failures}
Lint issues: #{lint_issues}

## Request

1. Analyze current implementation
2. Fix failing tests
3. Resolve lint issues
4. Suggest next development step
5. Maintain code quality standards

## Constraints

- Follow existing patterns
- Don't add heavy dependencies
- Ensure backward compatibility
- Write comprehensive tests
```

## Team Integration Best Practices

### Onboarding New Developers

1. **Setup AI workspace:** `make setup-ai`
2. **Review AI/rules:** Understand team guidelines
3. **Practice with AI/code-review:** Learn self-review process
4. **Study AI/tasks/patterns:** See successful examples

### Knowledge Sharing Process

1. **Document successful prompts** in AI/prompts
2. **Share insights** in team chat channels
3. **Update best practices** in AI/rules
4. **Create examples** in AI/tasks

### Quality Assurance

1. **Mandatory self-review** using AI tools
2. **Document AI usage** in MR descriptions
3. **Validate suggestions** against team rules
4. **Continuous improvement** based on feedback

## Metrics and Monitoring

### Repository Health Indicators

- AI/ folder usage frequency
- Self-review process adoption
- Prompt effectiveness ratings
- Developer satisfaction scores

### Success Metrics

- Reduced review cycle time
- Improved code quality scores
- Faster onboarding for new developers
- Higher team productivity ratings
