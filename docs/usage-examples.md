![CursorRIPER♦Σ](../res/github-header-sigma-sm.png)
# 🔍 @ Symbol Usage Examples
*v1.0 | Created: 2025-04-10*

## 🧩 Basic Symbol Usage

### 📄 File References (Γ₁)
```
// In activeContext.md
## 🔮 Context References
- Active Files: [main.js, utils.js, config.json]

// In discussions
I've added the configuration file to our context: 📄config.json
This should match the requirement [↗️σ₁:R₁|📄config.json]
```

### 💻 Code References (Γ₃)
```
// In activeContext.md
## 🔮 Context References
- Active Code: [calculateTotals(), UserClass, validateInput()]

// In discussions
The bug appears to be in the validation function: 💻validateInput()
This implementation satisfies requirement [↗️σ₁:R₄|💻calculateTotals()]
```

### 📚 Documentation References (Γ₄)
```
// In activeContext.md
## 🔮 Context References
- Active Docs: [API Guide, Setup Instructions]

// In discussions
According to our technical documentation: 📚API Guide
This matches our documentation standard [↗️σ₃:D₂|📚Setup Instructions]
```

## 🔄 Mode-Specific Examples

### 🔍 Research Mode (Ω₁) Example
```
// Auto-activated on mode switch
@Mode: RESEARCH (Ω₁) → Context set: [📚Documentation, 📁Project Structure, 🔄Git History]

// Command usage
!adoc API Documentation   // Add documentation reference
!ad src/components/       // Add folder reference
!ag feature/login         // Add git branch reference

// In discussion
Based on our research context (🔍Γ[📚,📁,🔄]), we should examine...
```

### 💡 Innovate Mode (Ω₂) Example
```
// Auto-activated on mode switch
@Mode: INNOVATE (Ω₂) → Context set: [💻Code Elements, 📚Documentation, 📝Notepads]

// Command usage
!ac UserAuthentication    // Add code reference
!adoc Security Guidelines // Add documentation reference
!an AuthIdeas             // Add notepad reference

// In discussion
Considering our innovation context (💡Γ[💻,📚,📝]), we could approach...
```

### ⚙️ Execute Mode (Ω₄) Example
```
// Auto-activated on mode switch
@Mode: EXECUTE (Ω₄) → Context set: [💻Code Elements, 📄Files, 📌Pinned Files]

// Command usage
!ac implementFeature()    // Add code reference
!af src/feature.js        // Add file reference
!pf test/feature.test.js  // Pin test file to context

// In discussion
According to our execution context (⚙️Γ[💻,📄,📌]), we should implement...
```

## 🔗 Advanced Usage Examples

### 🛡️ Protection-Context Integration
```
// Applying protection to code context
🔒💻validateInput() = Ψ₁(PROTECTED) + Γ₃(Code:validateInput())

// In activeContext.md
## 🔮 Protection Context
- Protected: [🔒💻validateInput(), 🔒📄config.json]
- Guarded: [🛡️💻processPayment(), 🛡️📄secrets.js]

// Command usage
!cp validateInput()       // Add protection and code reference
```

### 📊 Context Operations
```
// Context intersection example
Active Files ∩ Protected Files = {config.json}  // Files that are both active and protected

// Context union example
Debug Code ∪ Test Code = {validateInput(), testValidation()}  // Combined context

// Context filtering
ΦΓ₂(🔒💻, "auth") → {authenticateUser(), validateSession()}  // Protected auth code

// Context persistence
ΦΓ₃(Γ₃, 📂) → Updated activeContext.md  // Save code context to memory
```

### 🔀 Cross-Reference Enhancements
```
// Requirement with code implementation reference
[↗️σ₁:R₃|💻implementFeature()] = "Feature implementation satisfying requirement R₃"

// Issue with file context reference
[↗️σ₅:I₂|📄buggy-file.js] = "Issue I₂ related to file buggy-file.js"

// Protected region with documentation reference
[↗️σ₆:P₃|📚Security Guidelines] = "Protected region P₃ with security documentation"
```

## 🧪 Practical Workflow Example

### 🔄 Complete Mode Transition with Context
```
// Current State
@Mode: RESEARCH (Ω₁)
@Context: [📚API Docs, 📁src/auth/, 🔄feature/login]

// Transition command issued
/i  // Switch to INNOVATE mode

// System performs:
1. Σ_backup.create_backup()
2. update_mode(Ω₂)
3. apply_default_context(MΓ₂)
4. update_file(𝕄[3])

// New State
@Mode: INNOVATE (Ω₂)
@Context: [💻AuthService, 📚Security Docs, 📝Auth Ideas]
// Previous context preserved in memory with timestamp
```

### 📝 Context-Aware Planning Example
```
// In plan mode with context
@Mode: PLAN (Ω₃)
@Context: [📄implementation.js, 📁src/feature/, 📏Coding Standards]

// Creating context-aware tasks
## 📋 Implementation Tasks
- T₁: Implement feature [↗️σ₁:R₂|📄implementation.js]
- T₂: Write unit tests [↗️σ₁:R₂|📁src/feature/tests/]
- T₃: Ensure code standards [↗️σ₁:R₂|📏Coding Standards]

// Context tracking in tasks
T₁.context = {📄implementation.js, 💻implementFeature()}
T₂.context = {📁src/feature/tests/, 📄test-utils.js}
T₃.context = {📏Coding Standards, 📚Style Guide}
```

### 🔎 Context-Aware Review Example
```
// In review mode with context
@Mode: REVIEW (Ω₅)
@Context: [💻validateUser(), 📄user-validation.js, 🔄PR#42]

// Review findings with context references
## 🔍 Review Findings
- F₁: Validation incomplete [↗️σ₁:R₅|💻validateUser()]
- F₂: Edge cases not handled [↗️σ₁:R₅|📄user-validation.js]
- F₃: Tests passing [↗️σ₁:R₅|🔄PR#42]

// Context status in review
F₁.context_status = 🟡💻  // Partially relevant context
F₂.context_status = 🟢📄  // Active context
F₃.context_status = 🟣🔄  // Essential context
```

---
*These examples demonstrate real-world usage of the @ symbol notation system within the CursorRIPER Σ framework.*
