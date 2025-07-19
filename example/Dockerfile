# AI-Friendly Development Dockerfile

FROM node:18-alpine

# Set working directory
WORKDIR /app

# Install system dependencies for AI development
RUN apk add --no-cache \
    git \
    curl \
    make \
    python3 \
    py3-pip

# Create AI directory structure
RUN mkdir -p AI/{docs,code-review,prompts,rules,tasks,presentation}

# Copy package files first for better caching
COPY package*.json ./

# Install dependencies
RUN npm install

# Install AI development tools
RUN npm install -g \
    eslint \
    prettier \
    http-server

# Copy application code
COPY . .

# Set up AI development environment
RUN chmod +x AI/code-review/HOW_TO_USE.md || true
RUN touch AI/code-review/code-changes.txt
RUN touch AI/code-review/AI_REVIEW.md

# Create development user
RUN addgroup -g 1001 -S nodejs
RUN adduser -S developer -u 1001 -G nodejs

# Set permissions
RUN chown -R developer:nodejs /app
USER developer

# Expose port
EXPOSE 3000

# Health check
HEALTHCHECK --interval=30s --timeout=3s --start-period=5s --retries=3 \
    CMD curl -f http://localhost:3000/ || exit 1

# Default command for development
CMD ["npm", "start"]

# Development mode with hot reload
# Alternative: CMD ["npm", "run", "dev"]

# AI development helper labels
LABEL ai.workflow.patterns="explore-plan-code-review,prototype-rewrite-improve,build-integrate-delegate-iterate"
LABEL ai.tools.supported="cursor,chatgpt,copilot,diff-critic"
LABEL ai.context.optimized="true"
LABEL maintainer="AI Development Team"
