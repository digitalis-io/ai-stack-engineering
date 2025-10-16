# AI Stack Engineering - Claude Code Plugin Marketplace

This repository is a Claude Code plugin marketplace for Digitalis.io that distributes the `ai-stack-engineering` plugin customized for our tech stack: Go, React/TypeScript, Apache Cassandra, PostgreSQL, Apache Kafka, and OpenSearch.

**Based on [every-marketplace](https://github.com/EveryInc/every-marketplace) by Every, Inc.** - We're grateful to Kieran Klaassen and the Every team for creating the original compounding engineering framework.

## Repository Structure

```
ai-stack-engineering/
├── .claude-plugin/
│   └── marketplace.json          # Marketplace catalog (lists available plugins)
└── plugins/
    └── compounding-engineering/   # The plugin (inherited structure)
        ├── .claude-plugin/
        │   └── plugin.json        # Plugin metadata
        ├── agents/                # 22 specialized AI agents (17 original + 5 new)
        ├── commands/              # 6 slash commands
        └── README.md              # Plugin documentation
```

## New Stack-Specific Agents

Our fork adds these agents for the Digitalis.io tech stack:
- `golang-reviewer` - Idiomatic Go review (Uber style guide, concurrency, interfaces)
- `cassandra-guardian` - Cassandra data modeling (modern compaction strategies), preventing hot partitions
- `kafka-guardian` - Event streaming reliability, preventing data loss
- `react-reviewer` - Modern React/TypeScript, fixing re-renders and hook issues
- `search-sentinel` - OpenSearch/Elasticsearch relevance and performance (works with both)

Note: PostgreSQL optimization is covered by the existing `data-integrity-guardian` agent.

## Philosophy: Compounding Engineering

**Each unit of engineering work should make subsequent units of work easier—not harder.**

When working on this repository, follow the compounding engineering process:

1. **Plan** → Understand the change needed and its impact
2. **Delegate** → Use AI tools to help with implementation
3. **Assess** → Verify changes work as expected
4. **Codify** → Update this CLAUDE.md with learnings

## Working with This Repository

### Adding a New Plugin

1. Create plugin directory: `plugins/new-plugin-name/`
2. Add plugin structure:
   ```
   plugins/new-plugin-name/
   ├── .claude-plugin/plugin.json
   ├── agents/
   ├── commands/
   └── README.md
   ```
3. Update `.claude-plugin/marketplace.json` to include the new plugin
4. Test locally before committing

### Updating the AI Stack Engineering Plugin

When agents or commands are added/removed:

1. **Scan for actual files:**

   ```bash
   # Count agents
   ls plugins/compounding-engineering/agents/*.md | wc -l

   # Count commands
   ls plugins/compounding-engineering/commands/*.md | wc -l
   ```

2. **Update plugin.json** at `plugins/compounding-engineering/.claude-plugin/plugin.json`:

   - Update `components.agents` count
   - Update `components.commands` count
   - Update `agents` object to reflect which agents exist
   - Update `commands` object to reflect which commands exist
   - Remember: plugin name is `ai-stack-engineering` but directory is still `compounding-engineering`

3. **Update plugin README** at `plugins/compounding-engineering/README.md`:

   - Update agent/command counts in the intro
   - Update the agent/command lists to match what exists

4. **Update marketplace.json** at `.claude-plugin/marketplace.json`:
   - Usually doesn't need changes unless changing plugin description/tags

### Marketplace.json Structure

The marketplace.json follows the official Claude Code spec:

```json
{
  "name": "marketplace-identifier",
  "owner": {
    "name": "Owner Name",
    "url": "https://github.com/owner"
  },
  "metadata": {
    "description": "Marketplace description",
    "version": "1.0.0"
  },
  "plugins": [
    {
      "name": "plugin-name",
      "description": "Plugin description",
      "version": "1.0.0",
      "author": { ... },
      "homepage": "https://...",
      "tags": ["tag1", "tag2"],
      "source": "./plugins/plugin-name"
    }
  ]
}
```

**Only include fields that are in the official spec.** Do not add custom fields like:

- `downloads`, `stars`, `rating` (display-only)
- `categories`, `featured_plugins`, `trending` (not in spec)
- `type`, `verified`, `featured` (not in spec)

### Plugin.json Structure

Each plugin has its own plugin.json with detailed metadata:

```json
{
  "name": "plugin-name",
  "version": "1.0.0",
  "description": "Plugin description",
  "author": { ... },
  "keywords": ["keyword1", "keyword2"],
  "components": {
    "agents": 22,
    "commands": 6
  },
  "agents": {
    "category": [
      {
        "name": "agent-name",
        "description": "Agent description",
        "use_cases": ["use-case-1", "use-case-2"]
      }
    ]
  },
  "commands": {
    "category": ["command1", "command2"]
  }
}
```

## Testing Changes

### Test Locally

1. Install the marketplace locally:

   ```bash
   claude /plugin marketplace add /Users/yourusername/ai-stack-engineering
   ```

2. Install the plugin:

   ```bash
   claude /plugin install ai-stack-engineering
   ```

3. Test agents and commands:
   ```bash
   claude /review
   claude agent golang-reviewer "review this Go code"
   claude agent cassandra-guardian "review this Cassandra schema"
   claude agent kafka-guardian "check my consumer offset management"
   claude agent search-sentinel "optimize this search query"
   ```

### Validate JSON

Before committing, ensure JSON files are valid:

```bash
cat .claude-plugin/marketplace.json | jq .
cat plugins/compounding-engineering/.claude-plugin/plugin.json | jq .
```

## Common Tasks

### Adding a New Agent

1. Create `plugins/compounding-engineering/agents/new-agent.md`
2. Update plugin.json agent count and agent list
3. Update README.md agent list
4. Test with `claude agent new-agent "test"`

### Adding a New Command

1. Create `plugins/compounding-engineering/commands/new-command.md`
2. Update plugin.json command count and command list
3. Update README.md command list
4. Test with `claude /new-command`

### Updating Tags/Keywords

Tags should reflect the compounding engineering philosophy and our tech stack:

- Core philosophy: `ai-powered`, `compounding-engineering`, `workflow-automation`, `knowledge-management`
- Tech stack: `go`, `golang`, `react`, `typescript`, `cassandra`, `postgresql`, `kafka`, `opensearch`
- General: `code-review`, `quality`

## Commit Conventions

Follow these patterns for commit messages:

- `Add [agent/command name]` - Adding new functionality
- `Remove [agent/command name]` - Removing functionality
- `Update [file] to [what changed]` - Updating existing files
- `Fix [issue]` - Bug fixes
- `Simplify [component] to [improvement]` - Refactoring

Include the Claude Code footer:

```
🤖 Generated with [Claude Code](https://claude.com/claude-code)

Co-Authored-By: Claude <noreply@anthropic.com>
```

## Resources to search for when needing more information

- [Claude Code Plugin Documentation](https://docs.claude.com/en/docs/claude-code/plugins)
- [Plugin Marketplace Documentation](https://docs.claude.com/en/docs/claude-code/plugin-marketplaces)
- [Plugin Reference](https://docs.claude.com/en/docs/claude-code/plugins-reference)

## Key Learnings

_This section captures important learnings as we work on this repository._

### 2025-10-16: Forked from every-marketplace for Digitalis.io tech stack

Created AI Stack Engineering as a fork of every-marketplace by Every, Inc. Key customizations:

- Added 5 new stack-specific agents with personality and voice matching existing quality:
  - `golang-reviewer` - Pragmatic Go engineer who's debugged production at 3am
  - `cassandra-guardian` - Battle-hardened Cassandra expert (modern features, UCS)
  - `kafka-guardian` - Reliability engineer who's hunted down data loss bugs
  - `react-reviewer` - Frontend dev who's fixed infinite re-renders too many times
  - `search-sentinel` - OpenSearch/Elasticsearch engineer who's tuned relevance at scale
- Used consistent naming patterns: reviewer, guardian, sentinel (matching existing agents)
- Each agent has personality, philosophy, memorable closing lines like dhh-rails-reviewer
- Removed postgresql-specialist (covered by existing data-integrity-guardian)
- Updated code-simplicity-reviewer with measurable quality metrics (cyclomatic complexity, SOLID principles)
- Updated all metadata (marketplace.json, plugin.json) to reflect ai-stack-engineering branding
- Maintained proper attribution to original project in LICENSE, README.md, and CLAUDE.md

**Learning:** Agent quality matters more than quantity. Each agent should have a distinct voice and personality, not just be a checklist. Use consistent naming patterns that match the existing ecosystem.

### 2025-10-09: Simplified marketplace.json to match official spec (from original)

The initial marketplace.json included many custom fields (downloads, stars, rating, categories, trending) that aren't part of the Claude Code specification. We simplified to only include:

- Required: `name`, `owner`, `plugins`
- Optional: `metadata` (with description and version)
- Plugin entries: `name`, `description`, `version`, `author`, `homepage`, `tags`, `source`

**Learning:** Stick to the official spec. Custom fields may confuse users or break compatibility with future versions.
