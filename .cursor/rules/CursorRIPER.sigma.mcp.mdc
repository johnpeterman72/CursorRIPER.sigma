# 🔌 CursorRIPER Σ MCP Master Configuration
# Version: 1.1.0
# Enable/disable MCP services by uncommenting @file directives

## 📋 MCP Service Integration for CursorRIPER Σ

This configuration file enables Model Context Protocol (MCP) services
within the CursorRIPER Σ framework. Each service is modular and optional.

### 🛠️ Available Services:

#### Φ - Filesystem Operations
# Provides local file system access and manipulation
# @file .cursor/rules/mcp_filesystem.mdc

#### Θ - GitHub Operations  
# GitHub repository management and collaboration
# Requires: GITHUB_TOKEN environment variable
# @file .cursor/rules/mcp_github.mdc

#### Λ - Web Search Operations
# Web search capabilities via Brave Search API
# Requires: BRAVE_SEARCH_API_KEY environment variable
# @file .cursor/rules/mcp_websearch.mdc

#### Υ - Browser Automation Operations
# Puppeteer/Playwright browser automation and testing
# @file .cursor/rules/mcp_puppeteer.mdc

#### Ξ - Container Operations
# Docker container and compose management
# Requires: Docker daemon running
# @file .cursor/rules/mcp_docker.mdc

### 📝 Configuration Instructions:

1. **Install MCP servers** for desired services:
   ```bash
   # Filesystem (included with Cursor)
   # No installation needed
   
   # GitHub
   npm install -g @modelcontextprotocol/server-github
   
   # Web Search
   npm install -g @modelcontextprotocol/server-brave-search
   
   # Puppeteer
   npm install -g @modelcontextprotocol/server-puppeteer
   # OR Playwright (recommended)
   npm install -g @executeautomation/playwright-mcp-server
   
   # Docker
   npm install -g docker-mcp
   ```

2. **Set environment variables**:
   - `GITHUB_TOKEN`: Personal access token for GitHub
   - `BRAVE_SEARCH_API_KEY`: API key from brave.com/search/api

3. **Uncomment @file directives** above for services you want to enable

4. **Update .cursor/mcp.json** with server configurations (see example below)

### 📋 Example mcp.json:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["@modelcontextprotocol/server-filesystem"],
      "config": {
        "directories": ["D:\\Cursor Projects\\CursorRIPER.sigma"]
      }
    },
    "github": {
      "command": "npx",
      "args": ["@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_TOKEN": "${GITHUB_TOKEN}"
      }
    },
    "brave-search": {
      "command": "npx",
      "args": ["@modelcontextprotocol/server-brave-search"],
      "env": {
        "BRAVE_SEARCH_API_KEY": "${BRAVE_SEARCH_API_KEY}"
      }
    },
    "playwright": {
      "command": "npx",
      "args": ["@executeautomation/playwright-mcp-server"]
    },
    "docker": {
      "command": "npx",
      "args": ["docker-mcp"]
    }
  }
}
```

### 🔗 Service Integration Map:

```
Composite Operations = {
  Θ×Ξ: deploy_from_github(),      # GitHub → Docker
  Λ×Θ: search_and_clone(),       # Search → GitHub  
  Υ×Θ: test_and_commit(),        # Test → GitHub
  Φ×Θ: sync_local_to_github()    # Files → GitHub
}
```

### ⚠️ Important Notes:

- Services are independent and can be enabled/disabled individually
- Missing services gracefully degrade with warnings
- Mode restrictions apply to all MCP operations
- Protection levels enforce security on sensitive operations
- Context tracking maintains state across operations

For detailed service documentation, see:
- `/docs/mcp/` directory for setup guides
- Individual service rule files for operation details
