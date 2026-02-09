# 🤖 Claude Code Agents

A curated collection of 16 custom subagents for [Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview) — drop them in and let Claude automatically delegate tasks to the right specialist.

Built for full-stack developers and solo founders working with **React Native**, **Next.js**, **TypeScript**, and building products end-to-end.

## Why Custom Agents?

Claude Code's subagents give you:
- **Separate context windows** — keep your main conversation clean
- **Specialized system prompts** — each agent is an expert at one thing
- **Cost control** — route routine tasks to Haiku, complex ones to Sonnet
- **Automatic delegation** — Claude picks the right agent based on your task

## 📦 Agents

### 🛠 Engineering

| Agent | Model | What It Does |
|-------|-------|-------------|
| `react-native-dev` | Sonnet | Expo/RN components, navigation, native APIs, platform-specific code |
| `nextjs-dev` | Sonnet | App Router, server components, server actions, API routes |
| `api-architect` | Sonnet | REST API design, database schemas, auth flows, system design |
| `ui-designer` | Sonnet | Component styling, layouts, design systems (Tailwind + StyleSheet) |
| `code-reviewer` | Sonnet | Security, quality, performance, and best practice review (read-only) |
| `debugger` | Sonnet | Systematic root cause analysis with a structured diagnostic process |
| `perf-optimizer` | Sonnet | Re-render fixes, bundle size, network, memory leaks |
| `test-writer` | Haiku | Unit, integration, and E2E tests with Jest + Testing Library |
| `git-manager` | Haiku | Commits, branches, PRs, merge conflicts, conventional commits |
| `doc-writer` | Haiku | READMEs, API docs, architecture docs, inline comments |

### 📈 Marketing & Growth

| Agent | Model | What It Does |
|-------|-------|-------------|
| `cmo` | Sonnet | Brand positioning, GTM strategy, messaging frameworks, campaign architecture, asset review with a perfectionist CMO eye |
| `creative-director` | Sonnet | Visual design direction, UI polish, brand identity, pixel-level design critique, app store assets, landing page design review |
| `demand-gen` | Sonnet | Demand generation, lead funnels, SEO/content strategy, email sequences, landing page CRO, paid acquisition, growth experiments |

### 🗂 Planning

| Agent | Model | What It Does |
|-------|-------|-------------|
| `product-planner` | Sonnet | Feature specs, user stories, task breakdown, prioritization |

### 🙏 Personal

| Agent | Model | What It Does |
|-------|-------|-------------|
| `faith-anchor` | Haiku | Detects when you're struggling, reminds you to pray, and delivers a Bible verse matched to your exact situation |
| `et-motivator` | Haiku | Eric Thomas-style motivation rooted in faith. Fires up when you're about to quit — intense, raw, and points you back to God's purpose for your life |

> 💡 Haiku agents are 3x cheaper and 2x faster — great for routine tasks. Sonnet handles the heavy lifting.

## 🚀 Quick Start

### Install globally (all projects)
```bash
git clone https://github.com/YOUR_USERNAME/claude-code-agents.git
mkdir -p ~/.claude/agents
cp claude-code-agents/agents/*.md ~/.claude/agents/
```

### Install per-project
```bash
cd your-project
mkdir -p .claude/agents
cp path/to/claude-code-agents/agents/*.md .claude/agents/
```

### Cherry-pick specific agents
```bash
mkdir -p ~/.claude/agents
cp agents/debugger.md ~/.claude/agents/
cp agents/code-reviewer.md ~/.claude/agents/
```

## 💬 Usage

Once installed, Claude Code **automatically delegates** to the right agent. You can also invoke them explicitly:

```
> Use the debugger agent to figure out why the app crashes on launch
> Use the code-reviewer agent to review my staged changes
> Use the product-planner agent to break down the search feature into tasks
> Use the perf-optimizer agent to check why this screen is laggy
```

Manage your agents anytime:
```
/agents
```

## 🔧 Customization

Every agent is a Markdown file with YAML frontmatter. Fork this repo and make them yours:

**Change the model:**
```yaml
model: opus    # Most capable, highest cost
model: sonnet  # Balanced (default for most agents)
model: haiku   # Fast and cheap
```

**Restrict tools:**
```yaml
tools: Read, Grep, Glob  # Read-only agent
tools: Read, Write, Edit, Bash, Glob, Grep  # Full access
```

**Edit the system prompt:**
The body of each `.md` file IS the system prompt. Add your conventions, remove what you don't need, make it specific to your stack.

## 📂 Repo Structure

```
claude-code-agents/
├── agents/
│   ├── react-native-dev.md
│   ├── nextjs-dev.md
│   ├── code-reviewer.md
│   ├── debugger.md
│   ├── api-architect.md
│   ├── ui-designer.md
│   ├── test-writer.md
│   ├── git-manager.md
│   ├── product-planner.md
│   ├── perf-optimizer.md
│   ├── doc-writer.md
│   ├── cmo.md
│   ├── creative-director.md
│   ├── demand-gen.md
│   ├── faith-anchor.md
│   └── et-motivator.md
├── README.md
├── LICENSE
└── install.sh
```

## ⚡ One-Line Install

```bash
curl -fsSL https://raw.githubusercontent.com/YOUR_USERNAME/claude-code-agents/main/install.sh | bash
```

## 🤝 Contributing

1. Fork this repo
2. Add or improve an agent in `agents/`
3. Test it in Claude Code (`/agents` to verify it loads)
4. Open a PR with a description of what the agent does and when to use it

Agent PRs should include:
- A clear `name` and `description` in the frontmatter
- A focused system prompt (one job, done well)
- Appropriate model choice with rationale
- Minimal tool permissions (principle of least privilege)

## 📄 License

MIT — use these however you want.

---

**Built with [Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview)** · Star ⭐ if these agents save you time
