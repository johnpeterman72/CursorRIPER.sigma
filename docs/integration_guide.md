![CursorRIPER♦Σ](../res/github-header-sigma-sm.png)
# CursorRIPER.sigma User Guide
*Adding the CursorRIPER.sigma Framework to Existing Projects*

## Introduction

CursorRIPER.sigma is a highly condensed version of the CursorRIPER Framework using symbolic notation, emoji, and mathematical symbols. This framework provides a structured approach to project management through five RIPER modes (Research, Innovate, Plan, Execute, Review) and a robust memory system.

This guide will walk you through the process of integrating CursorRIPER.sigma with your existing projects.

## Prerequisites

- An existing project that you want to enhance with the CursorRIPER.sigma framework
- The CursorRIPER.sigma framework files

## Setup Process

### Step 1: Initialize the System

```
/initialize system
```

**What this does:** Creates the basic directory structure (📂 and 📦 folders) and generates all template memory files. It establishes the foundation for the framework by running the `Φ_file.init()` and `Φ_memory.initialize()` functions.

### Step 2: Set Development Phase

```
/set phase development
```

**What this does:** Establishes the current project phase as Π₁: 🏗️DEVELOPMENT, indicating that your project is in active development. This affects how the framework processes commands and what operations are available to you.

### Step 3: Set Research Mode

```
/set mode research
```
or the shorthand:
```
/r
```

**What this does:** Sets the current RIPER mode to Ω₁: 🔍RESEARCH, focusing the framework on gathering information about your existing project. This activates specific task categories in the framework and prepares it for analysis.

### Step 4: Update Project Brief

```
/update projectbrief
```

**What this does:** Opens the project summary template (σ₁) for editing, where you should input:
- Project overview and purpose
- Key requirements (R₁, R₂, etc.)
- Success criteria
- Project scope

This creates the foundation for all future framework operations.

### Step 5: Update Technical Context

```
/update techContext
```

**What this does:** Prompts you to document your existing project's technology stack, environment, and dependencies in the σ₃ memory file. This helps the framework understand the technical context of your project.

### Step 6: Analyze Project

```
/analyze project
```

**What this does:** Automatically scans your existing project structure and generates insights in the activeContext.md file (σ₄). This provides an initial assessment of your project's components and architecture.

### Step 7: Create Initial Progress Tracking

```
/create initial-progress
```

**What this does:** Establishes baseline metrics in the progress.md file (σ₅), setting initial completion percentages, milestones, and known issues based on your current project state.

### Step 8: Set Protection Levels

```
/set protection-levels
```

**What this does:** Configures appropriate code protection settings in the protection.md file (σ₆), establishing which parts of your code require special handling or permissions.

### Step 9: Create Initial Backup

```
/backup create initial
```

**What this does:** Creates the first backup of all memory files with a timestamped identifier. This preserves the initial state before the framework begins actively working with your project.

### Step 10: Transition to Innovate Mode

```
/mode innovate
```
or the shorthand:
```
/i
```

**What this does:** Transitions to Ω₂: 💡INNOVATE mode, enabling the framework to suggest improvements and possibilities based on the gathered research.

## Using RIPER Modes

The CursorRIPER.sigma framework operates through five distinct modes, each with its own focus:

### 🔍 Research Mode (Ω₁)
```
/mode research
```
or
```
/r
```
Focus: Understanding the project, gathering information, exploring the codebase

### 💡 Innovate Mode (Ω₂)
```
/mode innovate
```
or
```
/i
```
Focus: Generating ideas, suggesting improvements, exploring possibilities

### 📝 Plan Mode (Ω₃)
```
/mode plan
```
or
```
/p
```
Focus: Creating implementation plans, establishing milestones, setting priorities

### ⚙️ Execute Mode (Ω₄)
```
/mode execute
```
or
```
/e
```
Focus: Implementing solutions, writing code, following the established plan

### 🔎 Review Mode (Ω₅)
```
/mode review
```
or
```
/rev
```
Focus: Testing implementations, validating outputs, ensuring adherence to requirements

## Memory System

The framework maintains six memory files:

1. **σ₁: Project Brief** (📋) - Requirements, scope, and success criteria
2. **σ₂: System Patterns** (🏛️) - Architecture, components, and design decisions
3. **σ₃: Technical Context** (💻) - Technology stack, environment, and dependencies
4. **σ₄: Active Context** (🔮) - Current focus, changes, and next steps
5. **σ₅: Progress** (📊) - Status tracking, milestones, and issues
6. **σ₆: Protection** (🛡️) - Security levels and permission settings

## Advanced Features

### Context Reference System
Use Γ (Gamma) symbols to reference specific contexts:
```
[↗️σ₁:R₁|Γ₃]
```

### Permission System
Control access using ℙ (Pi) symbols:
```
[ℙ(Ω₁):read_only]
```

### Backup System
Create backups at any time:
```
/backup create custom_name
```

### File Protection
Six protection levels are available to secure code and resources:
```
/set protection-level file_name 3
```

## Troubleshooting

If you encounter issues:

1. Check the relevant memory files for error messages
2. Use `/status` to see the current state of the framework
3. Use `/validate system` to check for consistency issues
4. Restore from a backup if necessary: `/backup restore timestamp`

## Symbol Reference

For a complete reference of symbols used in the framework, check the automatically generated `symbol-reference-guide.md` file in the 📂 directory.

---

*For more detailed information on specific features, refer to the documentation in the docs/ directory.*
