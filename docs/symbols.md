# 🔣 Symbol Reference Guide
*v1.3 | Created: 2025-04-09 | Updated: 2025-04-10*

## 📁 File Symbols
- 📂 = /memory-bank/
- 📦 = /memory-bank/backups/
- σ₁ = projectbrief.md
- σ₂ = systemPatterns.md
- σ₃ = techContext.md
- σ₄ = activeContext.md
- σ₅ = progress.md
- σ₆ = protection.md

## 🔄 Mode & Phase Symbols
- Ω₁ = 🔍 RESEARCH
- Ω₂ = 💡 INNOVATE
- Ω₃ = 📝 PLAN
- Ω₄ = ⚙️ EXECUTE
- Ω₅ = 🔎 REVIEW
- Π₁ = 🌱 UNINITIATED
- Π₂ = 🚧 INITIALIZING
- Π₃ = 🏗️ DEVELOPMENT
- Π₄ = 🔧 MAINTENANCE

## 🛡️ Protection Symbols (Ψ)
- Ψ₁ = PROTECTED - Do not modify
- Ψ₂ = GUARDED - Ask before modifying
- Ψ₃ = INFO - Context note
- Ψ₄ = DEBUG - Debugging code
- Ψ₅ = TEST - Testing code
- Ψ₆ = CRITICAL - Business logic

## 📎 Context Symbols (Γ)
- Γ₁ = 📄 @Files - File reference
- Γ₂ = 📁 @Folders - Folder reference
- Γ₃ = 💻 @Code - Code reference
- Γ₄ = 📚 @Docs - Documentation reference
- Γ₅ = 📏 @Cursor Rules - Project rules reference
- Γ₆ = 🔄 @Git - Git history reference
- Γ₇ = 📝 @Notepads - Notepad reference
- Γ₈ = 📌 #Files - File context without reference

## 🔐 Permission Symbols (ℙ)
- ℙ = {C: create, R: read, U: update, D: delete} - CRUD permissions
- ℙ(Ω₁) = {R: ✓, C: ✗, U: ✗, D: ✗} - Research mode permissions
- ℙ(Ω₂) = {R: ✓, C: ~, U: ✗, D: ✗} - Innovate mode permissions
- ℙ(Ω₃) = {R: ✓, C: ✓, U: ~, D: ✗} - Plan mode permissions
- ℙ(Ω₄) = {R: ✓, C: ✓, U: ✓, D: ~} - Execute mode permissions
- ℙ(Ω₅) = {R: ✓, C: ✗, U: ✗, D: ✗} - Review mode permissions

## 🔍 Operation Sets (𝕆)
- 𝕆ᵣₑₐₗ = {modify_files, write_code, delete_content, refactor} - Real operations
- 𝕆ᵥᵢᵣₜᵤₐₗ = {suggest_ideas, explore_concepts, evaluate_approaches} - Virtual operations
- 𝕆ₒᵦₛₑᵣᵥₑ = {read_files, analyze_content, identify_patterns} - Observe operations

## 📊 Status Indicators
- ✅ = Complete/Done
- ⏳ = In Progress
- 🔜 = Planned/Upcoming
- ⚠️ = Warning/Risk
- ❌ = Blocked/Failed
- 🟢 = Active context
- 🟡 = Partially relevant context
- 🔴 = Deprecated/removed context
- 🟣 = Essential/core context
- ✓ = Permitted operation
- ✗ = Forbidden operation
- ~ = Conditional/Limited operation

## 🔗 Cross-Reference Notation
- [↗️σ₁:R₁] = Reference to Requirement 1 in projectbrief.md
- [↗️σ₄:T₃] = Reference to Task 3 in activeContext.md
- [↗️σ₆:P₂] = Reference to Protected Region 2 in protection.md
- [↗️σ₁:R₁|Γ₃] = Reference to Requirement 1 with code context
- [↗️σ₄:T₃|Γ₁] = Reference to Task 3 with file context
- [ℙ(Ω₁):read_only] = Reference to Research mode's read-only permission
- [𝕊(Ω₄):𝕆ᵣₑₐₗ] = Reference to Execute mode's real operation permissions

## 🏷️ Common Indexing
- R₁, R₂... = Requirements
- F₁, F₂... = Features
- T₁, T₂... = Tasks
- D₁, D₂... = Decisions
- I₁, I₂... = Issues
- M₁, M₂... = Milestones
- P₁, P₂... = Protected Regions
- C₁, C₂... = Context References
- O₁, O₂... = Operations

## 🧮 Mathematical Operators
- ⟶ = Leads to/Results in
- ∧ = AND (logical)
- ∨ = OR (logical)
- ¬ = NOT (logical)
- ↔ = Bi-directional relationship
- → = One-way relationship/transition
- ∩ = Intersection/overlap
- ∪ = Union/combine
- ∈ = Element of/belongs to
- ∉ = Not an element of

## 💬 Protection Commands
- !cp = Add PROTECTED comment
- !cg = Add GUARDED comment
- !ci = Add INFO comment
- !cd = Add DEBUG comment
- !ct = Add TEST comment
- !cc = Add CRITICAL comment

## 🔍 Context Commands
- !af = @Files (Add file reference)
- !ad = @Folders (Add directory reference)
- !ac = @Code (Add code reference)
- !adoc = @Docs (Add documentation reference)
- !ar = @Cursor Rules (Add rules reference)
- !ag = @Git (Add git reference)
- !an = @Notepads (Add notepad reference)
- !pf = #Files (Pin file to context)

## 🔐 Permission Commands
- !cp = Check permissions for current mode
- !pm = Check if operation is permitted
- !sp = Show permissions for specified mode
- !vm = Verify mode appropriate for operation

---
*Reference guide for symbolic notation used in CursorRIPER Σ framework*