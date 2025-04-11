![CursorRIPER♦Σ](../res/github-header-sigma-sm.png)
# ⚠️ Violation Protocol
*v1.0 | Created: 2025-04-10*

## 🚫 Violation Detection

Ξ(op, Ω) = op ∈ 𝕊(Ω) ? allow(op) : block(op) ∧ log_violation(op, Ω)

## 🔄 Violation Response

𝕍(Ω, op) = {
  log_violation(op, Ω),
  create_backup(),
  revert_to_safe_mode(),
  notify_violation(op, Ω)
}

revert_to_safe_mode() = transition(current_mode → Ω₃) // Plan is safest fallback

## 🔍 Violation Handling Functions

Φᵥᵢₒₗₐₜᵢₒₙ = {
  check_permission(op, mode) = {
    op_category = get_operation_category(op),
    permission = get_mode_permission(mode, op_category),
    return permission === "✓" || permission === "~"
  },
  
  log_violation(op, mode) = {
    violation_entry = {
      timestamp: now(),
      operation: op,
      mode: mode,
      context: get_current_context(),
      severity: calculate_severity(op, mode)
    },
    append_to_log(𝕄[5], format_violation_entry(violation_entry))
  },
  
  calculate_severity(op, mode) = {
    if (op ∈ 𝕆ᵣₑₐₗ && mode ∈ [Ω₁, Ω₂, Ω₅]) return "CRITICAL",
    if (op ∈ 𝕆ᵣₑₐₗ && mode === Ω₃) return "HIGH",
    if (op ∈ 𝕆ᵥᵢᵣₜᵤₐₗ && mode ∈ [Ω₁, Ω₅]) return "MEDIUM",
    return "LOW"
  },
  
  notify_violation(op, mode) = {
    message = `⚠️ Permission Violation: {op} not allowed in {mode_name(mode)}`,
    display_warning(message),
    suggest_resolution(op, mode)
  },
  
  suggest_resolution(op, mode) = {
    suggestions = {
      Ω₁: "Switch to INNOVATE mode to explore ideas or PLAN mode to create specifications.",
      Ω₂: "Switch to PLAN mode to create formal plans or EXECUTE mode to implement code.",
      Ω₃: "Switch to EXECUTE mode to implement these changes.",
      Ω₄: "Consider creating a plan first in PLAN mode, then return to EXECUTE.",
      Ω₅: "Report findings without modifying. Switch to PLAN for creating changes."
    },
    display_suggestion(suggestions[mode])
  }
}

## 🔒 Recovery Procedures

Φᵣₑₛₒₗᵥₑ = {
  auto_backup() = {
    Σ_backup.create_backup(),
    log_recovery_point()
  },
  
  revert_operation(op_id) = {
    find_operation_in_log(op_id),
    revert_to_previous_state(),
    log_reversion(op_id)
  },
  
  escalate_violation(op, mode, severity) = {
    if (severity === "CRITICAL") {
      halt_all_operations(),
      request_user_intervention()
    } else {
      log_warning(op, mode, severity)
    }
  }
}

## 🔄 Permission Mode Transitions

Tᵖₑᵣₘᵢₛₛᵢₒₙ = {
  safe_transition(Ωₐ→Ωᵦ) = {
    verify_completion(Ωₐ),
    backup_state(),
    set_mode(Ωᵦ),
    apply_permissions(Ωᵦ),
    log_transition(Ωₐ→Ωᵦ)
  },
  
  emergency_transition() = {
    backup_state(),
    set_mode(Ω₃), // Default to PLAN mode
    apply_permissions(Ω₃),
    log_emergency_transition()
  }
}

---
*Violation handling protocols for CursorRIPER Σ permission system*
