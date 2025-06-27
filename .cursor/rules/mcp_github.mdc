# 🐙 GitHub MCP Integration for CursorRIPER Σ
# Symbol: Θ (Theta)
# Version: 1.0.0

## 📋 Service Definition
```
service = "GitHub Operations"
symbol = "Θ"
requires = "@modelcontextprotocol/server-github"
```

## 🔧 Operation Mapping
```
Θ_ops = {
  repo: {
    create: "@modelcontextprotocol-server-github:create_repository",
    search: "@modelcontextprotocol-server-github:search_repositories", 
    fork: "@modelcontextprotocol-server-github:fork_repository",
    clone: "git clone via get_file_contents"
  },
  branch: {
    create: "@modelcontextprotocol-server-github:create_branch",
    list: "@modelcontextprotocol-server-github:list_commits",
    checkout: "via create_branch with from_branch"
  },
  file: {
    create: "@modelcontextprotocol-server-github:create_or_update_file",
    push: "@modelcontextprotocol-server-github:push_files",
    get: "@modelcontextprotocol-server-github:get_file_contents"
  },
  pr: {
    create: "@modelcontextprotocol-server-github:create_pull_request",
    review: "@modelcontextprotocol-server-github:create_pull_request_review",
    merge: "@modelcontextprotocol-server-github:merge_pull_request",
    list: "@modelcontextprotocol-server-github:list_pull_requests"
  },
  issue: {
    create: "@modelcontextprotocol-server-github:create_issue",
    update: "@modelcontextprotocol-server-github:update_issue",
    comment: "@modelcontextprotocol-server-github:add_issue_comment",
    list: "@modelcontextprotocol-server-github:list_issues"
  }
}
```

## 🔒 Mode Restrictions
```
MΘ = {
  Ω₁: [search_*, list_*, get_*],                    # RESEARCH: read-only
  Ω₂: [search_*, list_*, get_*, fork_repository],   # INNOVATE: read + fork
  Ω₃: [all_ops],                                    # PLAN: all operations
  Ω₄: [create_*, update_*, push_*, merge_*],        # EXECUTE: write ops
  Ω₅: [get_*, list_*, search_*]                     # REVIEW: read-only
}
```

## 🔑 Permission Matrix
```
ℙΘ = {
  create: [Ω₃, Ω₄],
  read: [Ω₁, Ω₂, Ω₃, Ω₄, Ω₅],
  update: [Ω₃, Ω₄],
  delete: [Ω₃]
}
```

## 📍 Context Integration
```
Γ_github = {
  current_repo: active repository reference,
  current_branch: active branch name,
  pending_prs: open pull requests,
  assigned_issues: assigned issue list
}
```

## ⚡ Command Shortcuts
```
SΘ = {
  !gr: "search_repositories",
  !gc: "create_repository",
  !gp: "push_files",
  !gpr: "create_pull_request",
  !gi: "create_issue",
  !gb: "create_branch",
  !gm: "merge_pull_request"
}
```

## 🛡️ Protection Levels
```
ΨΘ = {
  push_files: Ψ₂,           # GUARDED - code changes
  merge_pull_request: Ψ₆,   # CRITICAL - main branch
  delete_*: Ψ₆,            # CRITICAL - destructive
  create_repository: Ψ₃     # INFO - new repo
}
```

## 🔄 Mode-Specific Behaviors
```
apply_github_op(op, mode) = {
  check: op ∈ MΘ[mode] ? proceed : deny("Operation not allowed in " + mode),
  protect: op ∈ ΨΘ ? apply_protection(ΨΘ[op]) : continue,
  log: record_operation(op, mode, timestamp),
  execute: Θ_ops[category][operation]()
}
```

## 🚨 Safety Protocols
```
ΔΘ = {
  merge_*: require_review() ∧ check_ci_status(),
  delete_*: confirm() ∧ backup_reference(),
  push_to_main: deny() ∨ (confirm() ∧ Ψ₆)
}
```

## 🔌 Feature Detection
```
detect_github() = {
  try: tools.find("@modelcontextprotocol-server-github:*"),
  catch: warn("GitHub MCP not available. Install with: npm install -g @modelcontextprotocol/server-github"),
  fallback: disable_github_features()
}
```
