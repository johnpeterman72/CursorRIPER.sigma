# 🔣 CursorRIPER Σ @ Symbol Integration
*v1.0 | Created: 2025-04-10*

## 📎 @ Symbol Notation System

### 🎯 Core @ Symbols (Γ)
- Γ₁ = @Files → 📄 (File reference)
- Γ₂ = @Folders → 📁 (Folder reference)
- Γ₃ = @Code → 💻 (Code reference)
- Γ₄ = @Docs → 📚 (Documentation reference)
- Γ₅ = @Cursor Rules → 📏 (Project rules reference)
- Γ₆ = @Git → 🔄 (Git history reference)
- Γ₇ = @Notepads → 📝 (Notepad reference)
- Γ₈ = #Files → 📌 (File context without reference)

### 🔄 Mode-Symbol Mapping (MΓ)
- MΓ₁ = Ω₁(🔍RESEARCH) ⟶ [Γ₄, Γ₂, Γ₆]
- MΓ₂ = Ω₂(💡INNOVATE) ⟶ [Γ₃, Γ₄, Γ₇]
- MΓ₃ = Ω₃(📝PLAN) ⟶ [Γ₁, Γ₂, Γ₅]
- MΓ₄ = Ω₄(⚙️EXECUTE) ⟶ [Γ₃, Γ₁, Γ₈]
- MΓ₅ = Ω₅(🔎REVIEW) ⟶ [Γ₃, Γ₁, Γ₆]

### 🔗 Symbol Command Shortcuts (SΓ)
- SΓ₁ = !af → @Files (Add file reference)
- SΓ₂ = !ad → @Folders (Add directory reference)
- SΓ₃ = !ac → @Code (Add code reference)
- SΓ₄ = !adoc → @Docs (Add documentation reference)
- SΓ₅ = !ar → @Cursor Rules (Add rules reference)
- SΓ₆ = !ag → @Git (Add git reference)
- SΓ₇ = !an → @Notepads (Add notepad reference)
- SΓ₈ = !pf → #Files (Pin file to context)

### 📈 Protection-Symbol Linking (PΓ)
- PΓ₁ = Ψ₁(PROTECTED) + Γ₃ → 🔒💻 (Protected code)
- PΓ₂ = Ψ₂(GUARDED) + Γ₃ → 🛡️💻 (Guarded code)
- PΓ₃ = Ψ₃(INFO) + Γ₃ → ℹ️💻 (Info-annotated code)
- PΓ₄ = Ψ₄(DEBUG) + Γ₃ → 🐞💻 (Debug code)
- PΓ₅ = Ψ₅(TEST) + Γ₃ → 🧪💻 (Test code)
- PΓ₆ = Ψ₆(CRITICAL) + Γ₃ → ⚠️💻 (Critical code)

### 🔀 Cross-Reference Extensions (CRΓ)
- [↗️σ₁:R₁|Γ₃] = Reference to requirement with code context
- [↗️σ₄:T₃|Γ₁] = Reference to task with file context
- [↗️σ₆:P₂|Γ₄] = Reference to protected region with docs context

### 🧩 @ Memory Integration (σΓ)
- σΓ₁ = σ₄(activeContext.md) + Γ section
- σΓ₂ = activeContext.contextReferences = [Γ₁...Γₙ]
- σΓ₃ = Φ_symbol_persist(Γ₁...Γₙ, 📂) = persist @ references

### 📊 Context Status Indicators (CSΓ)
- 🟢Γ = Active context
- 🟡Γ = Partially relevant context
- 🔴Γ = Deprecated/removed context
- 🟣Γ = Essential/core context

## 🧮 Mathematical Expression System

### 🔢 Context Mathematical Operations
- Γ₁ ∩ Γ₂ = Intersection of file and folder contexts
- Γ₃ ∪ Γ₄ = Union of code and documentation contexts
- Γₙ \ Γₘ = Context difference operation
- Γₙ → Ω₁ = Applying context to Research mode
- Γₙ → Ψₘ = Applying context to Protection level
- Γₙ ⟶ σₘ = Storing context in memory file

### 📐 Context Functions (ΦΓ)
- ΦΓ₁ = expand(Γₙ) ⟶ full context expansion
- ΦΓ₂ = filter(Γₙ, criteria) ⟶ filtered context
- ΦΓ₃ = persist(Γₙ, 📂) ⟶ save context to memory
- ΦΓ₄ = retrieve(Γₙ, 📂) ⟶ load context from memory
- ΦΓ₅ = rank(Γₙ, relevance) ⟶ prioritize context

### 🔄 Context Transition Functions
- Ω₁ → Ω₂ ⟶ MΓ₁ → MΓ₂ (Update context during mode switch)
- Γ₁ → Γ₁' = Context version change
- Ψₙ(Γₘ) ⟶ PΓₙ = Apply protection to context

## 🛠️ Integration Implementation

### 📋 Memory File Updates
```
// Add to activeContext.md template
## 🔮 Context References
- Active Files: [fileA, fileB, ...]
- Active Code: [functionA, classB, ...]
- Active Docs: [docX, docY, ...]
- Context Command: !ac functionA
```

### 📝 Context Persistence
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

### 🔄 Mode Transitions with Context
```
Ω₁ → Ω₂ = {
  backup_context(),
  update_mode(Ω₂),
  apply_default_context(MΓ₂),
  update_file(𝕄[3])
}
```

---
*This notation system integrates Cursor's @ symbol capabilities with CursorRIPER Σ framework*