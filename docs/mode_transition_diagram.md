![CursorRIPER♦Σ](../res/github-header-sigma-sm.png)
# 🔄 Mode Transition Diagram
*v1.0 | Created: 2025-04-10*

## 📊 Mode Transitions with Permission Enforcement

```
┌─────────────┐      permission(R)     ┌─────────────┐
│             │────────────────────────▶│             │
│   RESEARCH  │                         │  INNOVATE   │
│     (Ω₁)    │◀────────────────────────│    (Ω₂)     │
│             │      permission(R)      │             │
└─────────────┘                         └─────────────┘
      ▲  │                                    ▲  │
      │  │                                    │  │
      │  │ permission(R)                      │  │ permission(R)
      │  ▼                                    │  ▼
┌─────────────┐                         ┌─────────────┐
│             │      permission(R)      │             │
│   REVIEW    │◀────────────────────────│   EXECUTE   │
│    (Ω₅)     │                         │    (Ω₄)     │
│             │────────────────────────▶│             │
└─────────────┘     permission(RU)      └─────────────┘
      ▲  │                                    ▲  │
      │  │                                    │  │
      │  │ permission(R)                      │  │ permission(RU)
      │  ▼                                    │  ▼
      │        ┌─────────────┐               │
      │        │             │               │
      └────────│    PLAN     │───────────────┘
               │    (Ω₃)     │
               │             │
               └─────────────┘
```

## 🔐 Permission Enforcement at Transition

Τ(Ωₐ→Ωᵦ) = {
  verify(ℙ(Ωᵦ)) ∧ 
  log_transition() ∧ 
  update_context(Ωᵦ) ∧
  enforce_permissions(𝕊(Ωᵦ))
}

## 📝 Transition Rules

1. **Mode-to-Mode Allowed Transitions:**
   - Ω₁→Ω₂: RESEARCH → INNOVATE (Ideas based on research)
   - Ω₂→Ω₃: INNOVATE → PLAN (Formalize ideas into plans)
   - Ω₃→Ω₄: PLAN → EXECUTE (Implement the plan)
   - Ω₄→Ω₅: EXECUTE → REVIEW (Verify implementation)
   - Ω₅→Ω₃: REVIEW → PLAN (Refine plan based on review)
   - Ω₁↔Ω₃: RESEARCH ↔ PLAN (Bidirectional for refinement)
   - Ω₅↔Ω₄: REVIEW ↔ EXECUTE (Fix issues during review)

2. **Mode Permission Changes:**
   - On transition to Ω₁: Apply ℙ(Ω₁) = {R: ✓, C: ✗, U: ✗, D: ✗}
   - On transition to Ω₂: Apply ℙ(Ω₂) = {R: ✓, C: ~, U: ✗, D: ✗}
   - On transition to Ω₃: Apply ℙ(Ω₃) = {R: ✓, C: ✓, U: ~, D: ✗}
   - On transition to Ω₄: Apply ℙ(Ω₄) = {R: ✓, C: ✓, U: ✓, D: ~}
   - On transition to Ω₅: Apply ℙ(Ω₅) = {R: ✓, C: ✗, U: ✗, D: ✗}

3. **Safe Transition Protocol:**
   ```
   transition(Ωₐ→Ωᵦ) = {
     backup_state(),
     verify_completion(Ωₐ),
     set_mode(Ωᵦ),
     apply_permissions(ℙ(Ωᵦ)),
     update_context(MΓ[Ωᵦ]),
     log_transition(Ωₐ→Ωᵦ)
   }
   ```

## ⚠️ Violation Recovery Transitions

```
      ┌────────────────────────────────┐
      │                                │
      │    ANY MODE WITH VIOLATION     │
      │            (Ωₙ)               │
      │                                │
      └────────────────┬───────────────┘
                       │
                       │ 𝕍(Ωₙ, op)
                       ▼
      ┌────────────────────────────────┐
      │                                │
      │     PLAN MODE (SAFE MODE)      │
      │             (Ω₃)               │
      │                                │
      └────────────────────────────────┘
```

---
*Mode transition diagram with permission enforcement for CursorRIPER Σ framework*
