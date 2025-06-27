# 🏢 BMAD Integration Guide for CursorRIPER Σ

## 📋 Overview

BMAD-Method integration transforms CursorRIPER Σ from memory-bank driven to PRD-driven enterprise methodology. This guide covers migration strategies and best practices.

## 🎯 Integration Philosophy

BMAD enhances CursorRIPER Σ with:
- **Role-based workflows** (Β)
- **PRD-driven development** (Ρ)
- **Quality gates** (Κ)
- **Enterprise features** (Ε)

While maintaining:
- Symbolic notation efficiency
- RIPER mode discipline
- Token optimization
- Modular architecture

## 🔄 Migration Strategies

### Option 1: Soft Migration (Recommended)

**Phase 1: Preparation (Week 1)**
```
1. Continue using memory banks (σ₁-σ₆)
2. Enable role system:
   - Uncomment in .cursor/bmad.json:
     @file .cursor/rules/bmad_roles.mdc
3. Assign team roles:
   - Product Owner → Β₁
   - Architect → Β₂
   - Developers → Β₃
   - QA → Β₄
   - DevOps → Β₅
4. Practice role switching:
   !br Developer
```

**Phase 2: Parallel Running (Week 2-3)**
```
1. Enable PRD system:
   @file .cursor/rules/prd_system.mdc
2. Create first PRD from memory banks:
   !prdn
3. Map memory content:
   σ₁ (projectbrief) → Ρ₁ (objectives)
   σ₂ (systemPatterns) → Architect artifacts
   σ₃ (techContext) → Ρ₃ (constraints)
4. Run both systems in parallel
```

**Phase 3: Gate Introduction (Week 4)**
```
1. Enable quality gates:
   @file .cursor/rules/quality_gates.mdc
2. Start with advisory mode
3. Practice gate workflows:
   !kg - Check current gate
   !kgc - View checklist
4. Gradually enforce gates
```

### Option 2: Full Migration (Advanced Teams)

```
1. Enable all BMAD components immediately
2. Archive existing memory banks
3. Create comprehensive PRD
4. Enforce all quality gates
5. Activate enterprise features
```

## 👥 Role Adoption Guide

### Product Owner (Β₁)
**Primary Modes**: RESEARCH (Ω₁), INNOVATE (Ω₂)
```
Workflow:
1. !br ProductOwner
2. /r - Enter research mode
3. Gather requirements
4. !prdn - Create PRD
5. Define objectives (Ρ₁)
6. Write user stories (Ρ₄)
7. !kga - Approve PRD gate
```

### Architect (Β₂)
**Primary Modes**: INNOVATE (Ω₂), PLAN (Ω₃)
```
Workflow:
1. !br Architect
2. /i - Enter innovate mode
3. Design system architecture
4. /p - Switch to plan mode
5. Create technical specs
6. Update constraints (Ρ₃)
7. !kga - Approve design gate
```

### Developer (Β₃)
**Primary Modes**: PLAN (Ω₃), EXECUTE (Ω₄)
```
Workflow:
1. !br Developer
2. /p - Enter plan mode
3. Review PRD and specs
4. Create implementation plan
5. /e - Switch to execute mode
6. Implement features
7. !kg - Check code review gate
```

### QA Engineer (Β₄)
**Primary Modes**: EXECUTE (Ω₄), REVIEW (Ω₅)
```
Workflow:
1. !br QA
2. /e - Enter execute mode
3. Create test plans
4. Execute tests
5. /rev - Switch to review mode
6. Verify implementation
7. !kga - Approve QA gate
```

### DevOps (Β₅)
**Primary Modes**: EXECUTE (Ω₄), REVIEW (Ω₅)
```
Workflow:
1. !br DevOps
2. Setup CI/CD pipelines
3. Configure monitoring
4. Prepare deployment
5. !kga - Approve deployment gate
```

## 📄 PRD Workflow

### Creating PRD
```bash
# 1. Initialize PRD
!prdn

# 2. Navigate to PRD
cd prd/active/

# 3. Fill components
- objectives.md (Ρ₁)
- requirements.md (Ρ₂)
- constraints.md (Ρ₃)
- stories/*.md (Ρ₄)
- acceptance/*.md (Ρ₅)
- metrics.md (Ρ₆)

# 4. Validate PRD
!prdv

# 5. Check completeness
!prdc
```

### PRD States
```
draft → in_review → approved → in_development → completed
         ↓
      (revisions)
```

## 🚦 Quality Gate Process

### Gate Progression
```
START → Κ₁ → Κ₂ → Κ₃ → Κ₄ → Κ₅ → RELEASE
        PRD  Design Code  QA   Deploy
```

### Gate Workflow
```bash
# 1. Check current gate
!kg

# 2. View checklist
!kgc

# 3. Complete blockers
- Fix all items marked ❌
- Upload required artifacts
- Run required tests

# 4. Request approval
!kgr

# 5. Gate approval (by authorized role)
!kga
```

### Emergency Override
```bash
!kgs  # Skip gate - requires justification
```

## 🏢 Enterprise Features

### Documentation Generation
```bash
# Generate all docs
!edg

# Generate specific docs
!edgt  # Technical documentation
!edga  # API documentation
!edgu  # User guide
```

### Version Management
```bash
# Bump version
!evb minor  # 1.0.0 → 1.1.0

# Create release tag
!evt

# View changelog
!evc
```

### Compliance Tracking
```bash
# Check compliance score
!ecs

# Generate compliance report
!ecr

# View compliance gaps
!ecg
```

## 📊 Best Practices

### 1. Role Discipline
- Stay within role boundaries
- Use appropriate modes for role
- Request approval from correct roles

### 2. PRD Maintenance
- Keep PRD as single source of truth
- Update PRD before implementation
- Archive completed PRDs

### 3. Gate Hygiene
- Never skip gates without reason
- Complete all blockers before proceeding
- Maintain audit trail

### 4. Documentation
- Generate docs after each gate
- Keep docs version-aligned
- Automate where possible

## 🔧 Configuration Examples

### Team Configuration
```json
{
  "team": {
    "product_owner": ["alice@company.com"],
    "architects": ["bob@company.com"],
    "developers": ["carol@company.com", "dave@company.com"],
    "qa": ["eve@company.com"],
    "devops": ["frank@company.com"]
  },
  "gate_enforcement": "advisory",  // advisory | strict
  "prd_required": true,
  "auto_documentation": true
}
```

### Gate Customization
```javascript
// In quality_gates.mdc
Κ_custom = {
  security_review: {
    phase: "Pre-deployment",
    blockers: {
      security_scan: "passed",
      penetration_test: "completed"
    },
    approvers: ["security_team"]
  }
}
```

## 🚨 Common Challenges

### "Role permissions conflict"
- Check role-mode affinity
- Some operations need specific roles
- Use !brp to see role permissions

### "Gate blocked indefinitely"
- Review !kgb for blockers
- Ensure artifacts uploaded
- Check approver availability

### "PRD out of sync"
- Always update PRD first
- Use !prdv to validate
- Archive old versions properly

## 📈 Success Metrics

Track these KPIs:
1. **Gate cycle time**: Time spent at each gate
2. **PRD accuracy**: Changes after approval
3. **Defect escape rate**: Bugs found post-gates
4. **Documentation coverage**: Auto-generated %
5. **Compliance score**: Overall compliance %

## 🎓 Training Resources

1. **Role-specific guides**: `/docs/bmad/roles/`
2. **PRD templates**: `/prd/templates/`
3. **Gate checklists**: `/quality/checklists/`
4. **Video tutorials**: Coming soon
5. **Practice project**: `/examples/bmad-tutorial/`

## 🔄 Rollback Plan

If BMAD doesn't fit your team:
1. Disable components in `.cursor/bmad.json`
2. Revert to memory banks
3. Keep what works (e.g., just roles)
4. No framework damage - fully reversible

---
*BMAD Integration Guide v1.0 | Framework v1.0.5*
