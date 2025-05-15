![CursorRIPER♦Σ](../res/github-header-sigma-sm.png)
# CursorRIPER♦Σ 1.0.4 Array Reference

This document provides a comprehensive reference for all arrays used in the CursorRIPER♦Σ 1.0.4 framework. Arrays are fundamental organizing structures that help categorize, map, and relate different elements of the framework.

## 📚 Core Arrays

### 𝕋: Task Operations Array
Tasks and operations available to Claude, indexed from 0-15:
```
𝕋 = [read_files, ask_questions, observe_code, document_findings,
     suggest_ideas, explore_options, evaluate_approaches,
     create_plan, detail_specifications, sequence_steps,
     implement_code, follow_plan, test_implementation,
     validate_output, verify_against_plan, report_deviations]
```
- **Purpose**: Defines what operations Claude can perform in each mode
- **Usage**: Referenced by mode definitions (Ω) to specify allowed/forbidden operations
- **Indexing**: Used with array slicing notation, e.g., +𝕋[0:3] enables first 4 operations

### 𝕄: Memory Files Array
Core memory files that store project information:
```
𝕄 = [📂projectbrief.md, 📂systemPatterns.md, 
     📂techContext.md, 📂activeContext.md, 
     📂progress.md, 📂protection.md]
```
- **Purpose**: Defines the memory bank files for persistent storage
- **Usage**: Referenced throughout the framework for file operations
- **Indexing**: 𝕄[0] is projectbrief.md, 𝕄[1] is systemPatterns.md, etc.

### Ψ: Protection Levels Array
Code protection levels from most to least restrictive:
```
Ψ = [PROTECTED, GUARDED, INFO, DEBUG, TEST, CRITICAL]
```
- **Purpose**: Defines the available protection levels for code sections
- **Usage**: Used by the code protection system to mark and enforce protection
- **Indexing**: Ψ[0] is PROTECTED, Ψ[1] is GUARDED, etc.

### Ψ₊: Protection End Markers Array
End markers corresponding to each protection level:
```
Ψ₊ = [END-P, END-G, END-I, END-D, END-T, END-C]
```
- **Purpose**: Defines the end markers that close protected code sections
- **Usage**: Paired with protection levels to clearly mark section boundaries
- **Indexing**: Ψ₊[0] is END-P (ends PROTECTED sections), etc.

### ℜ: Reference Map
Structured map of protection references and their attributes:
```
ℜ = {
  Ψ: { // Protection
    1: {s: "PROTECTED", e: "END-P", h: "!cp"},
    2: {s: "GUARDED", e: "END-G", h: "!cg"},
    3: {s: "INFO", e: "END-I", h: "!ci"},
    4: {s: "DEBUG", e: "END-D", h: "!cd"},
    5: {s: "TEST", e: "END-T", h: "!ct"},
    6: {s: "CRITICAL", e: "END-C", h: "!cc"}
  }
}
```
- **Purpose**: Maps protection levels to their start markers, end markers, and command shortcuts
- **Usage**: Used for consistent reference across protection system components
- **Structure**: Hierarchical map with numeral keys and attribute objects

## 📎 Context Arrays

### Γ: Context Types Array
Types of context references available in the framework:
```
Γ = [FILES, FOLDERS, CODE, DOCS, RULES, GIT, NOTEPADS, PINNED]
```
- **Purpose**: Defines the types of context that can be referenced
- **Usage**: Used to categorize and manage context references
- **Indexing**: Γ[0] is FILES, Γ[1] is FOLDERS, etc.

### Γ_symbols: Context Symbols Map
Maps context types to their emoji symbols and Cursor @-references:
```
Γ_symbols = {
  Γ₁: 📄 @Files,
  Γ₂: 📁 @Folders,
  Γ₃: 💻 @Code,
  Γ₄: 📚 @Docs,
  Γ₅: 📏 @Cursor Rules,
  Γ₆: 🔄 @Git,
  Γ₇: 📝 @Notepads,
  Γ₈: 📌 #Files
}
```
- **Purpose**: Provides visual symbols and Cursor integration for context types
- **Usage**: Used in UI representation and integration with Cursor's context system
- **Structure**: Maps subscripted Γ symbols to emoji and @-references

### MΓ: Mode-Context Mapping Array
Maps RIPER modes to their default context types:
```
MΓ = {
  Ω₁: [Γ₄, Γ₂, Γ₆],  // RESEARCH: docs, folders, git
  Ω₂: [Γ₃, Γ₄, Γ₇],  // INNOVATE: code, docs, notepads
  Ω₃: [Γ₁, Γ₂, Γ₅],  // PLAN: files, folders, rules
  Ω₄: [Γ₃, Γ₁, Γ₈],  // EXECUTE: code, files, pinned
  Ω₅: [Γ₃, Γ₁, Γ₆]   // REVIEW: code, files, git
}
```
- **Purpose**: Defines which context types are most relevant for each mode
- **Usage**: Used when switching modes to update active context
- **Structure**: Maps mode symbols (Ω) to arrays of context type symbols (Γ)

## 🔐 Permission Arrays

### 𝕆ᵣₑₐₗ: Real Operations Array
Operations that modify the actual codebase:
```
𝕆ᵣₑₐₗ = {modify_files, write_code, delete_content, refactor}
```
- **Purpose**: Defines operations that make real changes to code
- **Usage**: Used by permission system to enforce operation restrictions
- **Permissions**: Most restricted operations, requiring Execute mode

### 𝕆ᵥᵢᵣₜᵤₐₗ: Virtual Operations Array
Operations that only conceptualize or plan changes:
```
𝕆ᵥᵢᵣₜᵤₐₗ = {suggest_ideas, explore_concepts, evaluate_approaches}
```
- **Purpose**: Defines operations that only work with concepts, not real code
- **Usage**: Used by permission system for Innovate and Plan modes
- **Permissions**: Intermediate restriction level

### 𝕆ₒᵦₛₑᵣᵥₑ: Observe Operations Array
Operations that only read or analyze existing content:
```
𝕆ₒᵦₛₑᵣᵥₑ = {read_files, analyze_content, identify_patterns}
```
- **Purpose**: Defines operations that only observe but don't modify
- **Usage**: Used by permission system for Research and Review modes
- **Permissions**: Least restricted operations, allowed in all modes

### 𝕊: Mode-Specific Operation Sets
Defines which operation types are allowed in each mode:
```
𝕊(Ω₁) = {𝕆ₒᵦₛₑᵣᵥₑ: ✓, 𝕆ᵥᵢᵣₜᵤₐₗ: ~, 𝕆ᵣₑₐₗ: ✗} // Research
𝕊(Ω₂) = {𝕆ₒᵦₛₑᵣᵥₑ: ✓, 𝕆ᵥᵢᵣₜᵤₐₗ: ✓, 𝕆ᵣₑₐₗ: ✗} // Innovate
𝕊(Ω₃) = {𝕆ₒᵦₛₑᵣᵥₑ: ✓, 𝕆ᵥᵢᵣₜᵤₐₗ: ✓, 𝕆ᵣₑₐₗ: ~} // Plan
𝕊(Ω₄) = {𝕆ₒᵦₛₑᵣᵥₑ: ✓, 𝕆ᵥᵢᵣₜᵤₐₗ: ~, 𝕆ᵣₑₐₗ: ✓} // Execute
𝕊(Ω₅) = {𝕆ₒᵦₛₑᵣᵥₑ: ✓, 𝕆ᵥᵢᵣₜᵤₐₗ: ~, 𝕆ᵣₑₐₗ: ✗} // Review
```
- **Purpose**: Defines permission matrices for each mode
- **Usage**: Used by the permission enforcement system
- **Structure**: Maps mode symbols (Ω) to permission objects
- **Values**: ✓ (allowed), ~ (partially allowed), ✗ (forbidden)

## 🔄 Integration Arrays

### PΓ: Protection-Context Integration
Maps combinations of protection levels and context types:
```
PΓ = {
  Ψ₁ + Γ₃: 🔒💻,  // Protected code
  Ψ₂ + Γ₃: 🛡️💻,  // Guarded code
  Ψ₃ + Γ₃: ℹ️💻,   // Info code
  Ψ₄ + Γ₃: 🐞💻,  // Debug code
  Ψ₅ + Γ₃: 🧪💻,  // Test code
  Ψ₆ + Γ₃: ⚠️💻   // Critical code
}
```
- **Purpose**: Provides visual representations for protected code contexts
- **Usage**: Used for referencing protected code regions in context
- **Structure**: Maps combinations to composite emoji representations

### ℙΓ: Permission-Context Integration
Maps combinations of permissions and context types:
```
ℙΓ = {
  ℙ(Ω₁) + Γ₁: 📄🔍, // Research file context
  ℙ(Ω₂) + Γ₃: 💻💡, // Innovate code context
  ℙ(Ω₃) + Γ₂: 📁📝, // Plan folder context
  ℙ(Ω₄) + Γ₃: 💻⚙️, // Execute code context
  ℙ(Ω₅) + Γ₁: 📄🔎  // Review file context
}
```
- **Purpose**: Provides visual representations for mode-specific contexts
- **Usage**: Used for referencing contexts with permission considerations
- **Structure**: Maps combinations to composite emoji representations

## 🧰 Memory and Project Arrays

### Π: Project Phases Array
The four phases of a project lifecycle:
```
Π₁ = 🌱UNINITIATED ⟶ framework_installed ∧ ¬project_started
Π₂ = 🚧INITIALIZING ⟶ START_active ∧ setup_ongoing  
Π₃ = 🏗️DEVELOPMENT ⟶ main_development ∧ RIPER_active
Π₄ = 🔧MAINTENANCE ⟶ long_term_support ∧ RIPER_active
```
- **Purpose**: Defines the project lifecycle phases
- **Usage**: Used to track and manage the project's current state
- **Structure**: Maps phase symbols (Π with subscripts) to phase definitions

### Π_transitions: Project Phase Transitions
Defines how phases transition:
```
Π_transitions = {
  Π₁→Π₂: 🔄"/start",
  Π₂→Π₃: ✅completion(START_phase),
  Π₃↔Π₄: 🔄user_request
}
```
- **Purpose**: Defines what triggers transitions between project phases
- **Usage**: Used to manage phase changes in the project lifecycle
- **Structure**: Maps transition arrows to triggers/commands

### Σ_memory: Memory System Map
Organizes memory components and their relationships:
```
Σ_memory = {
  σ₁ = 📋𝕄[0] ⟶ requirements ∧ scope ∧ criteria,
  σ₂ = 🏛️𝕄[1] ⟶ architecture ∧ components ∧ decisions,
  σ₃ = 💻𝕄[2] ⟶ stack ∧ environment ∧ dependencies,
  σ₄ = 🔮𝕄[3] ⟶ focus ∧ changes ∧ next_steps ∧ context_references,
  σ₅ = 📊𝕄[4] ⟶ status ∧ milestones ∧ issues,
  σ₆ = 🛡️𝕄[5] ⟶ protected_regions ∧ history ∧ approvals ∧ violations
}
```
- **Purpose**: Maps memory files to their content and purpose
- **Usage**: Used throughout the framework to access specific memory components
- **Structure**: Maps Greek sigma symbols with subscripts to file associations and content types

### S₁₋₆: START Phase Steps Array
The six steps of the START phase (part of Π₂):
```
S₁₋₆ = [requirements, technology, architecture, scaffolding, environment, memory]
```
- **Purpose**: Defines the steps to complete during initialization
- **Usage**: Used during Π₂ (INITIALIZING) phase to guide setup
- **Indexing**: S₁ is requirements, S₂ is technology, etc.

### START_process: START Phase Process Map
Detailed process steps for initialization:
```
START_process = {
  S₀: create_directory(📂),
  S₁: gather(requirements) ⟶ create(𝕄[0]),
  S₂: select(technologies) ⟶ update(𝕄[2]),
  S₃: define(architecture) ⟶ create(𝕄[1]),
  S₄: scaffold(project) ⟶ create(directories),
  S₅: setup(environment) ⟶ update(𝕄[2]),
  S₆: initialize(memory) ⟶ create(𝕄[0:5])
}
```
- **Purpose**: Defines the detailed actions for each START phase step
- **Usage**: Used during Π₂ (INITIALIZING) phase as step-by-step guide
- **Structure**: Maps process step symbols to sequences of actions

## 🔍 Command and Utility Arrays

### Φ_context_commands: Context Commands Map
Context-related command shortcuts:
```
Φ_context_commands = {
  !af(file) = Σ_context.add_reference(Γ₁, file),             // Add file reference
  !ad(folder) = Σ_context.add_reference(Γ₂, folder),         // Add folder reference
  !ac(code) = Σ_context.add_reference(Γ₃, code),             // Add code reference
  !adoc(doc) = Σ_context.add_reference(Γ₄, doc),             // Add documentation reference
  !ar(rule) = Σ_context.add_reference(Γ₅, rule),             // Add rule reference
  !ag(git) = Σ_context.add_reference(Γ₆, git),               // Add git reference
  !an(notepad) = Σ_context.add_reference(Γ₇, notepad),       // Add notepad reference
  !pf(file) = Σ_context.add_reference(Γ₈, file),             // Pin file to context
  !cs(ref, status) = Σ_context.set_status(ref, status),      // Set context status
  !cr(ref) = Σ_context.remove_reference(ref),                // Remove context reference
  !cc = Σ_context.clear_references(),                        // Clear all context references
  !cm = Σ_context.context_for_mode(current_mode)             // Set context for current mode
}
```
- **Purpose**: Defines command shortcuts for context operations
- **Usage**: Used to quickly add/manage context references
- **Structure**: Maps commands to context functions and parameters

### Φ_permission_commands: Permission Commands Map
Permission-related command shortcuts:
```
Φ_permission_commands = {
  !ckp = show_current_permissions(),                           // Check permissions for current mode
  !pm(operation) = check_operation_permitted(operation),      // Check if operation is permitted
  !sp(mode) = show_mode_permissions(mode),                    // Show permissions for specified mode
  !vm(operation) = suggest_appropriate_mode(operation)        // Verify mode appropriate for operation
}
```
- **Purpose**: Defines command shortcuts for permission operations
- **Usage**: Used to check and verify permissions
- **Structure**: Maps commands to permission functions and parameters

### Δ: Safety Protocols Array
Defines safety protocols for various operations:
```
Δ = {
  1: destructive_op(x) ⟶ warn ∧ confirm ∧ Σ_backup.create_backup(),
  2: phase_transition(x) ⟶ verify ∧ Σ_backup.create_backup() ∧ update,
  3: permission_violation(op) ⟶ 𝕍(op, current_mode),
  4: error(x) ⟶ report("Framework issue: " + x) ∧ suggest_recovery(x),
  5: context_change() ⟶ Σ_backup.backup_context() ∧ update_context_references()
}
```
- **Purpose**: Defines safety protocols for various operations
- **Usage**: Used throughout the framework to ensure safe operations
- **Structure**: Maps protocol numbers to safety sequences

## 📄 Template Arrays

### Σ_templates: Memory Templates Map
Template structures for memory files:
```
Σ_templates = {
  σ₁: """# σ₁: Project Brief\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*Π: {PHASE} | Ω: {MODE}*\n\n## 🏆 Overview\n[Project description]\n\n## 📋 Requirements\n- [R₁] [Requirement 1]\n...""",
  
  σ₂: """# σ₂: System Patterns\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*Π: {PHASE} | Ω: {MODE}*\n\n## 🏛️ Architecture Overview\n[Architecture description]\n...""",
  
  // Additional templates...
}
```
- **Purpose**: Provides template structures for memory files
- **Usage**: Used when initializing or resetting memory files
- **Structure**: Maps memory file symbols to template strings

### χ_refs: Extended Cross-References
Template formats for cross-referencing:
```
χ_refs = {
  standard: "[↗️σ₁:R₁]",  // Standard cross-reference
  with_context: "[↗️σ₁:R₁|Γ₃]",  // Cross-reference with context
  context_only: "[Γ₃:ClassA]",  // Context reference
  protection_context: "[Ψ₁+Γ₃:validate()]",  // Protection with context
  permission_context: "[ℙ(Ω₁):read_only]"  // Permission reference
}
```
- **Purpose**: Provides template formats for cross-referencing
- **Usage**: Used to create consistent cross-references across the framework
- **Structure**: Maps reference types to template strings

## 🔄 Relations Between Arrays

The CursorRIPER♦Σ framework uses a sophisticated system of interrelated arrays that work together to create a comprehensive environment:

1. **Mode-Based Relations**:
   - 𝕋 → Ω₁₋₅: Defines tasks allowed in each mode
   - MΓ → Ω₁₋₅: Defines context types for each mode
   - 𝕊 → Ω₁₋₅: Defines operation permissions for each mode

2. **Permission Hierarchies**:
   - 𝕆ᵣₑₐₗ → 𝕆ᵥᵢᵣₜᵤₐₗ → 𝕆ₒᵦₛₑᵣᵥₑ: Increasingly restricted operations
   - Ω₅ → Ω₁ → Ω₂ → Ω₃ → Ω₄: Increasingly permissive modes

3. **Context Integration**:
   - Γ → Γ_symbols → MΓ: Context types to symbols to mode mappings
   - Γ → PΓ: Context types combined with protection
   - Γ → ℙΓ: Context types combined with permissions

4. **Memory Structure**:
   - 𝕄 → Σ_memory → Σ_templates: Memory files to organized structure to templates
   - 𝕄 → S₁₋₆ → START_process: Memory files affected by START process

5. **Protection System**:
   - Ψ → Ψ₊ → ℜ: Protection levels to end markers to reference map
   - Ψ → PΓ: Protection levels combined with context

This interconnected system creates a robust framework where all components are related and integrated, providing a comprehensive environment for AI-assisted development with clear boundaries, permissions, and context awareness.
