# AI Stack Engineering

**Transform your engineering workflow from linear to exponential through compounding AI automation.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Based on Every](https://img.shields.io/badge/Based%20on-Every--Marketplace-blue)](https://github.com/EveryInc/every-marketplace)
[![Company: Digitalis.io](https://img.shields.io/badge/Company-Digitalis.io-green)](https://digitalis.io)

A Claude Code plugin marketplace featuring specialized AI agents and workflows customized for modern distributed systems: **Go, Java/Spring Boot, React/TypeScript, Apache Cassandra, PostgreSQL, Apache Kafka, and OpenSearch**.

---

## 🌟 Overview

AI Stack Engineering brings the **Compounding Engineering Philosophy** to your development workflow. Each unit of work doesn't just complete a task—it teaches the system, making every subsequent task easier, faster, and higher quality.

This isn't just another AI coding assistant. It's a fundamental shift in how we build software:
- **Linear AI**: Helps with today's problem, starts fresh tomorrow
- **Compounding AI**: Learns from every interaction, applies patterns automatically, prevents entire categories of bugs

## 🎯 Why This Exists

At [Digitalis.io](https://digitalis.io), we work with complex distributed systems daily. While AI assistants help with individual tasks, we needed something that:
- **Learns** from our specific tech stack patterns
- **Prevents** the bugs we've seen in production
- **Scales** our engineering expertise across the team
- **Compounds** knowledge over time, not just solves today's problem

This project customizes the brilliant [compounding engineering framework](https://github.com/EveryInc/every-marketplace) by [Every, Inc.](https://every.to) for our specific technology stack.

## 🙏 Attribution

**This project is based on [every-marketplace](https://github.com/EveryInc/every-marketplace) by Every, Inc.**

We are deeply grateful to [Kieran Klaassen](https://github.com/kieranklaassen) and the team at [Every](https://every.to) for creating the Compounding Engineering Philosophy and the original plugin framework. Their innovative vision of AI-powered development workflows inspired us to create this specialized version.

Our contribution focuses on adapting their framework for distributed systems engineering with our specific tech stack while maintaining the core philosophy that makes it powerful.

## 🚀 Quick Start

### Installation

#### Method 1: Quick Install (Recommended)
```bash
# 1. Add marketplace directly from GitHub
claude /plugin marketplace add https://github.com/digitalis-io/ai-stack-engineering

# 2. Install the plugin
claude /plugin install ai-stack-engineering

# 3. (Recommended) Install Context7 for up-to-date docs
claude mcp add --transport sse context7 https://mcp.context7.com/sse
```

#### Method 2: Local Install (For Customization)
```bash
# 1. Clone the repository
git clone https://github.com/digitalis-io/ai-stack-engineering

# 2. Add marketplace from local path
claude /plugin marketplace add ./ai-stack-engineering

# 3. Install the plugin
claude /plugin install ai-stack-engineering

# 4. (Recommended) Install Context7 for up-to-date docs
claude mcp add --transport sse context7 https://mcp.context7.com/sse
```

### Verify Installation

```bash
/plugin list   # Should show ai-stack-engineering
/mcp list      # Should show Context7 (if installed)
/review        # Test the review command
```

### Your First Compounding Experience

```bash
# Plan a feature with AI research
claude /plan "Build Kafka consumer that writes to Cassandra"

# Execute the plan
claude /work

# Review with specialized agents
claude /review

# The magic: Next time you build something similar,
# the system already knows your patterns
```

## 🔄 The Compounding Engineering Workflow

### How Your Development Accelerates Over Time

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│  📊 TIME TO BUILD SIMILAR FEATURES                                 │
│                                                                     │
│  Week 1:   ████████████████████████████████████  4 hours          │
│  Week 2:   ████████████████████  2 hours                          │
│  Week 4:   ████████  1 hour                                       │
│  Month 2:  ██  20 minutes                                         │
│                                                                     │
│  🚀 10x FASTER with better quality                                │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘

     PLAN           DELEGATE         ASSESS          CODIFY
      🎯      ➜       📋       ➜      🔍       ➜      📝
   Research        AI Builds      Review Code    Save Learning
     ┃                ┃               ┃               ┃
     └────────────────┴───────────────┴───────────────┘
                           ⬇
                   Knowledge compounds
                   for next iteration
```

### The 4 Phases That Compound:

**1. 🎯 PLAN** - AI researches best practices for your exact stack
   - Searches Cassandra docs for partition strategies
   - Finds Go concurrency patterns that work
   - Learns Kafka delivery guarantees

**2. 📋 DELEGATE** - AI builds with accumulated knowledge
   - Applies your code style automatically
   - Uses patterns that worked before
   - Avoids mistakes from previous iterations

**3. 🔍 ASSESS** - 23 specialized agents review in parallel
   - `cassandra-guardian` prevents hot partitions
   - `kafka-guardian` ensures no data loss
   - `golang-reviewer` catches race conditions

**4. 📝 CODIFY** - Learnings become permanent rules
   - "Always use prepared statements with Cassandra"
   - "Never use unbuffered channels in Go"
   - "Always commit Kafka offsets after processing"

### What This Really Means:

**Week 1:** 4 hours to build a feature (learning your patterns)
**Week 2:** 2 hours for similar complexity (applying patterns)
**Month 2:** 40 minutes for the same work (full compound effect)

The system learns:
- ✅ Your code style and conventions
- ✅ Your common bugs and how to prevent them
- ✅ Your architecture patterns
- ✅ Your tech stack quirks (Cassandra partitions, Kafka offsets, Go concurrency)

**The Result**: Not just faster development, but exponentially better code quality.

## 🤖 Our Tech Stack Agents

### Specialized for Distributed Systems (6 Custom Agents)

#### `golang-reviewer`
*"I've debugged production at 3am. Make it obvious, make it work, make it fast—in that order."*
- Catches concurrency bugs, goroutine leaks, race conditions
- Enforces idiomatic Go patterns (Uber style guide)
- Production-ready error handling and observability

#### `java-craftsman`
*"I've seen AbstractSingletonProxyFactoryBean and lived. Keep it simple."*
- Prevents overengineering and enterprise anti-patterns
- Spring Boot configuration and best practices
- SOLID principles without the religion

#### `cassandra-guardian`
*"Ah, another hot partition in the making. Let me save you from 3am alerts."*
- Modern features: SAI indexes, vector search, UCS compaction
- Prevents unbounded partitions and tombstone disasters
- Data modeling that actually scales

#### `kafka-guardian`
*"At-least-once usually means at-least-twice. Let's fix that."*
- Ensures delivery guarantees actually work
- Prevents data loss during rebalancing
- Consumer group management that survives production

#### `react-reviewer`
*"Every unnecessary re-render is death by a thousand paper cuts."*
- Catches hook dependency issues before they bite
- Prevents infinite re-render loops
- TypeScript that actually helps

#### `search-sentinel`
*"Your fancy query DSL doesn't matter if users can't find anything."*
- OpenSearch/Elasticsearch relevance tuning
- Query performance at scale
- Index design that doesn't explode

### Core Engineering Agents (17 from Original)

A comprehensive suite of specialized agents for every aspect of software development:

- **Code Quality** - Simplicity, security, and performance optimization
- **Architecture** - System design and pattern recognition
- **Data Systems** - Database integrity and PostgreSQL optimization
- **Research** - Documentation and best practices discovery
- **Workflow** - PR resolution and knowledge capture
- **Language Experts** - Rails, Python, and TypeScript specialists

📖 **[See Complete Agent Guide](docs/AGENTS.md)** - Detailed documentation for all 23 agents with personalities, expertise, and use cases.

## 📚 Documentation

### Essential Guides
- 📖 **[Workflow Guide](docs/WORKFLOW_GUIDE.md)** - Comprehensive guide to compounding engineering
- 🚀 **[Quick Start](docs/QUICK_START.md)** - Get running in 5 minutes
- 📝 **[Article: The Philosophy](https://every.to/p/my-ai-is-already-fixed-the-code)** - Original concept by Every

### Commands Reference

| Command | Purpose | What It Does |
|---------|---------|--------------|
| `/plan` | Strategic planning | Researches best practices, creates implementation phases |
| `/work` | Execute tasks | Implements with learned patterns applied |
| `/review` | Multi-agent review | Parallel analysis by all specialized agents |
| `/triage` | Issue prioritization | Decides what to fix and in what order |
| `/resolve` | Parallel fixes | Resolves multiple issues simultaneously |
| `/context` | Memory management | Monitors token usage and suggests compaction |


## 💡 Philosophy: The Mindset Shift

### Traditional Engineering
```
Fix bug → Done
Write feature → Done
Review code → Done
```

### Compounding Engineering
```
Fix bug → Test added → Pattern recorded → Category prevented
Write feature → Pattern learned → Reused automatically
Review code → Standards extracted → Applied forever
```

**Every bug becomes impossible to repeat.**
**Every review makes future code better.**
**Every feature becomes a reusable pattern.**

## 🏢 About Digitalis.io

[Digitalis.io](https://digitalis.io) specializes in:
- **Cassandra Consulting**: From modeling to operations at scale
- **Kafka Architecture**: Event-driven systems that don't lose data
- **Distributed Systems**: Building systems that scale
- **Performance Engineering**: Optimizing for real-world workloads

We've taken these production learnings and encoded them into our AI agents.

## 🤝 Contributing

While this is a customized fork for our tech stack, we welcome:
- **Bug Reports**: Found an issue? [Open an issue](https://github.com/digitalis-io/ai-stack-engineering/issues)
- **Stack Adaptations**: Want to fork for your stack? We'll help!
- **Agent Improvements**: Better patterns for our tech? PR welcome!

For the original framework or different tech stacks, visit [every-marketplace](https://github.com/EveryInc/every-marketplace).

## 🔗 Related Projects

- **[Every Marketplace](https://github.com/EveryInc/every-marketplace)** - The original framework
- **[Apache Cassandra](https://cassandra.apache.org)** - The database that scales
- **[Apache Kafka](https://kafka.apache.org)** - Event streaming platform
- **[OpenSearch](https://opensearch.org)** - Search and analytics engine

## 📄 License

MIT License - See [LICENSE](LICENSE) file for details.

Based on every-marketplace by Every, Inc., used under MIT License.

---

<div align="center">

**Ready to compound your engineering?**

[⭐ Star this repo](https://github.com/digitalis-io/ai-stack-engineering) • [🐛 Report an issue](https://github.com/digitalis-io/ai-stack-engineering/issues) • [💬 Join the discussion](https://github.com/digitalis-io/ai-stack-engineering/discussions)

Built with ❤️ by [Digitalis.io](https://digitalis.io) • Inspired by [Every](https://every.to)

</div>