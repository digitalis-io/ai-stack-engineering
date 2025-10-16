# AI Stack Engineering - Quick Start Guide

> 🚀 **Go from zero to 10x productivity in 30 minutes**

## The Compounding Principle

Each unit of engineering work makes the next one easier. Your code reviews teach the system. Your bug fixes become permanent prevention. Your architecture decisions compound into patterns. **Today's 30-minute investment saves hours tomorrow.**

## Prerequisites

- Claude Code CLI installed (`claude --version`)
- Git repository with your project
- 30 minutes for your first feature
- (Next time: 15 minutes for the same complexity)

## Installation

### Step 1: Install the Plugin

#### Option A: Quick Install (Recommended)
```bash
# Add marketplace directly from GitHub
claude /plugin marketplace add https://github.com/digitalis-io/ai-stack-engineering

# Install the plugin
claude /plugin install ai-stack-engineering
```

#### Option B: Local Install (For Customization)
```bash
# Clone the plugin repository
git clone https://github.com/digitalis-io/ai-stack-engineering

# Add marketplace from local path
claude /plugin marketplace add ./ai-stack-engineering

# Install the plugin
claude /plugin install ai-stack-engineering
```

### Step 2: Install Context7 MCP (Recommended)

For up-to-date documentation:

```bash
claude mcp add --transport sse context7 https://mcp.context7.com/sse
```

### Step 3: Verify Installation

```bash
/plugin list  # Check plugin installed
/mcp list    # Check Context7 available
```

💡 **Why Context7?** Fetches current docs for our tech stack, ensuring accurate, version-specific code.

## The 4 Phases

⚠️ **Terminology Clarification:** The `/plan` command creates LOCAL markdown files on your filesystem for documentation and context, NOT actual GitHub issues on github.com. The system does integrate with GitHub to learn from your repository history and can push code, but planning documents are local workflow files.

### 🎯 **PLAN** - Research and architect (teaches patterns)
- Use `/plan "your feature request"`
- Agents research best practices for your stack
- Creates local planning document (markdown file with phases)
- Learns your architecture preferences
- Note: Creates a LOCAL file, not a GitHub web issue

### 📋 **DELEGATE** - Execute systematically (applies patterns)
- Use `/work` to implement phases
- To-dos persist across sessions
- Each phase reviewed before next
- System applies learned patterns

### 🔍 **REVIEW** - Multi-agent assessment (catches issues)
- Use `/review` for parallel analysis
- Specialized agents for Go, Cassandra, Kafka, React, PostgreSQL, OpenSearch
- Issues prioritized by severity
- Every review improves future code

### 🔄 **CODIFY** - Record learnings (compounds knowledge)
- Use `/resolve` for parallel fixes
- Updates CLAUDE.md with patterns
- Prevents entire bug categories
- Makes next feature faster

## 5 Essential Commands

| Command | Purpose | When to Use |
|---------|---------|-------------|
| `/plan` | Research and architect | Starting any new feature |
| `/work` | Execute implementation | Building planned features |
| `/review` | Multi-agent code review | Before committing code |
| `/triage` | Prioritize found issues | After review finds problems |
| `/resolve` | Fix issues in parallel | Implementing review feedback |

## Simple Example: Go + Cassandra Service (30 min → 15 min)

### First Time (30 minutes)

```bash
# 1. Plan your service (5 min)
claude /plan "Create Go service that reads from Kafka and writes to Cassandra"

# 2. Implement Phase 1 (10 min)
claude /work
# → Sets up connections, health checks, logging

# 3. Implement Phase 2 (10 min)
claude /work
# → Adds business logic, error handling

# 4. Review and fix (5 min)
claude /review
claude /resolve
# → Fixes hot partitions, adds worker pool
```

### Second Time (15 minutes)

```bash
# System already knows:
# ✓ Your Cassandra partitioning strategy
# ✓ Your Kafka consumer patterns
# ✓ Your error handling style
# ✓ Your testing approach

claude /plan "Create order processing service"
# → Applies ALL learned patterns automatically
```

## The Compounding Mindset

❌ **Linear thinking**: "Fix this bug"
✅ **Compound thinking**: "Make this category of bugs impossible"

❌ **Linear thinking**: "Write this feature"
✅ **Compound thinking**: "Create a pattern for all similar features"

❌ **Linear thinking**: "Review this code"
✅ **Compound thinking**: "Teach the system my review standards"

## What To Do If Stuck

### Context overflow?
```bash
claude /context  # Check buffer usage
# Complete current phase, then compact
```

### Review taking too long?
```bash
claude /review --path specific/directory
```

### Not sure what patterns to codify?
```bash
claude agent feedback-codifier "extract patterns from recent work"
```

### Need help?
- Full guide: [WORKFLOW_GUIDE.md](./WORKFLOW_GUIDE.md)
- Report issues: https://github.com/digitalis-io/ai-stack-engineering/issues (actual GitHub repository)

## Start Today Checklist

**Right now (5 min):**
- [ ] Run the 3 installation commands
- [ ] Verify with `claude /review` (should show available)

**Your first feature (25 min):**
- [ ] Pick something small but real
- [ ] Run `/plan "your feature"`
- [ ] Execute with `/work`
- [ ] Review with `/review`
- [ ] Fix with `/resolve`

**Make it compound:**
- [ ] Add one learning to CLAUDE.md
- [ ] Notice tomorrow: the second feature is faster
- [ ] Week 1: See 2x productivity
- [ ] Month 1: Achieve 10x productivity

## The 10x Difference

```
Day 1:  Learn workflow      → 30 min feature
Day 2:  Patterns apply      → 20 min feature
Week 1: System knows you    → 15 min feature
Week 2: Preventing bugs     → 10 min feature
Month:  Full compounding    → 5 min feature

Same complexity. 6x faster. 10x fewer bugs.
```

## Remember

🔄 **Every bug you fix teaches the system**
🔄 **Every review makes future code better**
🔄 **Every feature becomes a reusable pattern**
🔄 **Every day compounds into the next**

---

**Ready?** Install now. Build something. Watch it compound.

Quick install (one-liner):
```bash
claude /plugin marketplace add https://github.com/digitalis-io/ai-stack-engineering && \
claude /plugin install ai-stack-engineering && \
echo "🚀 Ready to compound your engineering!"
```

Or with local customization:
```bash
git clone https://github.com/digitalis-io/ai-stack-engineering && \
claude /plugin marketplace add ./ai-stack-engineering && \
claude /plugin install ai-stack-engineering && \
echo "🚀 Ready to compound your engineering!"
```

*Based on [Every's compounding engineering](https://github.com/EveryInc/every-marketplace) framework. Customized for Digitalis.io's stack: Go, React, Cassandra, PostgreSQL, Kafka, OpenSearch.*