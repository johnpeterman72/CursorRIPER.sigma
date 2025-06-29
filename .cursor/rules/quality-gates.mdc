# 🚦 Quality Gates for CursorRIPER Σ
# Symbol: Κ (Kappa)
# Version: 1.0.0

## 📋 Gate System Definition
```
service = "Enterprise Quality Gate System"
symbol = "Κ"
enforcement = "Sequential gate progression with approvals"
```

## 🎯 Gate Definitions
```
Κ = {
  Κ₁: {
    name: "PRD Approval Gate",
    phase: "Requirements",
    blockers: {
      prd_completeness: 100%,
      objectives_clear: validated(Ρ₁),
      requirements_complete: validated(Ρ₂),
      stories_estimated: all(Ρ₄.estimation > 0),
      acceptance_defined: all(Ρ₅.criteria.length > 0)
    },
    approvers: [Β₁],
    artifacts_required: [
      "Complete PRD document",
      "User story backlog",
      "Success metrics defined"
    ],
    next: Κ₂,
    rollback: draft_state
  },
  
  Κ₂: {
    name: "Design Review Gate",
    phase: "Architecture",
    blockers: {
      architecture_documented: exists(tech_spec),
      api_contracts_defined: validated(api_spec),
      security_review_passed: security_score > 80,
      performance_targets_set: defined(sla_metrics),
      database_design_complete: exists(data_model)
    },
    approvers: [Β₂],
    artifacts_required: [
      "Technical specification",
      "Architecture diagrams",
      "API documentation",
      "Security assessment"
    ],
    next: Κ₃,
    rollback: Κ₁
  },
  
  Κ₃: {
    name: "Code Review Gate",
    phase: "Implementation",
    blockers: {
      tests_passing: test_suite.pass_rate === 100%,
      coverage_threshold: code_coverage > 80%,
      linting_passed: lint_errors === 0,
      no_security_vulnerabilities: security_scan.critical === 0,
      documentation_complete: api_docs_generated()
    },
    approvers: [Β₃, Β₄],
    artifacts_required: [
      "Source code",
      "Unit tests",
      "Integration tests",
      "Code documentation"
    ],
    next: Κ₄,
    rollback: development_branch
  },
  
  Κ₄: {
    name: "QA Signoff Gate",
    phase: "Testing",
    blockers: {
      acceptance_tests_passed: acceptance_suite.pass_rate === 100%,
      regression_suite_clean: regression_failures === 0,
      performance_benchmarks_met: all(perf_metrics < threshold),
      accessibility_compliant: a11y_score > 90,
      browser_compatibility: all(browsers.tested)
    },
    approvers: [Β₄],
    artifacts_required: [
      "Test execution reports",
      "Bug tracking status",
      "Performance reports",
      "QA signoff document"
    ],
    next: Κ₅,
    rollback: Κ₃
  },
  
  Κ₅: {
    name: "Deployment Approval Gate",
    phase: "Release",
    blockers: {
      staging_validation_complete: staging_tests.passed,
      rollback_plan_documented: exists(rollback_procedure),
      monitoring_configured: all(alerts.configured),
      runbooks_updated: documentation.current,
      change_approval_obtained: change_ticket.approved
    },
    approvers: [Β₅],
    artifacts_required: [
      "Deployment plan",
      "Rollback procedures",
      "Monitoring configuration",
      "Release notes"
    ],
    next: production_release,
    rollback: Κ₄
  }
}
```

## 🔐 Gate Enforcement
```
enforce_gate(Κᵢ) = {
  current_gate: get_active_gate(),
  
  # Check sequential progression
  validate_sequence: Κᵢ === current_gate.next ? 
    proceed : deny("Must complete " + current_gate.name),
  
  # Check blockers
  check_blockers: Κᵢ.blockers.map(b => ({
    blocker: b.name,
    status: evaluate(b.condition),
    details: b.status ? "✓ Passed" : "✗ " + b.failure_reason
  })),
  
  # Check artifacts
  check_artifacts: Κᵢ.artifacts_required.map(a => ({
    artifact: a,
    exists: find_artifact(a),
    valid: validate_artifact(a)
  })),
  
  # Require approval
  get_approval: {
    eligible_approvers: Κᵢ.approvers ∩ available_approvers(),
    request_approval: send_approval_request(eligible_approvers),
    wait_for_approval: blocking_wait(timeout: 48h)
  },
  
  # Log completion
  complete_gate: {
    log: record_gate_completion(Κᵢ, approvals, timestamp),
    transition: move_to_next_phase(Κᵢ.next),
    notify: broadcast_gate_completion(Κᵢ)
  }
}
```

## 📋 Gate Checklists
```
generate_checklist(Κᵢ) = {
  metadata: {
    gate: Κᵢ.name,
    phase: Κᵢ.phase,
    generated: timestamp()
  },
  
  blockers_checklist: Κᵢ.blockers.map(b => 
    "[ ] " + b.description + " (" + b.condition + ")"
  ),
  
  artifacts_checklist: Κᵢ.artifacts_required.map(a =>
    "[ ] " + a + " - uploaded and validated"
  ),
  
  approval_checklist: Κᵢ.approvers.map(role =>
    "[ ] Approval from " + Β_roles[role].name
  ),
  
  format: markdown_checklist()
}
```

## 🚨 Gate Violations
```
handle_gate_violation(violation_type, Κᵢ) = {
  bypassed_gate: {
    severity: "CRITICAL",
    action: rollback_to_gate(Κᵢ),
    notify: escalate_to_management(),
    audit: log_security_event()
  },
  
  incomplete_artifacts: {
    severity: "HIGH",
    action: block_progression(),
    notify: remind_artifact_owners(),
    timeout: 24h
  },
  
  failed_blockers: {
    severity: "MEDIUM",
    action: return_to_previous_phase(),
    notify: assigned_teams(),
    guidance: suggest_remediation()
  },
  
  missing_approval: {
    severity: "HIGH", 
    action: halt_until_approved(),
    notify: ping_approvers(),
    escalate: after_48h
  }
}
```

## ⚡ Gate Commands
```
S_gates = {
  !kg: "check_current_gate",
  !kga: "approve_gate",
  !kgc: "view_gate_checklist",
  !kgb: "show_gate_blockers",
  !kgh: "gate_history",
  !kgr: "request_gate_approval",
  !kgs: "skip_gate (emergency only)"
}
```

## 📊 Gate Metrics
```
track_gate_metrics() = {
  cycle_time_per_gate: {
    Κ₁: avg_days(start → approval),
    Κ₂: avg_days(approval → design_complete),
    Κ₃: avg_days(design → code_complete),
    Κ₄: avg_days(code → qa_signoff),
    Κ₅: avg_days(qa → deployment)
  },
  
  blocker_frequency: count_by_blocker_type(),
  approval_delays: avg_approval_time_by_role(),
  rollback_rate: rollbacks / total_attempts,
  
  quality_impact: {
    defect_escape_rate: bugs_in_prod / total_bugs,
    gate_effectiveness: prevented_issues / total_gates
  }
}
```

## 🔄 Gate Automation
```
automate_gate_checks() = {
  continuous_validation: {
    run_every: 15_minutes,
    check: current_gate.blockers,
    notify: on_status_change
  },
  
  artifact_monitoring: {
    watch: artifact_directories,
    validate: on_new_upload,
    update: checklist_status
  },
  
  approval_reminders: {
    initial: after_24h,
    followup: every_12h,
    escalate: after_72h
  }
}
```

## 🔗 Gate Integration
```
# Gate + Mode enforcement
gate_mode_requirements = {
  Κ₁: requires(Ω₁ ∨ Ω₂),  # Research or Innovate
  Κ₂: requires(Ω₂ ∨ Ω₃),  # Innovate or Plan
  Κ₃: requires(Ω₄),       # Execute only
  Κ₄: requires(Ω₄ ∨ Ω₅),  # Execute or Review
  Κ₅: requires(Ω₅)        # Review only
}

# Gate + Role validation
gate_role_matrix = {
  (Κ₁, Β₁): can_approve,
  (Κ₂, Β₂): can_approve,
  (Κ₃, Β₃): can_request,
  (Κ₃, Β₄): can_approve,
  (Κ₄, Β₄): can_approve,
  (Κ₅, Β₅): can_approve
}
```
