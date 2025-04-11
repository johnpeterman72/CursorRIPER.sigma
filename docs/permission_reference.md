![CursorRIPER♦Σ](../res/github-header-sigma-sm.png)
# 🔐 Permission System Quick Reference
*v1.0 | Created: 2025-04-10*

## 📋 Mode Permission Matrix

| Mode | Read | Create | Update | Delete |
|------|------|--------|--------|--------|
| 🔍 RESEARCH (Ω₁) | ✓ | ✗ | ✗ | ✗ |
| 💡 INNOVATE (Ω₂) | ✓ | ~ | ✗ | ✗ |
| 📝 PLAN (Ω₃) | ✓ | ✓ | ~ | ✗ |
| ⚙️ EXECUTE (Ω₄) | ✓ | ✓ | ✓ | ~ |
| 🔎 REVIEW (Ω₅) | ✓ | ✗ | ✗ | ✗ |

## 🔍 Operation Category Permissions

| Mode | Observe | Virtual | Real |
|------|---------|---------|------|
| 🔍 RESEARCH (Ω₁) | ✓ | ~ | ✗ |
| 💡 INNOVATE (Ω₂) | ✓ | ✓ | ✗ |
| 📝 PLAN (Ω₃) | ✓ | ✓ | ~ |
| ⚙️ EXECUTE (Ω₄) | ✓ | ~ | ✓ |
| 🔎 REVIEW (Ω₅) | ✓ | ~ | ✗ |

## 🔣 Legend
- ✓ = Allowed
- ✗ = Forbidden
- ~ = Conditional/Limited

## 📝 Operation Categories
- **Observe Operations (𝕆ₒᵦₛₑᵣᵥₑ)**: read_files, analyze_content, identify_patterns
- **Virtual Operations (𝕆ᵥᵢᵣₜᵤₐₗ)**: suggest_ideas, explore_concepts, evaluate_approaches
- **Real Operations (𝕆ᵣₑₐₗ)**: modify_files, write_code, delete_content, refactor

## 🔄 Mode Commands
- `/r` - Switch to RESEARCH mode (Ω₁)
- `/i` - Switch to INNOVATE mode (Ω₂)
- `/p` - Switch to PLAN mode (Ω₃)
- `/e` - Switch to EXECUTE mode (Ω₄)
- `/rev` - Switch to REVIEW mode (Ω₅)

## ⚠️ Violation Severity Levels
- **CRITICAL**: Real operations in RESEARCH, INNOVATE, or REVIEW modes
- **HIGH**: Real operations in PLAN mode
- **MEDIUM**: Virtual operations in RESEARCH or REVIEW modes
- **LOW**: All other violations

## 🔒 Permission Command Examples
```
!ckp = Check permissions for current mode
!pm <operation> = Check if operation is permitted in current mode
!sp <mode> = Show all permissions for specified mode
!vm <operation> = Verify mode appropriate for operation
```

---
*Quick reference for the permission system in CursorRIPER Σ framework*
