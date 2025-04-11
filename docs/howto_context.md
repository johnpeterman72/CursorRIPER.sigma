![CursorRIPER♦Σ](../res/github-header-sigma-sm.png)
# 📚 How to Use Context References in CursorRIPER Σ
*v1.0 | Created: 2025-04-10*

This guide provides practical examples of how to use the context reference system in CursorRIPER Σ.

## 📋 Table of Contents
1. [Basic Context References](#basic-context-references)
2. [Working with Mode-Specific Context](#working-with-mode-specific-context)
3. [Context Status Management](#context-status-management)
4. [Cross-References with Context](#cross-references-with-context)
5. [Protection and Context Integration](#protection-and-context-integration)
6. [Context in Memory Files](#context-in-memory-files)
7. [Advanced Context Operations](#advanced-context-operations)

## Basic Context References

### Adding File References
```
// Add a specific file to your context
!af src/main.js

// Add multiple files
!af src/components/Auth.js
!af src/utils/helpers.js

// Reference in discussion
According to the implementation in 📄src/components/Auth.js, we need to...
```

### Adding Code References
```
// Add specific function to context
!ac validateUser()

// Add a class to context
!ac AuthController

// Reference in discussion
The 💻validateUser() function should handle these edge cases...
```

### Adding Documentation References
```
// Add API documentation to context
!adoc API Reference

// Reference in discussion
Based on 📚API Reference, we should implement the endpoint as...
```

### Removing Context References
```
// Remove a reference that's no longer needed
!cr src/components/Auth.js

// Clear all context references
!cc
```

## Working with Mode-Specific Context

### Setting Context for Current Mode
```
// Switch to Research mode
/r

// Apply default context for Research mode (docs, folders, git)
!cm

// Result:
// 📚API Documentation, 📁src/components/, 🔄feature/auth
```

### Mode-Specific Usage Examples

#### Research Mode (Ω₁)
```
/r
!cm
!adoc Security Best Practices
!ad src/auth/
!ag commit:a8f2e3
```

#### Innovate Mode (Ω₂)
```
/i
!cm
!ac AuthProtocol
!adoc OAuth Standards
!an Auth Ideas
```

#### Plan Mode (Ω₃)
```
/p
!cm
!af src/roadmap.md
!ad test/
!ar Coding Standards
```

#### Execute Mode (Ω₄)
```
/e
!cm
!ac implementAuth()
!af src/auth/login.js
!pf test/auth/login.test.js
```

#### Review Mode (Ω₅)
```
/rev
!cm
!ac validateCredentials()
!af src/auth/validation.js
!ag PR#42
```

## Context Status Management

### Setting Context Status
```
// Mark a reference as essential
!cs validateUser() essential

// Mark a reference as partially relevant
!cs helpers.js partially

// Mark a reference as deprecated
!cs oldUtil.js deprecated
```

### Referencing by Status
```
// In discussions
According to the essential context (🟣💻validateUser()), we should...

The partially relevant 🟡📄helpers.js contains utility functions...

We should replace 🔴📄oldUtil.js with the new implementation.
```

## Cross-References with Context

### Basic Cross-References with Context
```
// Reference a requirement with code context
This implementation satisfies [↗️σ₁:R₃|Γ₃:validateUser()]

// Reference a task with file context
According to task [↗️σ₄:T₂|Γ₁:auth.js], we need to...

// Reference a protected region with documentation
The protected region [↗️σ₆:P₁|Γ₄:Security Guide] specifies...
```

### Context-Only References
```
// Direct context reference
The [Γ₃:AuthService] needs to handle these cases...

// With protection level
The [Ψ₁+Γ₃:validateUser()] function is protected and should not...
```

## Protection and Context Integration

### Referencing Protected Code
```
// Protected code reference
The 🔒💻validateUser() function contains critical authentication logic...

// Guarded code reference
The 🛡️💻processPayment() function should only be modified after review...

// Info code reference
The ℹ️💻logActivity() function provides context for debugging...
```

### Combined Protection and Context
```
// Add protected code to context
!ac validateUser()
!cp validateUser()

// Combined reference in discussion
The 🔒💻validateUser() function satisfies requirement [↗️σ₁:R₂|Γ₃]
```

## Context in Memory Files

### Reading Context from Active Context
```
// activeContext.md excerpt:
## 📎 Context References
- 📄 Active Files: [auth.js, config.json]
- 💻 Active Code: [validateUser(), AuthService]
- 📚 Active Docs: [Security Guide]
- 🔄 Git References: [PR#42]

## 📡 Context Status
- 🟢 Active: [auth.js, AuthService]
- 🟣 Essential: [validateUser()]
- 🟡 Partially Relevant: [config.json]
```

### Updating Context via Mode Switching
```
// Current context contains research references
/i
!cm

// Context is updated with innovate-specific references
// Previous context is backed up before replacement
```

## Advanced Context Operations

### Context Intersection
```
// Find overlap between active files and protected files
Let's look at the intersection of 📄 ∩ 🔒 = {auth.js, config.json}
```

### Context Union
```
// Combine debug and test code contexts for testing
We need to consider 🐞💻 ∪ 🧪💻 = {debug(), test(), validate.test()}
```

### Context Filtering
```
// Filter context by criteria
ΦΓ₂(💻, "auth") → {authenticateUser(), validateSession()}

// Context prioritization
ΦΓ₅(📄, "critical") → [auth.js, encryption.js]
```

---

## 🔍 Quick Tips

1. Start with `!cm` after switching modes to get default context
2. Use specific context commands (!af, !ac, etc.) to fine-tune
3. Set status (!cs) for important references
4. Use cross-references with context for traceability
5. Backup context is created automatically on major changes
6. Combine protection and context for security-critical code
7. Use context operations for complex relationships

---
*This guide provides examples for using the context reference system in CursorRIPER Σ*
