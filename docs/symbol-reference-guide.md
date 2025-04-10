# 🔣 CursorRIPER Σ Comprehensive Symbol Reference Guide
*v2.0 | Created: 2025-04-10*

## 📁 File Symbols

| Symbol | Description |
|--------|-------------|
| 📂     | /memory-bank/ |
| 📦     | /memory-bank/backups/ |
| σ₁     | projectbrief.md |
| σ₂     | systemPatterns.md |
| σ₃     | techContext.md |
| σ₄     | activeContext.md |
| σ₅     | progress.md |
| σ₆     | protection.md |

## 🔄 Mode & Phase Symbols

| Symbol | Emoji | Description |
|--------|-------|-------------|
| Ω₁     | 🔍    | RESEARCH mode |
| Ω₂     | 💡    | INNOVATE mode |
| Ω₃     | 📝    | PLAN mode |
| Ω₄     | ⚙️    | EXECUTE mode |
| Ω₅     | 🔎    | REVIEW mode |
| Π₁     | 🌱    | UNINITIATED phase |
| Π₂     | 🚧    | INITIALIZING phase |
| Π₃     | 🏗️    | DEVELOPMENT phase |
| Π₄     | 🔧    | MAINTENANCE phase |

## 🛡️ Protection Symbols (Ψ)

| Symbol | Description |
|--------|-------------|
| Ψ₁     | PROTECTED - Do not modify |
| Ψ₂     | GUARDED - Ask before modifying |
| Ψ₃     | INFO - Context note |
| Ψ₄     | DEBUG - Debugging code |
| Ψ₅     | TEST - Testing code |
| Ψ₆     | CRITICAL - Business logic |

## 📎 Context Symbols (Γ)

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

## 🔐 Permission Symbols (ℙ)

| Symbol | Description |
|--------|-------------|
| ℙ | {C: create, R: read, U: update, D: delete} - CRUD permissions |
| ℙ(Ω₁) | {R: ✓, C: ✗, U: ✗, D: ✗} - Research mode permissions |
| ℙ(Ω₂) | {R: ✓, C: ~, U: ✗, D: ✗} - Innovate mode permissions |
| ℙ(Ω₃) | {R: ✓, C: ✓, U: ~, D: ✗} - Plan mode permissions |
| ℙ(Ω₄) | {R: ✓, C: ✓, U: ✓, D: ~} - Execute mode permissions |
| ℙ(Ω₅) | {R: ✓, C: ✗, U: ✗, D: ✗} - Review mode permissions |

## 🔍 Operation Sets (𝕆)

| Symbol | Description |
|--------|-------------|
| 𝕆ᵣₑₐₗ | {modify_files, write_code, delete_content, refactor} - Real operations |
| 𝕆ᵥᵢᵣₜᵤₐₗ | {suggest_ideas, explore_concepts, evaluate_approaches} - Virtual operations |
| 𝕆ₒᵦₛₑᵣᵥₑ | {read_files, analyze_content, identify_patterns} - Observe operations |

## 📊 Status Indicators

| Symbol | Description |
|--------|-------------|
| ✅ | Complete/Done |
| ⏳ | In Progress |
| 🔜 | Planned/Upcoming |
| ⚠️ | Warning/Risk |
| ❌ | Blocked/Failed |
| 🟢 | Active context |
| 🟡 | Partially relevant context |
| 🔴 | Deprecated/removed context |
| 🟣 | Essential/core context |
| ✓ | Permitted operation |
| ✗ | Forbidden operation |
| ~ | Conditional/Limited operation |

## 🏷️ Common Indexing

| Pattern | Description |
|---------|-------------|
| R₁, R₂... | Requirements |
| F₁, F₂... | Features |
| T₁, T₂... | Tasks |
| D₁, D₂... | Decisions |
| I₁, I₂... | Issues |
| M₁, M₂... | Milestones |
| P₁, P₂... | Protected Regions |
| C₁, C₂... | Context References |
| O₁, O₂... | Operations |

## 🧮 Mathematical Operators

| Symbol | Description |
|--------|-------------|
| ⟶ | Leads to/Results in |
| ∧ | AND (logical) |
| ∨ | OR (logical) |
| ¬ | NOT (logical) |
| ↔ | Bi-directional relationship |
| → | One-way relationship/transition |
| ∩ | Intersection/overlap |
| ∪ | Union/combine |
| ∈ | Element of/belongs to |
| ∉ | Not an element of |

## 🛠️ Protection Commands

| Command | Description |
|---------|-------------|
| !cp | Add PROTECTED comment |
| !cg | Add GUARDED comment |
| !ci | Add INFO comment |
| !cd | Add DEBUG comment |
| !ct | Add TEST comment |
| !cc | Add CRITICAL comment |

## 🔍 Context Commands

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

## 🔐 Permission Commands

| Command | Description |
|---------|-------------|
| !ckp | Check permissions for current mode |
| !pm | Check if operation is permitted |
| !sp | Show permissions for specified mode |
| !vm | Verify mode appropriate for operation |

**Note:** The permission command "!ckp" (Check permissions) was previously documented as "!cp" which caused a conflict with the protection command "!cp" (Add PROTECTED comment). This has been corrected.

## 🔄 Mode-Context Mapping

| Mode | Symbol | Default Context | Description |
|------|--------|----------------|-------------|
| RESEARCH | 🔍 Ω₁ | [Γ₄, Γ₂, Γ₆] | Docs, Folders, Git |
| INNOVATE | 💡 Ω₂ | [Γ₃, Γ₄, Γ₇] | Code, Docs, Notepads |
| PLAN | 📝 Ω₃ | [Γ₁, Γ₂, Γ₅] | Files, Folders, Rules |
| EXECUTE | ⚙️ Ω₄ | [Γ₃, Γ₁, Γ₈] | Code, Files, Pinned Files |
| REVIEW | 🔎 Ω₅ | [Γ₃, Γ₁, Γ₆] | Code, Files, Git |

## 🔗 Cross-Reference Notation

| Reference Type | Syntax | Example | Description |
|----------------|--------|---------|-------------|
| Standard | [↗️σₙ:Xᵢ] | [↗️σ₁:R₁] | Reference to item in memory file |
| With Context | [↗️σₙ:Xᵢ\|Γₘ] | [↗️σ₁:R₁\|Γ₃] | Reference with context |
| Context-only | [Γₙ:item] | [Γ₃:validate()] | Direct context reference |
| Protection+Context | [Ψₙ+Γₘ:item] | [Ψ₁+Γ₃:auth()] | Protected context reference |
| Permission | [ℙ(Ω₁):read_only] | [ℙ(Ω₁):read_only] | Reference to mode permissions |
| Operation Set | [𝕊(Ω₄):𝕆ᵣₑₐₗ] | [𝕊(Ω₄):𝕆ᵣₑₐₗ] | Reference to mode operations |

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
| Difference | Γₙ \ Γₘ | Context difference operation |
| Apply to Mode | Γₙ → Ωₘ | Applying context to mode |
| Apply to Protection | Γₙ → Ψₘ | Applying context to Protection level |
| Store in Memory | Γₙ ⟶ σₘ | Storing context in memory file |

## 📐 Context Functions (ΦΓ)

| Function | Syntax | Description |
|----------|--------|-------------|
| ΦΓ₁ | expand(Γₙ) | Full context expansion |
| ΦΓ₂ | filter(Γₙ, criteria) | Filtered context |
| ΦΓ₃ | persist(Γₙ, 📂) | Save context to memory |
| ΦΓ₄ | retrieve(Γₙ, 📂) | Load context from memory |
| ΦΓ₅ | rank(Γₙ, relevance) | Prioritize context |

## 🔄 Context Transition Functions

| Transition | Syntax | Description |
|------------|--------|-------------|
| Mode transition | Ω₁ → Ω₂ ⟶ MΓ₁ → MΓ₂ | Update context during mode switch |
| Version change | Γ₁ → Γ₁' | Context version change |
| Apply protection | Ψₙ(Γₘ) ⟶ PΓₙ | Apply protection to context |

## 🧩 @ Memory Integration (σΓ)

| Integration | Description |
|-------------|-------------|
| σΓ₁ | activeContext.md + Γ section |
| σΓ₂ | activeContext.contextReferences = [Γ₁...Γₙ] |
| σΓ₃ | Φ_symbol_persist(Γ₁...Γₙ, 📂) = persist @ references |

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

// Apply context persistence
ΦΓ₃(Γ₃, 📂) // Save code context to memory

// Filter context by criteria
ΦΓ₂(Γ₃, "validate") // Filter code context for validation functions

// Check permissions for current mode
!cp

// Verify if operation is permitted in current mode
!pm modify_files
```

## 📋 Implementation Examples

### Memory File Updates Integration
```
// Add to activeContext.md template
## 🔮 Context References
- Active Files: [fileA, fileB, ...]
- Active Code: [functionA, classB, ...]
- Active Docs: [docX, docY, ...]
- Context Command: !ac functionA
```

### Context Persistence Implementation
```
Φ_context = {
  active_references: [],
  add_reference(type, name) = {
    active_references.push({type, name, added: now()})
    update_file(𝕄[3], format(active_references))
  },
  clear_references() = {
    active_references = []
    update_file(𝕄[3], "")
  }
}
```

### Mode Transitions with Context Implementation
```
Ω₁ → Ω₂ = {
  backup_context(),
  update_mode(Ω₂),
  apply_default_context(MΓ₂),
  update_file(𝕄[3])
}
```

## 🔢 Indexing Array (𝕋)

| Index | Function | Description |
|-------|----------|-------------|
| 𝕋[0] | read_files | Read and analyze project files |
| 𝕋[1] | ask_questions | Ask questions about project requirements |
| 𝕋[2] | observe_code | Observe and understand existing code |
| 𝕋[3] | document_findings | Document research findings |
| 𝕋[4] | suggest_ideas | Suggest innovative ideas |
| 𝕋[5] | explore_options | Explore potential approaches |
| 𝕋[6] | evaluate_approaches | Evaluate different approaches |
| 𝕋[7] | create_plan | Create project implementation plan |
| 𝕋[8] | detail_specifications | Detail technical specifications |
| 𝕋[9] | sequence_steps | Create step sequence for implementation |
| 𝕋[10] | implement_code | Implement code according to plan |
| 𝕋[11] | follow_plan | Follow the implementation plan |
| 𝕋[12] | test_implementation | Test the implemented solution |
| 𝕋[13] | validate_output | Validate output against requirements |
| 𝕋[14] | verify_against_plan | Verify implementation against plan |
| 𝕋[15] | report_deviations | Report any deviations from plan |

### Mode-Function Mapping

| Mode | Active Functions | Inactive Functions | Description |
|------|------------------|-------------------|-------------|
| 🔍 RESEARCH (Ω₁) | +𝕋[0:3] | -𝕋[4:15] | Use research functions only |
| 💡 INNOVATE (Ω₂) | +𝕋[4:6] | -𝕋[8:15] | Use ideation functions only |
| 📝 PLAN (Ω₃) | +𝕋[7:9] | -𝕋[10:15] | Use planning functions only |
| ⚙️ EXECUTE (Ω₄) | +𝕋[10:12] | -[improve,create,deviate] | Use implementation functions only |
| 🔎 REVIEW (Ω₅) | +𝕋[13:15] | -[modify,improve] | Use review functions only |

### Function Activation Syntax

```
// Examples of function activation rules:
+𝕋[0:3] = Activate functions 0, 1, 2, 3
-𝕋[4:15] = Deactivate functions 4 through 15
+𝕋[7] = Activate function 7 only
-[improve,create,deviate] = Deactivate specific operations
```

---
*This comprehensive reference guide consolidates all symbolic notation for the CursorRIPER Σ framework*