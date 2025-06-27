# 🐳 Docker MCP Setup Guide

## Prerequisites

1. **Docker Desktop**: Installed and running
   - Windows: https://docs.docker.com/desktop/install/windows-install/
   - macOS: https://docs.docker.com/desktop/install/mac-install/
   - Linux: https://docs.docker.com/engine/install/

2. **Docker Daemon**: Must be running
3. **Sufficient Resources**: At least 4GB RAM allocated to Docker

## Installation

```bash
npm install -g docker-mcp
```

## Verify Docker Installation

```bash
# Check Docker is installed
docker --version

# Check Docker daemon is running
docker ps

# Check Docker Compose
docker compose version
```

## Configuration

No additional environment variables required if Docker is properly installed.

### Windows Specific
- Ensure Docker Desktop is running
- May need to enable virtualization in BIOS
- Use WSL2 backend (recommended)

### macOS Specific  
- Docker Desktop should start automatically
- Grant necessary permissions when prompted

### Linux Specific
- Add user to docker group:
  ```bash
  sudo usermod -aG docker $USER
  newgrp docker
  ```

## Verify MCP Installation

1. Restart Cursor IDE
2. Check MCP is loaded: Look for Docker operations
3. Test with: `!dls` (list containers)

## Available Operations

### Container Management
- **Create**: Spin up new containers
- **List**: Show running/stopped containers
- **Logs**: View container output
- **Remove**: Clean up containers

### Compose Operations
- **Deploy**: Launch multi-container stacks
- **Scale**: Adjust service replicas
- **Down**: Stop and remove stacks

### Image Operations
- **Pull**: Download images (automatic)
- **Build**: Create from Dockerfile

## Mode Restrictions

- **RESEARCH (Ω₁)**: List and logs only
- **INNOVATE (Ω₂)**: Read + pull images
- **PLAN (Ω₃)**: All operations
- **EXECUTE (Ω₄)**: Create, deploy, logs
- **REVIEW (Ω₅)**: Monitoring only

## Common Docker Compose Examples

### Basic Web App
```yaml
version: '3.8'
services:
  web:
    image: nginx:alpine
    ports:
      - "8080:80"
    volumes:
      - ./html:/usr/share/nginx/html
```

### Node.js with Database
```yaml
version: '3.8'
services:
  app:
    image: node:18-alpine
    working_dir: /app
    volumes:
      - .:/app
    command: npm start
    ports:
      - "3000:3000"
    depends_on:
      - db
  
  db:
    image: postgres:15-alpine
    environment:
      POSTGRES_PASSWORD: secret
    volumes:
      - pgdata:/var/lib/postgresql/data

volumes:
  pgdata:
```

## Resource Limits

### Development
- Max 10 containers
- 4GB memory total
- 2 CPU cores

### Production  
- Max 50 containers
- 16GB memory total
- 8 CPU cores

## Safety Features

1. **Confirmation Required**: For destructive operations
2. **Automatic Backups**: Config saved before changes
3. **Resource Validation**: Prevents overcommit
4. **Port Conflict Detection**: Automatic

## Best Practices

1. **Use Compose**: For multi-container apps
2. **Set Resource Limits**: Prevent runaway containers
3. **Volume Mounts**: For persistent data
4. **Health Checks**: Monitor container status
5. **Clean Up**: Remove unused containers/images

## Troubleshooting

### Docker Daemon Not Running
```bash
# Windows/macOS
# Start Docker Desktop application

# Linux
sudo systemctl start docker
```

### Permission Denied
```bash
# Linux: Add to docker group
sudo usermod -aG docker $USER
# Log out and back in
```

### Port Already in Use
```bash
# Find process using port
netstat -ano | findstr :8080  # Windows
lsof -i :8080                  # macOS/Linux

# Or use different port in compose
```

### Out of Space
```bash
# Clean up unused resources
docker system prune -a
```

## Integration Examples

### Deploy from GitHub
```javascript
// Combines GitHub + Docker
Θ×Ξ = deploy_from_github()
// Fetches Dockerfile and compose from repo
// Then deploys with Docker
```
