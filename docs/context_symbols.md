# 📎 Context Symbols Cheat Sheet
*v1.0 | Created: 2025-04-10*

## 🔍 Basic Context Symbols (Γ)

| Symbol | Emoji | Cursor Symbol | Description |
|--------|-------|---------------|-------------|
| Γ₁     | 📄    | @Files        | File reference |
| Γ₂     | 📁    | @Folders      | Folder reference |
| Γ₃     | 💻    | @Code         | Code reference |
| Γ₄     | 📚    | @Docs         | Documentation reference |
| Γ₅     | 📏    | @Cursor Rules | Project rules reference |
| Γ₆     | 🔄    | @Git          | Git history reference |
| Γ₇     | 📝    | @Notepads     | Notepad reference |
| Γ₈     | 📌    | #Files        | File context without reference |

## 🛠️ Command Shortcuts

| Command | Function | Description |
|---------|----------|-------------|
| !af     | Add File | Add file reference to context |
| !ad     | Add Directory | Add folder reference to context |
| !ac     | Add Code | Add code reference to context |
| !adoc   | Add Doc | Add documentation reference to context |
| !ar     | Add Rule | Add rule reference to context |
| !ag     | Add Git | Add git reference to context |
| !an     | Add Notepad | Add notepad reference to context |
| !pf     | Pin File | Pin file to context without reference |
| !cs     | Context Status | Set context reference status |
| !cr     | Context Remove | Remove context reference |
| !cc     | Context Clear | Clear all context references |
| !cm     | Context Mode | Set context for current mode |

## 🔄 Mode-Context Mapping

| Mode | Symbol | Default Context | Description |
|------|--------|----------------|-------------|
| RESEARCH | 🔍 Ω₁ | [Γ₄, Γ₂, Γ₆] | Docs, Folders, Git |
| INNOVATE | 💡 Ω₂ | [Γ₃, Γ₄, Γ₇] | Code, Docs, Notepads |
| PLAN | 📝 Ω₃ | [Γ₁, Γ₂, Γ₅] | Files, Folders, Rules |
| EXECUTE | ⚙️ Ω₄ | [Γ₃, Γ₁, Γ₈] | Code, Files, Pinned Files |
| REVIEW | 🔎 Ω₅ | [Γ₃, Γ₁, Γ₆] | Code, Files, Git |

## 🔄 Context Status Indicators

| Indicator | Description | Usage |
|-----------|-------------|-------|
| 🟢 | Active context | Currently relevant and in use |
| 🟡 | Partially relevant | Somewhat relevant but not primary |
| 🟣 | Essential | Core/essential context that must be considered |
| 🔴 | Deprecated | No longer relevant, maintained for history |

## 🔗 Cross-Reference with Context

| Reference Type | Syntax | Example | Description |
|----------------|--------|---------|-------------|
| Standard | [↗️σₙ:Xᵢ] | [↗️σ₁:R₁] | Reference to item in memory file |
| With Context | [↗️σₙ:Xᵢ\|Γₘ] | [↗️σ₁:R₁\|Γ₃] | Reference with context |
| Context-only | [Γₙ:item] | [Γ₃:validate()] | Direct context reference |
| Protection+Context | [Ψₙ+Γₘ:item] | [Ψ₁+Γ₃:auth()] | Protected context reference |

## 🛡️ Protection-Context Integration

| Symbol | Combination | Description |
|--------|-------------|-------------|
| 🔒💻 | Ψ₁ + Γ₃ | Protected code |
| 🛡️💻 | Ψ₂ + Γ₃ | Guarded code |
| ℹ️💻 | Ψ₃ + Γ₃ | Info code |
| 🐞💻 | Ψ₄ + Γ₃ | Debug code |
| 🧪💻 | Ψ₅ + Γ₃ | Test code |
| ⚠️💻 | Ψ₆ + Γ₃ | Critical code |

## 📊 Context Operations

| Operation | Syntax | Description |
|-----------|--------|-------------|
| Intersection | Γₙ ∩ Γₘ | Context elements common to both |
| Union | Γₙ ∪ Γₘ | Combined context elements |
| Apply to Mode | Γₙ → Ωₘ | Applying context to mode |
| Store in Memory | Γₙ ⟶ σₘ | Storing context in memory file |

## 📝 Context Usage Examples

```
// Add specific file to context
!af src/main.js

// Add code element with status
!ac validateUser()
!cs validateUser() essential

// Apply mode-specific context
!cm

// Cross-reference with context
Requirement [↗️σ₁:R₁|Γ₃:auth()] specifies...

// Reference protected code
The 🔒💻 auth() function should not be modified
```

---
*Quick reference for CursorRIPER Σ context system*