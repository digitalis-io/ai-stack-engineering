# AI Stack Engineering Plugin

Compounding engineering workflows for the **Digitalis.io tech stack**: Go, React/TypeScript, Apache Cassandra, PostgreSQL, Apache Kafka, and OpenSearch.

**Each unit of engineering work should make subsequent units of work easier—not harder.**

Based on [compounding-engineering](https://github.com/EveryInc/every-marketplace) by Every, Inc. - We're grateful to Kieran Klaassen and the Every team for creating the original framework.

## What's Inside

- **23 Specialized Agents** - Code reviewers, infrastructure guardians, and workflow automation
- **6 Slash Commands** - /review, /plan, /work, /triage, and more
- **Zero Hooks** - Lightweight and non-intrusive

## New Stack-Specific Agents

Our fork adds these agents for the Digitalis.io tech stack:

- **`golang-reviewer`** - Idiomatic Go review (Uber style guide, concurrency, interfaces)
- **`java-craftsman`** - Battle-tested Java/Spring Boot review, preventing overengineering disasters
- **`cassandra-guardian`** - Cassandra data modeling (modern compaction strategies), preventing hot partitions
- **`kafka-guardian`** - Event streaming reliability, preventing data loss
- **`react-reviewer`** - Modern React/TypeScript, fixing re-renders and hook issues
- **`search-sentinel`** - OpenSearch/Elasticsearch relevance and performance (works with both)

PostgreSQL optimization is covered by the existing `data-integrity-guardian` agent.

## All Agents

### Code Review (9 agents)
- `golang-reviewer` - Go code review with concurrency patterns and interface design
- `java-craftsman` - Java/Spring Boot review preventing AbstractFactoryFactory disasters
- `react-reviewer` - React/TypeScript review catching re-renders and hook issues
- `dhh-rails-reviewer` - Rails review in DHH's style
- `kieran-rails-reviewer` - Rails review emphasizing maintainability
- `kieran-typescript-reviewer` - TypeScript review for type safety
- `kieran-python-reviewer` - Python review for pythonic patterns
- `code-simplicity-reviewer` - Simplicity review with quality metrics
- `security-sentinel` - Security vulnerability detection

### Infrastructure (5 agents)
- `cassandra-guardian` - Cassandra data modeling and partition design
- `kafka-guardian` - Kafka/event streaming reliability
- `search-sentinel` - OpenSearch/Elasticsearch optimization
- `data-integrity-guardian` - PostgreSQL and database integrity
- `performance-oracle` - Performance analysis and optimization

### Architecture (2 agents)
- `architecture-strategist` - High-level architecture and design
- `pattern-recognition-specialist` - Code pattern detection

### Research (4 agents)
- `repo-research-analyst` - Codebase structure analysis
- `git-history-analyzer` - Git history and hotspot detection
- `framework-docs-researcher` - Framework documentation research
- `best-practices-researcher` - Industry best practices research

### Workflow (3 agents)
- `pr-comment-resolver` - PR feedback resolution
- `feedback-codifier` - Knowledge capture and documentation
- `every-style-editor` - Every writing style editing

## Commands

- `/review` - Comprehensive code review using multiple specialized agents
- `/plan` - Creates a structured plan for implementing changes
- `/work` - Executes planned tasks systematically
- `/triage` - Analyzes and prioritizes issues or tasks
- `/resolve-todo-parallel` - Resolves todos in parallel using multiple agents
- `/generate-command` - Generates new custom commands for your workflow

## Installation

### Method 1: Quick Install from GitHub (Recommended)

```bash
# Add marketplace directly from GitHub
claude /plugin marketplace add https://github.com/digitalis-io/ai-stack-engineering

# Install the plugin
claude /plugin install ai-stack-engineering
```

### Method 2: Local Install (For Customization)

```bash
# Clone the repository
git clone https://github.com/digitalis-io/ai-stack-engineering
cd ai-stack-engineering

# Add marketplace from local path
claude /plugin marketplace add ./ai-stack-engineering

# Install the plugin
claude /plugin install ai-stack-engineering
```

## Usage Examples

### Stack-Specific Reviews

```bash
# Go code review
claude agent golang-reviewer "review my Go service for concurrency issues"

# Java/Spring Boot review
claude agent java-craftsman "review this Spring Boot service for overengineering"

# Cassandra schema review
claude agent cassandra-guardian "review this table schema for hot partitions"

# Kafka consumer review
claude agent kafka-guardian "check my consumer offset management"

# React component review
claude agent react-reviewer "review this component for re-render issues"

# Search query optimization
claude agent search-sentinel "optimize this OpenSearch query"
```

### Workflow Commands

```bash
# Comprehensive review of current changes
claude /review

# Plan a feature implementation
claude /plan "add user authentication with JWT"

# Execute planned tasks
claude /work

# Triage issues
claude /triage "analyze these GitHub issues"
```

## Philosophy: Compounding Engineering

This plugin embodies the compounding engineering philosophy:

1. **Plan** → Understand the change needed and its impact
2. **Delegate** → Use AI tools to help with implementation
3. **Assess** → Verify changes work as expected
4. **Codify** → Update documentation with learnings

Each agent and command is designed to make your next unit of work easier, not harder.

## Tech Stack Coverage

- **Go** - Idiomatic patterns, concurrency, interfaces (golang-reviewer)
- **React/TypeScript** - Hooks, re-renders, component architecture (react-reviewer)
- **Cassandra** - Data modeling, partition design, UCS compaction (cassandra-guardian)
- **PostgreSQL** - Data integrity, consistency (data-integrity-guardian)
- **Kafka** - Event streaming, offset management (kafka-guardian)
- **OpenSearch/Elasticsearch** - Search relevance, performance (search-sentinel)

## Contributing

This plugin is maintained by Digitalis.io for our internal tech stack. If you'd like to customize it for your stack, fork and modify the agents in the `agents/` directory.

## License

MIT - See LICENSE file for details.

Based on compounding-engineering by Every, Inc.

## Links

- [GitHub Repository](https://github.com/digitalis-io/ai-stack-engineering)
- [Claude Code Documentation](https://docs.claude.com/en/docs/claude-code)
- [Original compounding-engineering](https://github.com/EveryInc/every-marketplace)
