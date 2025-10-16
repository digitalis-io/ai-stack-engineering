# AI Stack Engineering - Complete Agent Guide

This guide provides detailed documentation for all 24 specialized AI agents in the AI Stack Engineering plugin. Each agent has unique expertise and personality, designed to catch specific issues and improve your code quality.

## Table of Contents

- [Stack-Specific Agents (7 Custom)](#stack-specific-agents-7-custom)
  - [golang-reviewer](#golang-reviewer)
  - [java-craftsman](#java-craftsman)
  - [cassandra-guardian](#cassandra-guardian)
  - [kafka-guardian](#kafka-guardian)
  - [react-reviewer](#react-reviewer)
  - [search-sentinel](#search-sentinel)
  - [cpp-systems-specialist](#cpp-systems-specialist)
- [Code Quality Agents (5)](#code-quality-agents-5)
  - [code-simplicity-reviewer](#code-simplicity-reviewer)
  - [security-sentinel](#security-sentinel)
  - [performance-oracle](#performance-oracle)
  - [data-integrity-guardian](#data-integrity-guardian)
  - [kieran-typescript-reviewer](#kieran-typescript-reviewer)
- [Architecture & Design Agents (2)](#architecture--design-agents-2)
  - [architecture-strategist](#architecture-strategist)
  - [pattern-recognition-specialist](#pattern-recognition-specialist)
- [Rails Specialists (2)](#rails-specialists-2)
  - [dhh-rails-reviewer](#dhh-rails-reviewer)
  - [kieran-rails-reviewer](#kieran-rails-reviewer)
- [Python Specialist (1)](#python-specialist-1)
  - [kieran-python-reviewer](#kieran-python-reviewer)
- [Research & Analysis Agents (4)](#research--analysis-agents-4)
  - [framework-docs-researcher](#framework-docs-researcher)
  - [best-practices-researcher](#best-practices-researcher)
  - [repo-research-analyst](#repo-research-analyst)
  - [git-history-analyzer](#git-history-analyzer)
- [Workflow Agents (3)](#workflow-agents-3)
  - [pr-comment-resolver](#pr-comment-resolver)
  - [feedback-codifier](#feedback-codifier)
  - [every-style-editor](#every-style-editor)

---

## Stack-Specific Agents (7 Custom)

These agents were specifically created for the Digitalis.io tech stack, each with deep expertise in their domain.

### golang-reviewer

**Personality**: *"I've debugged production at 3am. Make it obvious, make it work, make it fast—in that order."*

**Expertise**:
- Idiomatic Go following Uber Style Guide
- Concurrency patterns and race condition detection
- Goroutine leak prevention
- Interface design and error handling
- Context propagation and cancellation
- Testing with table-driven tests

**Catches**:
- Race conditions before they hit production
- Goroutine leaks that cause memory issues
- Improper error handling (`_ = someFunc()`)
- Channel misuse and deadlocks
- Missing `defer` for cleanup
- Inefficient slice operations

**When to Use**:
- Reviewing any Go code
- Debugging performance issues
- Implementing concurrent systems
- API and library design

---

### java-craftsman

**Personality**: *"I've seen AbstractSingletonProxyFactoryBean and lived. Keep it simple."*

**Expertise**:
- Java/Spring Boot best practices
- Preventing overengineering and enterprise anti-patterns
- SOLID principles without the dogma
- Spring configuration and dependency injection
- JPA/Hibernate optimization
- Microservices patterns

**Catches**:
- AbstractFactoryFactory disasters
- Unnecessary abstraction layers
- N+1 query problems
- Spring Boot configuration issues
- Memory leaks in long-running processes
- Thread safety issues

**When to Use**:
- Spring Boot service reviews
- Refactoring overengineered code
- JPA/Hibernate optimization
- Microservice architecture decisions

---

### cassandra-guardian

**Personality**: *"Ah, another hot partition in the making. Let me save you from 3am alerts."*

**Expertise**:
- Modern Cassandra features (SAI, vector search, UCS compaction)
- Partition key design and data modeling
- Time-series data patterns
- Denormalization strategies
- Query optimization
- Tombstone management

**Catches**:
- Unbounded partition growth
- Hot partition patterns
- Inefficient queries requiring ALLOW FILTERING
- Missing time bucketing
- Tombstone accumulation
- Poor compaction strategy choices

**When to Use**:
- Designing new Cassandra schemas
- Debugging performance issues
- Planning data migrations
- Implementing time-series storage

---

### kafka-guardian

**Personality**: *"At-least-once usually means at-least-twice. Let's fix that."*

**Expertise**:
- Producer/consumer patterns
- Delivery guarantees (exactly-once, at-least-once)
- Offset management and commits
- Consumer group rebalancing
- Event schema evolution
- Stream processing patterns

**Catches**:
- Data loss during rebalancing
- Duplicate message processing
- Offset commit issues
- Consumer lag problems
- Poison message handling
- Schema compatibility breaks

**When to Use**:
- Building event-driven systems
- Implementing event sourcing
- Debugging message loss
- Optimizing consumer performance

---

### react-reviewer

**Personality**: *"Every unnecessary re-render is death by a thousand paper cuts."*

**Expertise**:
- Modern React with hooks
- TypeScript integration
- Performance optimization (memo, useMemo, useCallback)
- Component architecture
- State management patterns
- Server Components and RSC

**Catches**:
- Unnecessary re-renders
- Hook dependency issues
- Infinite render loops
- Memory leaks from event listeners
- Incorrect key prop usage
- State update batching issues

**When to Use**:
- React component reviews
- Performance optimization
- Hook implementation
- TypeScript integration

---

### search-sentinel

**Personality**: *"Your fancy query DSL doesn't matter if users can't find anything."*

**Expertise**:
- OpenSearch/Elasticsearch query optimization
- Index design and mappings
- Relevance tuning
- Aggregation performance
- Cluster scaling strategies
- Both OpenSearch and Elasticsearch compatibility

**Catches**:
- Inefficient queries that don't scale
- Poor index design causing slow searches
- Missing analyzers affecting relevance
- Expensive aggregations
- Mapping explosions
- Circuit breaker triggers

**When to Use**:
- Designing search functionality
- Optimizing query performance
- Tuning search relevance
- Planning index strategies

---

### cpp-systems-specialist

**Personality**: *"Make it correct, make it safe, then make it fast. In that order."*

**Expertise**:
- Modern C++ best practices (C++17/20/23)
- Memory safety and RAII patterns
- Thread safety and concurrency
- Undefined behavior prevention
- Template metaprogramming
- Cassandra C++ driver development
- Systems programming and performance

**Catches**:
- Memory leaks and use-after-free
- Race conditions and deadlocks
- Undefined behavior traps
- Buffer overflows and bounds violations
- Resource leaks (file handles, sockets)
- ABI compatibility issues
- Compilation time explosions from templates

**When to Use**:
- C/C++ code reviews
- Cassandra driver development
- Systems programming
- Performance-critical code
- Multi-threaded applications
- Memory-sensitive components

---

## Code Quality Agents (5)

These agents focus on general code quality, security, and maintainability across all languages.

### code-simplicity-reviewer

**Personality**: *"The best code is no code. The second best is simple code."*

**Expertise**:
- YAGNI (You Aren't Gonna Need It) principle
- Measurable complexity metrics
- Cyclomatic complexity analysis
- SOLID principle violations
- Code duplication detection
- Refactoring opportunities

**Catches**:
- Premature optimization
- Unnecessary abstractions
- Complex boolean logic
- Deep nesting (arrow anti-pattern)
- God classes and methods
- Feature envy

**When to Use**:
- Simplifying complex code
- Refactoring legacy systems
- Code review for maintainability
- Technical debt assessment

---

### security-sentinel

**Personality**: *"Think like an attacker, code like a defender."*

**Expertise**:
- OWASP Top 10 vulnerabilities
- Input validation and sanitization
- Authentication/authorization patterns
- Secrets management
- SQL injection prevention
- XSS and CSRF protection

**Catches**:
- Hardcoded credentials
- SQL injection vulnerabilities
- Missing input validation
- Insecure deserialization
- Weak cryptography
- Path traversal risks

**When to Use**:
- Security audits
- Pre-deployment reviews
- API endpoint security
- Authentication implementation

---

### performance-oracle

**Personality**: *"I've seen systems die from a thousand paper cuts."*

**Expertise**:
- Algorithmic complexity analysis
- Database query optimization
- Memory usage patterns
- Caching strategies
- Async/parallel processing
- Load testing insights

**Catches**:
- O(n²) algorithms hiding in loops
- N+1 query problems
- Memory leaks
- Inefficient data structures
- Missing indexes
- Synchronous operations that should be async

**When to Use**:
- Performance troubleshooting
- Scalability planning
- Database optimization
- Algorithm selection

---

### data-integrity-guardian

**Personality**: *"Data corruption is forever. Let's prevent it."*

**Expertise**:
- PostgreSQL optimization and best practices
- Database migrations safety
- Transaction boundaries
- ACID compliance
- Referential integrity
- Data privacy (GDPR, CCPA)

**Catches**:
- Unsafe migrations that lock tables
- Missing foreign key constraints
- Race conditions in data updates
- Transaction isolation issues
- Data loss scenarios
- Privacy regulation violations

**When to Use**:
- Database schema design
- Writing migrations
- Transaction management
- Data privacy compliance

---

### kieran-typescript-reviewer

**Personality**: *"TypeScript isn't just JavaScript with types—it's a better way to think."*

**Expertise**:
- Advanced TypeScript patterns
- Type safety and inference
- Generics and utility types
- Strict mode compliance
- Module systems
- Build configuration

**Catches**:
- Type assertions hiding bugs
- Any types defeating purpose
- Missing strict checks
- Incorrect generic constraints
- Module resolution issues
- Build configuration problems

**When to Use**:
- TypeScript code reviews
- Type system design
- Library API design
- Migration from JavaScript

---

## Architecture & Design Agents (2)

These agents focus on high-level system design and architectural patterns.

### architecture-strategist

**Personality**: *"Good architecture is invisible until you need to change something."*

**Expertise**:
- System design patterns
- Microservices vs monoliths
- API design and versioning
- Service boundaries
- Dependency management
- Architectural decision records (ADRs)

**Catches**:
- Inappropriate service boundaries
- Circular dependencies
- Missing abstraction layers
- Tight coupling
- Violation of architectural principles
- Technical debt accumulation

**When to Use**:
- System design reviews
- Service decomposition
- API design decisions
- Architecture documentation

---

### pattern-recognition-specialist

**Personality**: *"I see patterns others miss, and anti-patterns others accept."*

**Expertise**:
- Design pattern identification
- Anti-pattern detection
- Code smell recognition
- Refactoring opportunities
- Pattern consistency across codebase
- Emerging patterns in code evolution

**Catches**:
- Singleton abuse
- Anemic domain models
- Primitive obsession
- Inappropriate intimacy
- Shotgun surgery patterns
- Copy-paste programming

**When to Use**:
- Codebase analysis
- Refactoring planning
- Pattern standardization
- Code review

---

## Rails Specialists (2)

Specialized agents for Ruby on Rails applications with different philosophical approaches.

### dhh-rails-reviewer

**Personality**: *"Complexity is a bug. The Rails Way exists for a reason."*

**Expertise**:
- Rails conventions and idioms
- The Rails Way philosophy
- Majestic monolith patterns
- Hotwire and Turbo
- Action Cable patterns
- Rails performance tricks

**Catches**:
- Fighting Rails conventions
- Unnecessary service objects
- Overuse of gems
- Complex abstractions
- Non-RESTful routes
- Database performance issues

**When to Use**:
- Rails application reviews
- Simplifying complex Rails code
- Performance optimization
- Hotwire implementations

---

### kieran-rails-reviewer

**Personality**: *"Rails gives you power. Use it wisely."*

**Expertise**:
- Rails best practices
- Testing strategies
- Background job patterns
- API design in Rails
- Rails security
- Upgrade strategies

**Catches**:
- Missing database indexes
- N+1 queries
- Unsafe parameters
- Missing validations
- Poor test coverage
- Security vulnerabilities

**When to Use**:
- Rails code reviews
- API development
- Testing strategy
- Security audits

---

## Python Specialist (1)

### kieran-python-reviewer

**Personality**: *"Python is about readability. If it's not readable, it's not Pythonic."*

**Expertise**:
- Pythonic code patterns
- PEP 8 compliance
- Type hints and mypy
- Async/await patterns
- Package structure
- Testing with pytest

**Catches**:
- Non-Pythonic code
- Missing type hints
- Mutable default arguments
- Global state abuse
- Poor exception handling
- Inefficient list comprehensions

**When to Use**:
- Python code reviews
- API design
- Package structure
- Async implementation

---

## Research & Analysis Agents (4)

These agents help you understand codebases, research best practices, and analyze patterns.

### framework-docs-researcher

**Personality**: *"The documentation has the answer. Let me find it."*

**Expertise**:
- Finding relevant documentation
- API reference lookup
- Version-specific features
- Migration guides
- Best practices from official sources
- Community resources

**What it Does**:
- Searches official documentation
- Finds code examples
- Identifies version differences
- Locates migration paths
- Discovers configuration options
- Links to authoritative sources

**When to Use**:
- Learning new frameworks
- Resolving version issues
- Finding official examples
- Planning migrations

---

### best-practices-researcher

**Personality**: *"Standing on the shoulders of giants is smart, not lazy."*

**Expertise**:
- Industry best practices
- Community standards
- Style guides
- Design patterns
- Architecture patterns
- Testing strategies

**What it Does**:
- Researches industry standards
- Finds successful patterns
- Compares approaches
- Identifies anti-patterns
- Gathers community consensus
- Provides implementation examples

**When to Use**:
- Establishing standards
- Choosing between approaches
- Setting up new projects
- Creating style guides

---

### repo-research-analyst

**Personality**: *"Understanding the codebase is half the battle."*

**Expertise**:
- Repository structure analysis
- Code organization patterns
- Documentation discovery
- Convention identification
- Dependency mapping
- Architecture inference

**What it Does**:
- Maps repository structure
- Identifies coding patterns
- Finds documentation
- Discovers conventions
- Analyzes dependencies
- Infers architecture

**When to Use**:
- Onboarding to new codebases
- Understanding project structure
- Finding patterns to follow
- Architecture discovery

---

### git-history-analyzer

**Personality**: *"The commit history tells the real story."*

**Expertise**:
- Git history analysis
- Code evolution patterns
- Hotspot identification
- Author expertise mapping
- Bug introduction detection
- Refactoring history

**What it Does**:
- Analyzes commit patterns
- Identifies frequently changed files
- Maps developer expertise
- Finds bug-prone areas
- Tracks technical debt
- Discovers refactoring patterns

**When to Use**:
- Understanding code evolution
- Finding unstable areas
- Identifying experts
- Planning refactoring

---

## Workflow Agents (3)

These agents help with development workflow, documentation, and process automation.

### pr-comment-resolver

**Personality**: *"Every comment deserves a thoughtful resolution."*

**Expertise**:
- PR comment interpretation
- Code change implementation
- Comment prioritization
- Conflict resolution
- Clear communication
- Batch change management

**What it Does**:
- Analyzes PR comments
- Implements requested changes
- Provides clear summaries
- Handles multiple comments
- Resolves conflicts
- Updates documentation

**When to Use**:
- Addressing PR feedback
- Implementing reviewer suggestions
- Batch fixing issues
- Resolving code review comments

---

### feedback-codifier

**Personality**: *"Today's feedback is tomorrow's automation."*

**Expertise**:
- Pattern extraction from feedback
- Rule creation
- Documentation updates
- Knowledge persistence
- Learning extraction
- Process improvement

**What it Does**:
- Captures learnings from reviews
- Creates reusable rules
- Updates CLAUDE.md
- Documents patterns
- Codifies best practices
- Builds institutional knowledge

**When to Use**:
- After code reviews
- Post-incident analysis
- Capturing learnings
- Updating standards

---

### every-style-editor

**Personality**: *"Clear writing is clear thinking."*

**Expertise**:
- Every's house style guide
- Technical writing clarity
- Documentation structure
- Tone consistency
- Grammar and punctuation
- Readability optimization

**What it Does**:
- Edits for clarity
- Improves readability
- Ensures consistency
- Fixes grammar
- Optimizes structure
- Maintains voice

**When to Use**:
- Documentation writing
- README creation
- Blog post editing
- Comment clarity

---

## Using Agents Effectively

### Direct Agent Invocation

```bash
# Call a specific agent
claude agent golang-reviewer "review my concurrent code"
claude agent cassandra-guardian "check this schema design"
```

### Multiple Agents in Review

The `/review` command automatically selects relevant agents based on your code:

```bash
claude /review
# Detects Go code → runs golang-reviewer
# Finds Cassandra queries → runs cassandra-guardian
# Sees Kafka usage → runs kafka-guardian
# Plus universal agents for architecture, security, performance
```

### Agent Combinations

Some agents work particularly well together:

**For Go Services**:
- `golang-reviewer` + `security-sentinel` + `performance-oracle`

**For Java Services**:
- `java-craftsman` + `security-sentinel` + `performance-oracle`

**For C/C++ Systems**:
- `cpp-systems-specialist` + `security-sentinel` + `performance-oracle`
- For Cassandra drivers: `cpp-systems-specialist` + `cassandra-guardian`

**For Data Systems**:
- `cassandra-guardian` + `kafka-guardian` + `data-integrity-guardian`

**For Frontend**:
- `react-reviewer` + `kieran-typescript-reviewer` + `performance-oracle`

**For Architecture**:
- `architecture-strategist` + `pattern-recognition-specialist` + `git-history-analyzer`

### Tips for Best Results

1. **Be Specific**: Give agents specific context about what you're concerned about
2. **Use Multiple Agents**: Different perspectives catch different issues
3. **Learn from Feedback**: Use `feedback-codifier` to capture learnings
4. **Research First**: Use researcher agents before implementing new patterns
5. **Regular Reviews**: Run `/review` before every commit

---

## Agent Evolution

These agents improve over time as they:
- Learn your codebase patterns
- Understand your team's preferences
- Accumulate domain knowledge
- Build on previous reviews

The more you use them, the better they become at catching issues specific to your project and tech stack.