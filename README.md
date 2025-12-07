# Cursor AI Configuration for Software Engineers

A battle-tested collection of **Cursor IDE Rules and Commands** that supercharge your development workflow with AI assistance. These configurations provide structured, high-quality AI interactions for coding, debugging, architecture, and more.

## 🎯 What's This?

This repository contains production-ready **Cursor IDE configurations** organized into two powerful components:

1. **📋 Rules** (`.cursor/rules/`) - Automated AI workflows that guide the assistant through complex, multi-step processes
2. **⚡ Commands** (`.cursor/commands/`) - Quick-access prompt templates for common development tasks

These configurations help you:

- ✅ Get consistent, high-quality AI responses
- ✅ Automate complex workflows (PRDs, task generation, debugging)
- ✅ Reduce hallucinations and vague answers
- ✅ Generate production-ready code with tests
- ✅ Save time with reusable prompt templates

---

## 📌 Table of Contents

- [Quick Start](#-quick-start)
- [How to Use](#-how-to-use)
  - [Using Cursor Rules](#using-cursor-rules)
  - [Using Cursor Commands](#using-cursor-commands)
- [Available Configurations](#-available-configurations)
  - [Cursor Rules](#cursor-rules-automated-workflows)
  - [Cursor Commands](#cursor-commands-quick-prompts)
- [Installation](#-installation)
- [Prompt Strategy Reference](#-prompt-strategy-reference)

---

## 🚀 Quick Start

1. **Clone or copy this repository** into your project
2. The `.cursor/` folder will be automatically detected by Cursor IDE
3. Access **Rules** via the Rules panel or by mentioning them in chat
4. Access **Commands** via `Cmd+L` → Command palette or by typing the command name

---

## 💡 How to Use

### Using Cursor Rules

**Rules** are multi-step AI workflows that guide the assistant through complex processes. They're perfect for:

- Creating Product Requirements Documents
- Generating detailed task lists
- Deep-dive debugging and issue analysis

**How to trigger:**

1. Open Cursor's Rules panel (right sidebar)
2. Select a rule (e.g., "Generating a Product Requirements Document")
3. The AI will follow the structured workflow defined in the rule

**Example:**

```
@create-prd Build a user authentication system with email/password
```

The AI will:

1. Ask 3-5 clarifying questions
2. Wait for your responses
3. Generate a complete PRD in `/tasks/[feature-name]/prd-[feature-name].md`

---

### Using Cursor Commands

**Commands** are quick-access prompt templates for common tasks. They're perfect for:

- Quick code reviews
- Generating tests
- API design
- Performance optimization

**How to use:**

1. Type `/` in the chat to see available commands
2. Or simply type the command name (e.g., `qa-discovery`, `review-code`)
3. Fill in the placeholders with your specific context

**Example:**

```
@qa-discovery
Ask me up to 10 prioritized clarifying questions before producing any solution for:
Building a real-time notification system
```

---

## 📚 Available Configurations

### Cursor Rules (Automated Workflows)

Located in `.cursor/rules/` - These provide structured, multi-step guidance:

| Rule                 | Description                                       | Output                              |
| -------------------- | ------------------------------------------------- | ----------------------------------- |
| `create-prd.mdc`     | Generate detailed Product Requirements Documents  | `/tasks/[feature]/prd-[feature].md` |
| `debug.mdc`          | Create comprehensive issue analysis and fix plans | `/tasks/issue-[bug].md`             |
| `generate-tasks.mdc` | Break down features into actionable task lists    | `/tasks/tasks-[feature].md`         |

**Key Features:**

- ✅ Always asks clarifying questions first
- ✅ Uses multiple-choice format for easy responses (e.g., "1A, 2C")
- ✅ Automatically saves output to organized locations
- ✅ Designed for junior-friendly documentation

---

### Cursor Commands (Quick Prompts)

Located in `.cursor/commands/` - Quick-access templates for common tasks:

#### 🔍 Discovery & Planning

- `qa-discovery` - Ask prioritized clarifying questions before solving
- `pros-cons` - Compare architecture/design options with trade-offs
- `stepwise` - Break solutions into numbered steps with checkpoints

#### 🐛 Debugging & Quality

- `debug-checklist` - Generate prioritized debugging checklists
- `mre-bug` - Create minimal reproducible examples
- `review-code` - Comprehensive code review with diffs

#### 🏗️ Design & Architecture

- `api-design` - Design REST APIs with examples and specs
- `role-expert` - Invoke senior engineer persona for guidance
- `security-check` - Security audit with threat analysis

#### 🔧 Implementation

- `refactor-before-after` - Refactoring guide with comparisons
- `test-ci-gen` - Generate tests and CI/CD workflows
- `perf-optimize` - Performance tuning plans with benchmarks

#### 📝 Documentation & Workflow

- `auto-commit` - Generate commit messages and PR descriptions
- `prompt-refine` - Improve your prompts for better results
- `context7` - Auto-leverage Context7 for version-specific docs

---

## 💻 Installation

### Option 1: Use in Your Project (Recommended)

```bash
# Clone this repo
git clone https://github.com/yourusername/swe-essential-prompts.git

# Copy the .cursor folder to your project
cp -r swe-essential-prompts/.cursor /path/to/your/project/

# Cursor will automatically detect the configuration
```

### Option 2: Global Configuration

```bash
# Copy to your global Cursor config (applies to all projects)
cp -r .cursor ~/.cursor/global/

# Note: Check Cursor documentation for current global config path
```

### Option 3: Fork & Customize

1. Fork this repository
2. Customize rules and commands for your team's workflow
3. Share via Git for team-wide consistency

---

## 🎓 Prompt Strategy Reference

The configurations in this repo follow proven prompt engineering principles:

### Core Principles

All prompts and rules follow these battle-tested principles:

1. **🎯 Clear Role Instructions** - Specify expertise level and perspective
2. **📋 Explicit Output Format** - Define exactly what you want to receive
3. **🔄 Step-by-Step with Checkpoints** - Prevent AI from jumping ahead
4. **🔍 Visibility of Assumptions** - AI must state what it's assuming
5. **✅ Verification Built-In** - Tests, validation, and next steps included
6. **📁 File Structure Awareness** - Code includes context and organization
7. **🎓 Junior-Friendly** - Documentation accessible to all skill levels

### Key Patterns Used

#### 1. **Q&A Discovery** (`qa-discovery`)

Ask prioritized clarifying questions before solving. Reduces hallucinations.

#### 2. **Trade-off Analysis** (`pros-cons`)

Compare options with pros/cons, complexity, and recommendations.

#### 3. **Stepwise Execution** (`stepwise`)

Break into numbered steps, stop after each, wait for "next" command.

#### 4. **Expert Persona** (`role-expert`)

Invoke specific expertise level and reasoning style.

#### 5. **Minimal Reproducible Examples** (`mre-bug`)

Create runnable examples with file structure and commands.

---

## 🎯 Common Use Cases

### 🚀 Starting New Features

```
@create-prd Build a real-time notification system
```

→ Generates complete PRD with clarifying questions

### 🐛 Debugging Issues

```
@debug Analyze: Users can't log in after password reset
```

→ Creates structured issue analysis with root cause and fix plan

### 📋 Breaking Down Work

```
@generate-tasks Implement user profile editing feature
```

→ Generates hierarchical task list with sub-tasks and relevant files

### 🔍 Code Review

```
@review-code
```

→ Reviews current file with bugs, improvements, and suggested changes

### 🏗️ Architecture Decisions

```
@pros-cons
Compare: PostgreSQL, MongoDB, DynamoDB for user data storage
```

→ Detailed trade-off analysis with recommendation

### ⚡ Performance Tuning

```
@perf-optimize Optimize the dashboard rendering performance
```

→ Profiling plan, benchmarks, and optimization suggestions

---

## 🔧 Customization

### Adding Your Own Commands

1. Create a new `.md` file in `.cursor/commands/`
2. Use this template:

```markdown
# your-command-name

Brief description of what this command does.

[Placeholder for context - e.g., your code, feature description]

Provide:

- Expected output 1
- Expected output 2
- Expected output 3

Optional additional instructions...
```

3. Use it in Cursor: `@your-command-name`

### Adding Your Own Rules

1. Create a new `.mdc` file in `.cursor/rules/`
2. Start with front matter:

```markdown
---
alwaysApply: false
---

# Rule: Your Rule Name

## Goal

Clear description of what this rule accomplishes

## Process

1. Step 1
2. Step 2
   ...
```

3. Access via Cursor's Rules panel

---

## 💪 Best Practices

### 1. **Be Specific with Context**

❌ `@review-code`
✅ `@review-code Focus on security vulnerabilities and error handling`

### 2. **Chain Commands**

```
@qa-discovery Design a payment processing system
[Answer questions]
@create-prd [based on answers]
@generate-tasks [based on PRD]
```

### 3. **Use Stepwise for Complex Tasks**

```
@stepwise Migrate authentication from custom JWT to Auth0
[Say "next" after each step]
```

### 4. **Combine with Context7**

The `context7` command automatically checks your dependencies for version-specific docs:

```
@context7 Show me how to implement file uploads with Next.js
```

---

## 📚 Additional Resources

- [Cursor IDE Documentation](https://cursor.sh/docs)
- [Prompt Engineering Guide](https://www.promptingguide.ai/)
- [Context7 Documentation](https://context7.com/)

---

## 🤝 Contributing

Found a useful prompt pattern? Contributions welcome!

1. Fork this repository
2. Add your rule/command
3. Test it thoroughly
4. Submit a PR with examples

---

## 📄 License

MIT License - feel free to use and modify for your team

---

## 🙏 Acknowledgments

Built with ❤️ by software engineers who believe AI should be a force multiplier, not a source of frustration.

**Happy Coding!** 🚀
