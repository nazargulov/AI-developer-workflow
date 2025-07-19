# Code Examples for AI Developer Workflow Presentation

## Example 1: AI/docs Context Structure

```markdown
# AI/docs/main_context.md - Primary AI Context File

## Project Overview

- **Name:** E-commerce Platform
- **Domain:** Online retail platform
- **Architecture:** Microservices with shared database

## Key Business Logic

- **Payment Processing:** Secure transaction handling
- **Order Management:** Real-time order state management
- **User Management:** Authentication, profiles, preferences
- **Inventory System:** Stock tracking and management

## Development Patterns

- **Service Objects:** Business logic encapsulation
- **Interactors:** Complex workflow coordination
- **Decorators:** Presentation logic separation
- **Policies:** Authorization and access control

## AI-Relevant Information

- **Critical Paths:** Payment flows, order processing, user authentication
- **Security Requirements:** Data protection, audit trails, fraud prevention
- **Performance Needs:** Fast response times, high availability
- **Compliance:** Data protection regulations, security standards
```

```markdown
# AI/docs/payment_context.md - Domain-Specific Context

## Payment Processing Context

- **Providers:** Multiple payment gateways and processors
- **Currencies:** Multiple supported currencies with conversion
- **Methods:** Cards, digital wallets, bank transfers
- **Compliance:** Payment industry standards, security regulations

## Key Models and Services

- Transaction, PaymentMethod, PaymentProvider
- PaymentProcessingService, SecurityService
- CurrencyConversionService, ValidationService

## Critical Business Rules

- Transaction limits and validations
- Security checks and fraud prevention
- Currency conversion and fee calculations
- Regulatory compliance requirements
```

## Example 2: Enhanced Pre-Coding Prompt with AI/docs

```markdown
# Context Loading Prompt

## Primary Context

Load and analyze: AI/docs/main_context.md

## Specific Context (if applicable)

Additional context: AI/docs/payment_context.md

## Task Analysis Request

Ticket: #{ticket_id}
Description: #{ticket_description}

Based on the loaded context:

1. Identify affected domain areas
2. List relevant models and services
3. Break down into implementable subtasks
4. Flag compliance/security considerations
5. Suggest testing strategy

## Expected Output

- [ ] Domain analysis complete
- [ ] Affected components identified
- [ ] Implementation plan created
- [ ] Risk assessment done
```

## Example 3: Development Cycle Automation

```bash
#!/bin/bash
# AI-assisted development loop

echo "Starting AI-assisted development cycle..."

while true; do
    echo "1. Code implementation phase"
    # AI assists with code writing

    echo "2. Running tests..."
    make test
    if [ $? -ne 0 ]; then
        echo "Tests failed. AI analyzing failures..."
        # AI helps debug test failures
        continue
    fi

    echo "3. Running linter..."
    make lint
    if [ $? -ne 0 ]; then
        echo "Lint issues found. AI suggesting fixes..."
        # AI helps fix linting issues
        continue
    fi

    echo "4. Self-review with AI..."
    git diff dev -- '*.rb' '*.rake' > AI/code-review/code-changes.txt
    # AI performs code review using template

    echo "Cycle complete. Ready for human review."
    break
done
```

## Example 4: AI Code Review Template Usage

```markdown
# Self-Review Checklist (AI-Assisted)

## Before Submitting MR:

- [ ] Every line reviewed thoughtfully
- [ ] AI-generated portions documented
- [ ] No unnecessary dependencies added
- [ ] Tests cover new functionality
- [ ] Documentation updated if needed

## AI Review Questions:

1. Does this code follow project patterns?
2. Are there any potential security issues?
3. Is error handling adequate?
4. Can this be simplified?
5. Are there built-in alternatives to new dependencies?
```

## Example 5: Quality Control Script

```ruby
# AI-assisted quality control
class AIQualityChecker
  def self.check_mr_quality(diff_file)
    issues = []

    # Check for AI-generated code documentation
    unless documented_ai_usage?(diff_file)
      issues << "Missing AI usage documentation"
    end

    # Check for heavy dependencies
    if heavy_dependencies_added?(diff_file)
      issues << "Consider built-in alternatives"
    end

    # Check for proper error handling
    unless adequate_error_handling?(diff_file)
      issues << "Improve error handling"
    end

    issues
  end

  private

  def self.documented_ai_usage?(diff_file)
    # Logic to check if AI usage is documented
  end

  def self.heavy_dependencies_added?(diff_file)
    # Logic to detect heavy library additions
  end

  def self.adequate_error_handling?(diff_file)
    # Logic to check error handling patterns
  end
end
```

## Example 6: Metrics Collection

```yaml
# AI impact metrics configuration
ai_metrics:
  development_time:
    baseline_hours: 8
    ai_assisted_hours: 5.2
    improvement_percentage: 35%

  code_quality:
    pre_ai_bug_rate: 0.12
    post_ai_bug_rate: 0.08
    improvement: 33%

  developer_satisfaction:
    productivity_increase: 85%
    confidence_increase: 78%
    continuation_desire: 92%
```
