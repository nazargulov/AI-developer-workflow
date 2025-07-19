# Makefile for AI-Friendly Development

.PHONY: help setup test lint clean ai-review ai-setup docker-build docker-run

# Default target
help:
	@echo "AI-Friendly Development Makefile"
	@echo "================================="
	@echo ""
	@echo "Available targets:"
	@echo "  setup        - Set up development environment"
	@echo "  test         - Run all tests"
	@echo "  lint         - Run linting and code quality checks"
	@echo "  ai-review    - Perform AI-assisted code review"
	@echo "  ai-setup     - Set up AI development tools"
	@echo "  docker-build - Build Docker development image"
	@echo "  docker-run   - Run application in Docker"
	@echo "  clean        - Clean up generated files"
	@echo ""
	@echo "AI Workflow Commands:"
	@echo "  make ai-review   # Self-review using AI"
	@echo "  make test-watch  # Continuous testing during development"
	@echo "  make lint-fix    # Auto-fix linting issues"

# Development setup
setup: ai-setup
	@echo "Setting up development environment..."
	npm install || echo "No package.json found, skipping npm install"
	@echo "✅ Development environment ready"

# AI-specific setup
ai-setup:
	@echo "Setting up AI development tools..."
	@mkdir -p AI/code-review
	@touch AI/code-review/code-changes.txt
	@touch AI/code-review/AI_REVIEW.md
	@echo "✅ AI tools configured"

# Testing with AI assistance
test:
	@echo "Running tests..."
	@if [ -f "package.json" ]; then \
		npm test; \
	else \
		echo "No test framework detected. Add your test command here."; \
	fi
	@echo "✅ Tests completed"

# Continuous testing for development
test-watch:
	@echo "Starting continuous testing..."
	@if [ -f "package.json" ]; then \
		npm run test:watch || npm test -- --watch; \
	else \
		echo "Add your continuous testing command here"; \
	fi

# Linting and code quality
lint:
	@echo "Running linting checks..."
	@if [ -f "package.json" ]; then \
		npm run lint || npx eslint . || echo "No linter configured"; \
	else \
		echo "No linting configured. Consider adding ESLint or similar."; \
	fi
	@echo "✅ Linting completed"

# Auto-fix linting issues
lint-fix:
	@echo "Auto-fixing linting issues..."
	@if [ -f "package.json" ]; then \
		npm run lint:fix || npx eslint . --fix || echo "No auto-fix available"; \
	else \
		echo "No auto-fix configured."; \
	fi

# AI-assisted code review
ai-review:
	@echo "Performing AI-assisted code review..."
	@echo "Step 1: Generating git diff..."
	@git diff main -- '*.js' '*.html' '*.css' '*.md' '*.json' > AI/code-review/code-changes.txt || echo "No changes found"
	@echo "Step 2: Code review files prepared"
	@echo "Files ready for AI review:"
	@echo "  - AI/code-review/code-changes.txt (your changes)"
	@echo "  - AI/code-review/CODE_REVIEW_TEMPLATE.md (review template)"
	@echo "  - AI/docs/main_context.md (project context)"
	@echo "  - AI/rules/DEV_RULES.md (development rules)"
	@echo ""
	@echo "Next steps:"
	@echo "1. Load these files into your AI tool"
	@echo "2. Use prompt: 'Perform code review using the template and rules'"
	@echo "3. Save results to AI/code-review/AI_REVIEW.md"
	@echo "✅ AI review preparation completed"

# Pre-commit validation
pre-commit: lint test ai-review
	@echo "Pre-commit validation completed"

# Docker development
docker-build:
	@echo "Building Docker development image..."
	@docker build -t ai-workflow-example:dev -f Dockerfile .
	@echo "✅ Docker image built"

docker-run:
	@echo "Running application in Docker..."
	@docker run -p 3000:3000 -v $(PWD):/app ai-workflow-example:dev
	@echo "✅ Application running on http://localhost:3000"

# Development server
serve:
	@echo "Starting development server..."
	@if [ -f "package.json" ]; then \
		npm start || npm run dev || npx http-server .; \
	else \
		python3 -m http.server 3000 || python -m SimpleHTTPServer 3000; \
	fi

# Clean up generated files
clean:
	@echo "Cleaning up..."
	@rm -f AI/code-review/code-changes.txt
	@rm -f AI/code-review/AI_REVIEW.md
	@rm -rf node_modules/.cache
	@echo "✅ Cleanup completed"

# AI workflow helpers
workflow-explore:
	@echo "🔍 Starting Explore phase..."
	@echo "Load these context files:"
	@echo "  - AI/docs/main_context.md"
	@echo "  - AI/docs/[domain]_context.md (if applicable)"
	@echo "Use AI/prompts/PRE_CODE.md for guidance"

workflow-plan:
	@echo "📋 Starting Plan phase..."
	@echo "Break down your task into subtasks (20-30% AI automation)"
	@echo "Reference: AI/tasks/patterns/workflow_patterns.md"

workflow-code:
	@echo "💻 Starting Code phase..."
	@echo "Available commands:"
	@echo "  make test-watch  # Continuous testing"
	@echo "  make lint-fix    # Auto-fix issues"

workflow-review:
	@echo "✅ Starting Review phase..."
	@echo "Run: make ai-review"
	@echo "Then complete manual validation"

# Install AI development dependencies
install-ai-deps:
	@echo "Installing AI development dependencies..."
	@if [ -f "package.json" ]; then \
		npm install --save-dev eslint prettier husky lint-staged; \
	fi
	@echo "Consider adding: Cursor, GitHub Copilot, ChatGPT access"

# Generate AI usage report
ai-report:
	@echo "Generating AI usage report..."
	@echo "Recent AI-assisted commits:"
	@git log --oneline --grep="AI:" --since="1 month ago" || echo "No AI-tagged commits found"
	@echo ""
	@echo "Add 'AI:' prefix to commits that used AI assistance"
	@echo "Example: 'AI: Implement user authentication with JWT'"
