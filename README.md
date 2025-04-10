![CursorRIPER♦Σ](./res/github-header-sigma-sm.png)
# CursorRIPER♦Σ (Sigma)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
![Version](https://img.shields.io/badge/version-1.0.1-green)

> A symbolic, ultra-efficient AI prompt framework for software development assistance with code protection capabilities.

## 📚 Overview

CursorRIPER♦Σ is a highly optimized, symbolic implementation of the  [CursorRIPER framework](https://github.com/johnpeterman72/CursorRIPER) designed to enhance AI-assisted software development. It uses a symbolic notation system with mathematical operators, emojis, and Greek letters to compress complex development workflows into a minimal, yet comprehensive, token-friendly footprint.

The framework reduces ~15,000 words of instructions to under 1,000 while preserving full functionality, making it dramatically more efficient for AI token usage. The idea came from [Tof](https://forum.cursor.com/t/user-rules-with-memory-errors-tracking-rules-generation/68321)

## 🌟 Key Features

- **Symbolic Notation**: Uses Greek letters (Ω, Π, Σ, Δ), subscripts, and emoji for extreme conciseness
- **RIPER Workflow Modes**: Research, Innovate, Plan, Execute, Review (🔍R, 💡I, 📝P, ⚙️E, 🔎RV)
- **Structured Memory System**: Standardized file templates with cross-referencing
- **Phase-based Project Management**: Tracks project progress from initialization to maintenance
- **Automatic Memory**: Creates and maintains a structured memory bank for project context
- **Code Protection System**: Protects critical code sections with intelligent comment annotations

## 🧠 Framework Structure

### Modes (Ω)

```
Ω₁ = 🔍R ⟶ Research: Gather information and document findings
Ω₂ = 💡I ⟶ Innovate: Explore options and suggest ideas
Ω₃ = 📝P ⟶ Plan: Create specifications and sequence steps
Ω₄ = ⚙️E ⟶ Execute: Implement code according to plan
Ω₅ = 🔎RV ⟶ Review: Validate output against requirements
```

### Phases (Π)

```
Π₁ = 🌱UNINITIATED ⟶ Framework installed but not started
Π₂ = 🚧INITIALIZING ⟶ Setup in progress
Π₃ = 🏗️DEVELOPMENT ⟶ Main development work
Π₄ = 🔧MAINTENANCE ⟶ Long-term support
```

### Memory Files (σ)

```
σ₁ = 📋projectbrief.md ⟶ Requirements, scope, criteria
σ₂ = 🏛️systemPatterns.md ⟶ Architecture, components, decisions
σ₃ = 💻techContext.md ⟶ Stack, environment, dependencies
σ₄ = 🔮activeContext.md ⟶ Focus, changes, next steps
σ₅ = 📊progress.md ⟶ Status, milestones, issues
σ₆ = 🛡️protection.md ⟶ Protected regions, history, approvals
```

### Protection Levels (Ψ)

```
Ψ₁ = PROTECTED ⟶ Highest protection, do not modify
Ψ₂ = GUARDED ⟶ Ask before modifying
Ψ₃ = INFO ⟶ Context note
Ψ₄ = DEBUG ⟶ Debugging code
Ψ₅ = TEST ⟶ Testing code
Ψ₆ = CRITICAL ⟶ Business logic, highest protection
```

## 🚀 Getting Started

### Installation

1. Create a memory bank directory in your project:

```bash
mkdir -p /memory-bank/backups
```

2. Copy the CursorRIPER♦Σ framework `.mdc` files to your project rules folder: `.cursor/rules/`

4. Initialize the framework with the AI assistant:

```
/start
```

### Usage

Change modes by using the following commands with your AI assistant:

```
/research (or /r) - Research mode
/innovate (or /i) - Innovate mode
/plan (or /p) - Plan mode
/execute (or /e) - Execute mode
/review (or /rev) - Review mode
```

## 📑 Memory System

The framework automatically maintains six key memory files:

1. **Project Brief** (σ₁): Defines requirements, success criteria, and scope
2. **System Patterns** (σ₂): Captures architecture, components, and design decisions
3. **Technical Context** (σ₃): Records technology stack, environment, and dependencies
4. **Active Context** (σ₄): Tracks current focus, recent changes, and next steps
5. **Progress Tracker** (σ₅): Monitors project status, features, issues, and milestones
6. **Protection Registry** (σ₆): Tracks protected code regions, history, and approvals

## 🛡️ Code Protection System

The framework includes a robust code protection system that helps preserve critical code sections from unintended modifications:

### Protection Levels

- **PROTECTED**: Code that must not be modified under any circumstances
- **GUARDED**: Code that requires explicit permission before modification
- **INFO**: Context information relevant to understanding code
- **DEBUG**: Temporary code used for debugging purposes
- **TEST**: Code related to testing functionality
- **CRITICAL**: Business logic that must be treated with extreme care

### Protection Commands

Add code protection with shorthand commands:

```
!cp - Add PROTECTED comment
!cg - Add GUARDED comment
!ci - Add INFO comment
!cd - Add DEBUG comment
!ct - Add TEST comment
!cc - Add CRITICAL comment
```

See [Protection Commands](./docs/ProtectionCommands.md) for full documentation.

## ⚠️ Safety Features

- Automatic backups before destructive operations
- Confirmation prompts for critical actions
- Phase transition verification
- Error recovery suggestions
- Code protection system with mode-aware behavior

## 🔣 Symbol Reference

See the [Symbol Reference Guide](./docs/symbols.md) for a complete list of symbols and notation used in the framework.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

*CursorRIPER♦Σ: Symbolic efficiency for AI-assisted development with intelligent code protection.*
