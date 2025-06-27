# 🐳 Docker MCP Integration for CursorRIPER Σ
# Symbol: Ξ (Xi)
# Version: 1.0.0

## 📋 Service Definition
```
service = "Container Operations"
symbol = "Ξ"
requires = "docker-mcp"
```

## 🔧 Operation Mapping
```
Ξ_ops = {
  container: {
    create: "docker-mcp:create-container",
    list: "docker-mcp:list-containers",
    logs: "docker-mcp:get-logs",
    start: "docker exec via create",
    stop: "docker stop via compose"
  },
  compose: {
    deploy: "docker-mcp:deploy-compose",
    down: "modify compose_yaml with replicas: 0"
  },
  image: {
    pull: "implicit via create-container",
    build: "via Dockerfile in compose_yaml"
  }
}
```

## 🔒 Mode Restrictions
```
MΞ = {
  Ω₁: [list_*, logs],                      # RESEARCH: read-only
  Ω₂: [list_*, logs, pull],                # INNOVATE: read + pull
  Ω₃: [all_ops],                          # PLAN: all operations
  Ω₄: [create, deploy, logs],              # EXECUTE: runtime ops
  Ω₅: [logs, list_*]                      # REVIEW: monitoring
}
```

## 🔑 Permission Matrix
```
ℙΞ = {
  create: [Ω₃, Ω₄],
  read: [Ω₁, Ω₂, Ω₃, Ω₄, Ω₅],
  update: [Ω₃, Ω₄],
  delete: [Ω₃]              # Only PLAN can remove
}
```

## 📍 Context Integration
```
Γ_docker = {
  running_containers: active_container_list[],
  compose_stacks: deployed_stacks[],
  container_logs: recent_logs{},
  resource_usage: {cpu: %, memory: MB}
}
```

## ⚡ Command Shortcuts
```
SΞ = {
  !dc: "create container",
  !dd: "deploy compose stack",
  !dl: "get container logs",
  !dls: "list containers",
  !ds: "stop container",
  !dr: "remove container"
}
```

## 🛡️ Protection Levels
```
ΨΞ = {
  create_container: Ψ₃,     # INFO - new container
  deploy_compose: Ψ₂,       # GUARDED - stack deployment
  stop_*: Ψ₄,              # DEBUG - stopping services
  remove_*: Ψ₆             # CRITICAL - destructive
}
```

## 🔄 Mode-Specific Behaviors
```
apply_docker_op(op, mode) = {
  check: op ∈ MΞ[mode] ? proceed : deny("Operation not allowed in " + mode),
  protect: op ∈ ΨΞ ? apply_protection(ΨΞ[op]) : continue,
  validate: check_resources() ∧ verify_config(),
  execute: Ξ_ops[category][operation]()
}
```

## 🔐 Safety Protocols
```
ΔΞ = {
  remove_*: confirm() ∧ backup_config() ∧ check_dependencies(),
  deploy: validate_compose() ∧ check_port_conflicts(),
  scale: check_resources() ∧ gradual_rollout(),
  production_deploy: require(Ω₅) ∧ approval_gate()
}
```

## 📊 Resource Management
```
resource_limits = {
  dev: {
    containers: 10,
    memory: "4GB",
    cpu: "2 cores"
  },
  prod: {
    containers: 50,
    memory: "16GB", 
    cpu: "8 cores"
  }
}
```

## 🚀 Deployment Workflows
```
deployment_flow = {
  dev: {
    build: local_dockerfile,
    test: Υ.test_container(),
    deploy: Ξ.create_container()
  },
  staging: {
    compose: staging_compose.yml,
    validate: health_checks(),
    deploy: Ξ.deploy_compose()
  },
  prod: {
    approval: require_gate(Κ₅),
    deploy: blue_green_deployment(),
    monitor: continuous_logs()
  }
}
```

## 📝 Compose Template Integration
```
compose_generator(project) = {
  template: `
version: '3.8'
services:
  ${project.name}:
    image: ${project.image}
    ports: ${project.ports}
    environment: ${project.env}
    deploy:
      replicas: ${project.replicas || 1}
  `,
  validate: yaml_syntax ∧ image_exists ∧ port_available
}
```

## 🔌 Feature Detection
```
detect_docker() = {
  try: {
    tools.find("docker-mcp:*"),
    verify_docker_daemon()
  },
  catch: warn("Docker MCP not available. Ensure Docker daemon is running."),
  fallback: disable_container_features()
}
```

## 🔗 Integration with Other Services
```
Θ×Ξ = deploy_from_github() = {
  1: Θ.get_file_contents("Dockerfile"),
  2: Θ.get_file_contents("docker-compose.yml"),
  3: Ξ.validate_config(compose_yaml),
  4: Ξ.deploy_compose({
       project_name: repo_name,
       compose_yaml: contents
     })
}
```
