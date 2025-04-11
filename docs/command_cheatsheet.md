![CursorRIPER♦Σ](../res/github-header-sigma-sm.png)
# 📑 CursorRIPER Σ Command Cheatsheet

*v1.0 | Last Updated: 2025-04-11*

This cheatsheet provides a quick reference for all commands in the CursorRIPER Σ framework. Commands are organized by system and functionality.

## 🔍 RIPER Mode Commands

Switch between RIPER modes using these natural language commands:

| Natural Command | Shorthand | Symbol | Mode | Focus |
|-----------------|-----------|--------|------|-------|
| `/research`     | `/r`      | Ω₁/🔍R | RESEARCH | Gathering information and understanding the problem |
| `/innovate`     | `/i`      | Ω₂/💡I | INNOVATE | Generating ideas and exploring possibilities |
| `/plan`         | `/p`      | Ω₃/📝P | PLAN | Creating structured plans and specifications |
| `/execute`      | `/e`      | Ω₄/⚙️E | EXECUTE | Implementing the planned solution |
| `/review`       | `/rev`    | Ω₅/🔎RV | REVIEW | Validating and reviewing the implementation |

## 🔒 Protection System Commands

Control code protection levels using these commands:

| Command | Description | Protection Level |
|---------|-------------|------------------|
| `!cp`   | Set code to PROTECTED status | PROTECTED - DO NOT MODIFY |
| `!cg`   | Set code to GUARDED status | GUARDED - ASK BEFORE MODIFYING |
| `!ci`   | Set code to INFO status | INFO - CONTEXT NOTE |
| `!cd`   | Set code to DEBUG status | DEBUG - DEBUGGING CODE |
| `!ct`   | Set code to TEST status | TEST - TESTING CODE |
| `!cc`   | Set code to CRITICAL status | CRITICAL - BUSINESS LOGIC |

## 👁️ Context System Commands

Manage context references with these commands:

| Command | Description | Context Type |
|---------|-------------|--------------|
| `!af`   | Add FILES to context | Γ₁ (Files) |
| `!ad`   | Add DOCS to context | Γ₂ (Documentation) |
| `!ac`   | Add CODE to context | Γ₃ (Code) |
| `!ai`   | Add ISSUES to context | Γ₄ (Issues) |
| `!ap`   | Add PLANS to context | Γ₅ (Plans) |
| `!ar`   | Add REQUIREMENTS to context | Γ₆ (Requirements) |
| `!aa`   | Add APIs to context | Γ₇ (APIs) |
| `!at`   | Add TESTS to context | Γ₈ (Tests) |
| `!afs`  | Add FILESYSTEM to context | Γ₉ (Filesystem) |

## 🔑 Permission System Commands

Manage operation permissions with these commands:

| Command | Description |
|---------|-------------|
| `!ckp`  | Check permissions for current mode |
| `!pm`   | Check if operation is permitted in current mode |
| `!sp`   | Show all permissions for specified mode |
| `!vm`   | Verify mode appropriate for operation |

## 📁 Filesystem Commands (MCP)

Perform filesystem operations with these commands:

| Command | Description | Operation |
|---------|-------------|-----------|
| `!fr`   | Read file contents | Φ_fs.read |
| `!fm`   | Read multiple files | Φ_fs.read_multi |
| `!fw`   | Write to file | Φ_fs.write |
| `!fe`   | Edit file | Φ_fs.edit |
| `!fc`   | Create directory | Φ_fs.create_dir |
| `!fl`   | List directory contents | Φ_fs.list |
| `!ft`   | View directory tree | Φ_fs.tree |
| `!fv`   | Move file | Φ_fs.move |
| `!fs`   | Search files | Φ_fs.search |
| `!fi`   | Get file info | Φ_fs.info |
| `!fa`   | List allowed directories | Φ_fs.allowed |

## 💾 Memory Management Commands

Access and update memory files:

| Command | Description | Memory File |
|---------|-------------|-------------|
| `@ps`   | Access Project Summary | σ₁ (Project Summary) |
| `@sp`   | Access System Patterns | σ₂ (System Patterns) |
| `@tc`   | Access Tech Context | σ₃ (Tech Context) |
| `@ac`   | Access Active Context | σ₄ (Active Context) |
| `@pg`   | Access Progress | σ₅ (Progress) |
| `@pt`   | Access Protection | σ₆ (Protection) |

## 📊 Cross-Reference Notation

Create references between elements using these formats:

| Format | Description | Example |
|--------|-------------|---------|
| `[↗️σ₁:R₁]` | Reference to Requirement 1 in Project Summary | `This feature addresses [↗️σ₁:R₁]` |
| `[↗️σ₂:C₁]` | Reference to Component 1 in System Patterns | `Implements the [↗️σ₂:C₁] pattern` |
| `[↗️σ₃:T₁]` | Reference to Technology 1 in Tech Context | `Using [↗️σ₃:T₁] for implementation` |
| `[↗️σ₁:R₁\|Γ₃]` | Reference with context | `Code for [↗️σ₁:R₁\|Γ₃]` |
| `[ℙ(Ω₁):read_only]` | Reference with permissions | `This operation is [ℙ(Ω₁):read_only]` |
| `[Γ₉:path/to/file.js]` | Filesystem reference | `See [Γ₉:path/to/file.js]` |

## 🛡️ Safety Protocols

Safety protocols that trigger automatically:

| Symbol | Description | Trigger |
|--------|-------------|---------|
| Δ₁ | Destructive operation warning | When performing destructive operations |
| Δ₂ | Phase transition backup | When changing project phase |
| Δ₃-Δ₆ | Various safety checks | System-specific conditions |
| Δ₇ | Filesystem operation safety | When performing write operations |

## 🔄 Backup Commands

Manage system backups:

| Command | Description |
|---------|-------------|
| `!backup` | Create manual backup of all memory files |
| `!restore <timestamp>` | Restore from backup with specified timestamp |
| `!list-backups` | List all available backups |

## 🔮 Tips for Effective Use

- **Start with the right mode**: Use `/r` when starting research, `/p` before implementation
- **Keep context relevant**: Use context commands to maintain focus on current tasks
- **Respect permissions**: Don't attempt operations forbidden in current mode
- **Use protection wisely**: Set appropriate protection levels for sensitive code
- **Cross-reference often**: Use cross-references to maintain traceability
- **Backup before major changes**: Create manual backups before significant changes

---

Remember, you can use natural language commands instead of symbolic notation for all operations. The framework will work exactly the same way with either approach.

For a full reference of all symbols, see `docs/symbols.md`.
