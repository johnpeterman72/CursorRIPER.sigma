# 📝 CursorRIPER Σ Changelog

## [1.0.5] - 2025-06-27

### 🎉 Major Feature Release: MCP Services & BMAD Enterprise

#### Added - MCP Service Integrations

##### GitHub Integration (Θ)
- Complete GitHub API integration via MCP
- Repository, branch, PR, and issue management
- Mode-specific restrictions (read-only in RESEARCH/REVIEW)
- Protection levels for critical operations
- Cross-service integration with Docker (Θ×Ξ)
- Commands: `!gr`, `!gc`, `!gp`, `!gpr`, `!gi`, `!gb`, `!gm`

##### Web Search Integration (Λ)  
- Brave Search API integration
- Web and local search capabilities
- **Critical**: NO SEARCH in EXECUTE mode (maintain focus!)
- Context tracking with Γ₁₀ (results) and Γ₁₁ (history)
- Search result caching system
- Commands: `!ws`, `!wl`, `!wf`, `!wc`, `!wh`

##### Browser Automation (Υ)
- Puppeteer and Playwright support
- Test recording and playback
- Screenshot and scraping capabilities
- Mode-specific browser restrictions
- Protection levels for navigation/forms
- Commands: `!pn`, `!ps`, `!pc`, `!pf`, `!pt`, `!pe`, `!pg`

##### Docker Integration (Ξ)
- Container and compose management
- Safety protocols for destructive operations
- Resource limits and deployment workflows
- Integration with GitHub for CI/CD
- Commands: `!dc`, `!dd`, `!dl`, `!dls`, `!ds`, `!dr`

#### Added - BMAD-Method Enterprise Features

##### Role System (Β)
- 5 professional roles: Product Owner, Architect, Developer, QA, DevOps
- Role-mode affinity scoring
- Permission matrices per role
- Artifact management by role
- Commands: `!br`, `!bra`, `!brp`, `!brg`, `!brh`, `!brs`

##### PRD System (Ρ)
- 6 PRD components with validation
- Memory bank to PRD migration (σ → Ρ)
- PRD state management (draft → approved → completed)
- Template system for all components
- Commands: `!prd`, `!prdn`, `!prda`, `!prds`, `!prdv`, `!prdc`, `!prdh`

##### Quality Gates (Κ)
- 5 sequential gates: PRD, Design, Code, QA, Deployment
- Automated checklist generation
- Blocker tracking and enforcement
- Approval workflows by role
- Commands: `!kg`, `!kga`, `!kgc`, `!kgb`, `!kgh`, `!kgr`, `!kgs`

##### Enterprise Features (Ε)
- Automated documentation generation
- Semantic versioning system
- Compliance tracking (ISO, SOC2, GDPR)
- Comprehensive audit trail
- Commands: `!edg`, `!evb`, `!ecr`, `!eal`, and more

#### Enhanced
- Extended Reference Map (ℜ) with all new service symbols
- Symbol Reference Guide updated to v3.0
- Added comprehensive command shortcuts for all systems
- Cross-service integration patterns (Θ×Ξ, Λ×Θ, Υ×Θ)
- Mode-Role-Gate integration (M×Β×Κ)

#### Added - Documentation
- `/docs/quickstart.md` - 5-minute setup guide
- `/docs/bmad_integration_guide.md` - Enterprise adoption guide
- `/docs/integration_tests.md` - Comprehensive test suite
- `/docs/mcp/` - Individual service setup guides
- PRD templates in `/prd/templates/`
- Gate checklists in `/quality/checklists/`

#### Added - Configuration Files
- `CursorRIPER.sigma.mcp.mdc` - Master MCP configuration
- `.cursor/mcp.json` - MCP server definitions
- `.cursor/bmad.json` - BMAD configuration
- Modular rule files in `.cursor/rules/`

### 🏗️ Architecture Improvements
- Maintained modular design - all features optional
- Graceful degradation when services unavailable
- Preserved token efficiency with symbolic notation
- Extended but didn't break existing patterns

### 🔧 Technical Details
- 12 new rule files created
- 15+ documentation files added
- 100+ new command shortcuts
- 8 Greek letters assigned to new systems
- Backward compatible with v1.0.3

### 📊 Migration Notes
- Existing projects can continue with memory banks
- Soft migration path recommended
- BMAD components can be adopted incrementally
- No breaking changes to core framework

---

## Version 1.0.4 (2025-05-15)

### 🆕 New Features

- **Protection End Markers**: Added explicit end markers for protected code regions
  - New `Ψ₊` array defining end markers for each protection level
  - End markers follow the pattern "END-X" where X is the first letter of the protection level
  - Better boundary definition for protected regions makes it clear where protection begins and ends

- **Reference Map**: Added compact `ℜ` map for more structured extensibility
  - Maintains small footprint while enabling easier additions to the framework
  - Currently includes protection references, expandable to other systems
  - Provides a foundation for future framework extensions

### 🔄 Changes

- **Reorganized Framework Structure**: More logical section ordering
  - Core definitions at the beginning
  - Related systems grouped together
  - Operational components after reference systems

- **Consolidated Redundant Sections**:
  - Combined Violation Detection and Response into unified Violation System
  - Streamlined Safety Protocols to reduce redundancy

- **Enhanced Protection Scanner**:
  - Updated to detect and validate paired start and end markers
  - Improved reporting of mismatched or missing markers

### 🔧 Technical Details

- Protection comments now include both start and end markers
- End markers follow the pattern "END-P", "END-G", etc.
- Protection regions now have explicit boundaries
- CodeProtection.mdc updated to version 1.0.1
- RIPERsigma updated to version 1.0.4
- Reduced token size through section consolidation while maintaining full functionality

---
## [1.0.3] - 2025-04-10
### Added
- Complete permission system with CRUD operations (ℙ)
- Mode-specific permission enforcement
- Permission violation handling with severity levels
- Permission command shortcuts

### Enhanced  
- Protection system integration with permissions
- Context system integration with permissions
- Cross-reference notation for permissions

---

## [1.0.2] - 2025-04-09
### Added
- Context reference system using Γ (Gamma) symbols
- 8 context types mapping to Cursor @ symbols
- Mode-specific context mappings (MΓ)
- Context command shortcuts (!af, !ac, etc.)
- Protection-Context integration (PΓ)

### Enhanced
- Active context tracking in memory files
- Context status indicators
- Cross-reference notation with context

---

## [1.0.1] - 2025-04-09
### Added
- Code protection end markers (Ψ₊)
- Protection commands (!cp, !cg, etc.)
- Protection registry in σ₆

### Enhanced
- Protection behavior across all modes
- Scanner validation for paired markers

---

## [1.0.0] - 2025-04-08
### Initial Release
- Core RIPER modes (Ω₁-Ω₅)
- Memory bank system (σ₁-σ₆)
- Project phases (Π₁-Π₄)
- Code protection system (Ψ₁-Ψ₆)
- Mathematical notation system
- Symbolic framework foundation

---
*Following Semantic Versioning (MAJOR.MINOR.PATCH)*
