# 👥 BMAD Role System for CursorRIPER Σ
# Symbol: Β (Beta)
# Version: 1.0.0

## 📋 Role Definition System
```
service = "BMAD Role Management"
symbol = "Β"
transforms = "Memory-bank → PRD-driven development"
```

## 🎭 Role Mappings
```
Β_roles = {
  Β₁: {
    name: "Product Owner",
    primary_modes: [Ω₁, Ω₂],
    responsibilities: [
      "Define business objectives",
      "Create user stories", 
      "Set acceptance criteria",
      "Approve PRD documents"
    ],
    artifacts: [
      "PRD documents",
      "User stories",
      "Acceptance criteria",
      "Success metrics"
    ],
    permissions: ℙ_read ∪ ℙ_create(Ρ)
  },
  
  Β₂: {
    name: "Architect", 
    primary_modes: [Ω₂, Ω₃],
    responsibilities: [
      "Design system architecture",
      "Define technical standards",
      "Create API contracts",
      "Review technical designs"
    ],
    artifacts: [
      "Technical specifications",
      "System design documents",
      "API contracts",
      "Architecture diagrams"
    ],
    permissions: ℙ_all - ℙ_delete(production)
  },
  
  Β₃: {
    name: "Developer",
    primary_modes: [Ω₃, Ω₄],
    responsibilities: [
      "Implement features",
      "Write unit tests",
      "Create documentation",
      "Code reviews"
    ],
    artifacts: [
      "Source code",
      "Unit tests", 
      "Technical documentation",
      "Code commits"
    ],
    permissions: ℙ_standard ∪ ℙ_execute
  },
  
  Β₄: {
    name: "QA Engineer",
    primary_modes: [Ω₄, Ω₅],
    responsibilities: [
      "Create test plans",
      "Execute test cases",
      "Report bugs",
      "Verify fixes"
    ],
    artifacts: [
      "Test plans",
      "Test cases",
      "Bug reports",
      "QA signoff"
    ],
    permissions: ℙ_read ∪ ℙ_create(tests) ∪ ℙ_update(issues)
  },
  
  Β₅: {
    name: "DevOps",
    primary_modes: [Ω₄, Ω₅],
    responsibilities: [
      "Manage CI/CD",
      "Deploy applications",
      "Monitor systems",
      "Incident response"
    ],
    artifacts: [
      "Deployment configs",
      "CI/CD pipelines",
      "Monitoring dashboards",
      "Runbooks"
    ],
    permissions: ℙ_all
  }
}
```

## 🔄 Role Context Integration
```
Γ_roles = {
  active_role: Β_current ∈ {Β₁...Β₅},
  role_stack: [previous_roles],
  role_permissions: ℙ(Β_current),
  role_artifacts: artifacts[Β_current],
  role_gates: allowed_gates[Β_current]
}
```

## 🎯 Role-Mode Mapping
```
role_mode_affinity = {
  Β₁ × Ω₁: 1.0,  # Product Owner + Research = Perfect
  Β₁ × Ω₂: 0.9,  # Product Owner + Innovate = Great
  Β₁ × Ω₃: 0.3,  # Product Owner + Plan = Limited
  Β₁ × Ω₄: 0.1,  # Product Owner + Execute = Minimal
  Β₁ × Ω₅: 0.5,  # Product Owner + Review = Moderate
  
  Β₂ × Ω₁: 0.7,  # Architect + Research = Good
  Β₂ × Ω₂: 1.0,  # Architect + Innovate = Perfect
  Β₂ × Ω₃: 0.9,  # Architect + Plan = Great
  Β₂ × Ω₄: 0.2,  # Architect + Execute = Limited
  Β₂ × Ω₅: 0.6,  # Architect + Review = Moderate
  
  Β₃ × Ω₁: 0.3,  # Developer + Research = Limited
  Β₃ × Ω₂: 0.5,  # Developer + Innovate = Moderate
  Β₃ × Ω₃: 0.9,  # Developer + Plan = Great
  Β₃ × Ω₄: 1.0,  # Developer + Execute = Perfect
  Β₃ × Ω₅: 0.7,  # Developer + Review = Good
  
  Β₄ × Ω₁: 0.2,  # QA + Research = Minimal
  Β₄ × Ω₂: 0.3,  # QA + Innovate = Limited
  Β₄ × Ω₃: 0.6,  # QA + Plan = Moderate
  Β₄ × Ω₄: 0.9,  # QA + Execute = Great
  Β₄ × Ω₅: 1.0,  # QA + Review = Perfect
  
  Β₅ × Ω₁: 0.2,  # DevOps + Research = Minimal
  Β₅ × Ω₂: 0.3,  # DevOps + Innovate = Limited
  Β₅ × Ω₃: 0.7,  # DevOps + Plan = Good
  Β₅ × Ω₄: 1.0,  # DevOps + Execute = Perfect
  Β₅ × Ω₅: 0.9   # DevOps + Review = Great
}
```

## 🔐 Role Permissions
```
ℙ(Β) = {
  Β₁: {
    create: [Ρ_all, stories, criteria],
    read: [all],
    update: [Ρ_all, stories],
    delete: [draft_prd],
    approve: [Κ₁]
  },
  Β₂: {
    create: [tech_spec, design_docs, apis],
    read: [all],
    update: [tech_*, architecture],
    delete: [draft_designs],
    approve: [Κ₂]
  },
  Β₃: {
    create: [code, tests, docs],
    read: [all],
    update: [code, tests],
    delete: [feature_branches],
    approve: [Κ₃_partial]
  },
  Β₄: {
    create: [test_plans, bug_reports],
    read: [all],
    update: [test_*, bugs],
    delete: [test_data],
    approve: [Κ₄]
  },
  Β₅: {
    create: [all],
    read: [all],
    update: [all],
    delete: [all - production],
    approve: [Κ₅]
  }
}
```

## 🔄 Role Switching
```
switch_role(Β_new) = {
  validate: Β_new ∈ {Β₁...Β₅},
  check_mode: affinity[Β_new × Ω_current] > 0.5 ? proceed : warn,
  save_context: push(Γ_roles.role_stack, Β_current),
  update: {
    Β_current = Β_new,
    ℙ_active = ℙ(Β_new),
    artifacts = load_role_artifacts(Β_new)
  },
  notify: "Switched to " + Β_roles[Β_new].name
}
```

## 📋 Role Artifacts
```
create_artifact(type, content) = {
  check: type ∈ Β_current.artifacts ? proceed : deny,
  template: load_template(type, Β_current),
  create: {
    metadata: {role: Β_current, timestamp, author},
    content: apply_template(content)
  },
  store: /artifacts/Β_current/type/
}
```

## ⚡ Role Commands
```
S_roles = {
  !br: "switch_role",
  !bra: "show role artifacts",
  !brp: "show role permissions",
  !brg: "show allowed gates",
  !brh: "role history",
  !brs: "role suggestions for current mode"
}
```

## 🔗 Integration Points
```
# Role + Mode enforcement
enforce_role_mode(op) = {
  affinity_score = role_mode_affinity[Β_current × Ω_current],
  threshold = 0.3,
  
  affinity_score < threshold ? 
    warn("Role " + Β_current + " not optimal for mode " + Ω_current) :
    proceed(op)
}

# Role + Gate validation  
validate_gate_approver(Κ_gate) = {
  required_approvers = Κ_gate.approvers,
  can_approve = Β_current ∈ required_approvers,
  
  can_approve ? allow_approval() : deny("Role cannot approve this gate")
}
```

## 🎓 Role Guidance
```
suggest_role_for_task(task) = {
  analyze: extract_task_type(task),
  match: find_best_role(task_type),
  suggest: "Consider switching to " + Β_roles[match].name,
  reason: "This role specializes in " + task_type
}
```
