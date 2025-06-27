# 📄 PRD System for CursorRIPER Σ
# Symbol: Ρ (Rho)
# Version: 1.0.0

## 📋 PRD Definition System
```
service = "Product Requirements Document System"
symbol = "Ρ"
driver = "Transform memory-bank → PRD-driven methodology"
```

## 📐 PRD Components
```
Ρ = {
  Ρ₁: {
    name: "Business Objectives",
    required: true,
    template: "objectives_template.md",
    owner: Β₁,
    validation: [measurable, time_bound, aligned]
  },
  
  Ρ₂: {
    name: "Functional Requirements", 
    required: true,
    template: "requirements_template.md",
    owner: Β₁,
    validation: [specific, testable, prioritized]
  },
  
  Ρ₃: {
    name: "Technical Constraints",
    required: true,
    template: "constraints_template.md",
    owner: Β₂,
    validation: [feasible, documented, approved]
  },
  
  Ρ₄: {
    name: "User Stories",
    required: true,
    template: "story_template.md",
    owner: Β₁,
    validation: [sized, estimated, acceptance_defined]
  },
  
  Ρ₅: {
    name: "Acceptance Criteria",
    required: true,
    template: "acceptance_template.md",
    owner: Β₁ ∪ Β₄,
    validation: [measurable, complete, testable]
  },
  
  Ρ₆: {
    name: "Success Metrics",
    required: true,
    template: "metrics_template.md",
    owner: Β₁,
    validation: [quantifiable, trackable, relevant]
  }
}
```

## 📁 PRD Structure
```
/prd/
├── active/
│   ├── current_prd.md          # Ρ_active
│   ├── metadata.json           # Version, status, approvals
│   └── components/
│       ├── objectives.md       # Ρ₁
│       ├── requirements.md     # Ρ₂
│       ├── constraints.md      # Ρ₃
│       ├── stories/            # Ρ₄
│       ├── acceptance/         # Ρ₅
│       └── metrics.md          # Ρ₆
├── templates/
│   ├── prd_master.md
│   ├── objectives_template.md
│   ├── requirements_template.md
│   ├── constraints_template.md
│   ├── story_template.md
│   ├── acceptance_template.md
│   └── metrics_template.md
└── archive/
    └── [version]/              # Historical PRDs
```

## 🔄 Memory Bank Migration
```
σ_to_Ρ_migration = {
  σ₁: { // projectbrief.md
    migrate_to: Ρ₁,
    transform: extract_objectives(),
    preserve: backup_original()
  },
  
  σ₂: { // systemPatterns.md
    migrate_to: Β₂_artifacts,
    transform: convert_to_arch_docs(),
    link: reference_in_Ρ₃
  },
  
  σ₃: { // techContext.md
    migrate_to: Ρ₃,
    transform: structure_constraints(),
    enhance: add_validation_rules()
  },
  
  σ₄: { // activeContext.md
    migrate_to: Γ_prd ∪ Γ_roles,
    transform: separate_contexts(),
    maintain: real_time_sync()
  },
  
  σ₅: { // progress.md
    migrate_to: Κ_gates ∪ Ρ₆,
    transform: convert_to_metrics(),
    track: gate_completion_status()
  },
  
  σ₆: { // protection.md
    maintain: no_change,
    integrate: apply_to_PRD_sections()
  }
}
```

## 🔐 PRD State Management
```
Ρ_state = {
  draft: {
    editable: true,
    validators: [Β₁, Β₂],
    next: in_review
  },
  
  in_review: {
    editable: false,
    reviewers: [Β₁, Β₂, Β₃],
    next: approved ∨ draft
  },
  
  approved: {
    editable: false,
    locked: true,
    gate: Κ₁,
    next: in_development
  },
  
  in_development: {
    editable: change_requests_only,
    tracked: true,
    next: completed ∨ revised
  },
  
  completed: {
    editable: false,
    archived: true,
    reference: immutable
  }
}
```

## 📝 PRD Operations
```
create_prd(project_name) = {
  validate: no_active_prd() ∨ confirm_archive(),
  initialize: {
    id: generate_prd_id(),
    version: "1.0.0",
    created: timestamp(),
    state: "draft",
    components: init_all_Ρ()
  },
  structure: create_directory_structure(),
  templates: copy_templates_to_active(),
  return: prd_id
}

update_prd_component(Ρᵢ, content) = {
  check_state: Ρ_state[current].editable ? proceed : deny,
  check_owner: Β_current ∈ Ρᵢ.owner ? proceed : warn,
  validate: Ρᵢ.validation.all(content) ? proceed : errors,
  update: {
    content: content,
    modified: timestamp(),
    modified_by: Β_current
  },
  track: log_change(Ρᵢ, diff)
}
```

## ⚡ PRD Commands
```
S_prd = {
  !prd: "open_active_prd",
  !prdn: "create_new_prd", 
  !prda: "archive_current_prd",
  !prds: "show_prd_status",
  !prdv: "validate_prd_components",
  !prdc: "check_prd_completeness",
  !prdh: "prd_history"
}
```

## 🔍 PRD Validation
```
validate_prd() = {
  components: Ρ.map(c => ({
    name: c.name,
    valid: c.validation.all(c.content),
    errors: c.validation.failures()
  })),
  
  completeness: {
    required: Ρ.filter(c => c.required),
    complete: required.all(c => c.content.length > 0),
    percentage: (complete.count / required.count) * 100
  },
  
  ready_for_approval: completeness.percentage === 100
}
```

## 📊 PRD Context
```
Γ_prd = {
  active_prd: current_prd_id,
  prd_state: Ρ_state[current],
  prd_version: semantic_version,
  last_modified: timestamp,
  components_status: {
    Ρ₁: status,
    Ρ₂: status,
    ...
  },
  pending_reviews: review_queue[],
  change_requests: cr_queue[]
}
```

## 🔗 PRD Integration
```
# PRD + Gates
prd_gate_check(Κ₁) = {
  prd_complete: validate_prd().ready_for_approval,
  all_reviews: reviews_completed(),
  approvals: has_required_approvals(),
  
  all_true ? allow_gate_passage() : show_blockers()
}

# PRD + Modes
prd_mode_operations = {
  Ω₁: [read_prd, analyze_requirements],
  Ω₂: [read_prd, suggest_improvements],
  Ω₃: [read_prd, create_tech_spec],
  Ω₄: [read_prd, implement_requirements],
  Ω₅: [read_prd, verify_implementation]
}
```

## 📈 PRD Metrics
```
track_prd_metrics() = {
  cycle_time: approved_date - created_date,
  revision_count: version_history.length,
  requirement_changes: diff_count(Ρ₂),
  completion_rate: implemented / total_requirements,
  quality_score: (bugs_found / requirements) * 100
}
```
