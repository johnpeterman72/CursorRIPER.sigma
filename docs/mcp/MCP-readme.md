![CursorRIPER♦Σ](../res/github-header-sigma-sm.png)
# MCP Integration for CursorRIPER♦Σ

## 📚 Overview

CursorRIPER♦Σ now includes optional integration with Model Context Protocol (MCP) servers, enabling powerful capabilities like filesystem operations, web searches, and GitHub integration while maintaining the framework's symbolic notation and permission system.

## 🛠️ Features

- **Optional MCP Integration**: Use MCP services only if you have them installed
- **Symbolic Notation**: Consistent with the CursorRIPER♦Σ style (Φ for filesystem)
- **Mode-Specific Permissions**: MCP operations follow RIPER mode restrictions
- **Protection Integration**: MCP operations respect code protection levels
- **Context Integration**: MCP paths can be added to context references
- **Command Shortcuts**: Quick access to MCP operations with !f* commands

## ⚙️ Installation

### 1. MCP Server Setup

Install the MCP servers you want to use:

```bash
# Filesystem operations
npm install -g @modelcontextprotocol/server-filesystem

# Web search (optional)
npm install -g @modelcontextprotocol/server-websearch

# GitHub integration (optional)
npm install -g @modelcontextprotocol/server-github
```

### 2. Configure Cursor MCP

Create or update `.cursor/mcp.json` in your project:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "path/to/your/project"
      ]
    }
  }
}
```

### 3. Enable MCP Services (NOTE: CURRENTLY ONLY FILE SYSTEM IS WORKING & YOU CAN SKIP THIS STEP UNTIL OTHER ONES ARE BUILT OUT)

Edit `RIPERsigma.mcp.mdc` and uncomment the services you want to use:

```markdown
## 📁 Filesystem Services
@file ".cursor/rules/mcp_filesystem.mdc" # Local filesystem operations

## 🔍 Web Search Services
# @file ".cursor/rules/mcp_websearch.mdc" # Web search capabilities
```

## 🔍 Using MCP Filesystem

### Filesystem Operations

The filesystem operations are represented by the Φ_fs (Phi) symbol and include:

| Operation | Symbol | Description | Shortcut |
|-----------|--------|-------------|----------|
| Read File | Φ_fs.read | Read a file's contents | !fr |
| Multiple Read | Φ_fs.read_multi | Read multiple files | !fm |
| Write File | Φ_fs.write | Create or overwrite a file | !fw |
| Edit File | Φ_fs.edit | Make targeted edits to a file | !fe |
| Create Directory | Φ_fs.create_dir | Create a new directory | !fc |
| List Directory | Φ_fs.list | List contents of a directory | !fl |
| Directory Tree | Φ_fs.tree | Get recursive directory structure | !ft |
| Move File | Φ_fs.move | Move or rename a file | !fv |
| Search Files | Φ_fs.search | Find files matching a pattern | !fs |
| File Info | Φ_fs.info | Get file metadata | !fi |
| Allowed Dirs | Φ_fs.allowed | Get allowed directories | !fa |

### Example Usage

```
# Read a file
!fr("path/to/file.js")

# List directory contents
!fl("src/components")

# Search for JavaScript files
!fs("src", "*.js")

# Write to a file (Execute mode only)
!fw("output.txt", "File content")

# Add file to context
!afs("important.js")
```

## 🔒 Permission System

MCP operations respect the RIPER permission system:

| Mode | Read | Create | Update | Delete |
|------|------|--------|--------|--------|
| 🔍 Research | ✓ | ✗ | ✗ | ✗ |
| 💡 Innovate | ✓ | ~ | ✗ | ✗ |
| 📝 Plan | ✓ | ✓ | ~ | ✗ |
| ⚙️ Execute | ✓ | ✓ | ✓ | ~ |
| 🔎 Review | ✓ | ✗ | ✗ | ✗ |

## 📎 Context Integration

Add filesystem references to your context:

```
# Add file to context
!afs("src/main.js")

# Reference in cross-references
[Γ₉:src/components/Button.js]  # Filesystem reference
```

## 🛡️ Protection Levels

Filesystem operations are protected with the following levels:

| Level | Name | Allowed Operations |
|-------|------|-------------------|
| ψ₁ | Public | All operations |
| ψ₂ | Visible | read, list, search, info |
| ψ₃ | Limited | read, info |
| ψ₄ | Private | info only |
| ψ₅ | Restricted | none |
| ψ₆ | Forbidden | none |

## 🔍 Troubleshooting

### MCP Server Not Available

If you see "MCP Filesystem not available" errors:

1. Check that you've installed the MCP server: `npm list -g @modelcontextprotocol/server-filesystem`
2. Verify your `.cursor/mcp.json` configuration
3. Restart Cursor IDE

### Permission Errors

If operations are blocked due to permissions:

1. Check which RIPER mode you're in (`/r`, `/i`, `/p`, `/e`, `/rev`)
2. Switch to the appropriate mode for the operation (e.g., Execute mode for write operations)

### Path Errors

If you see path-related errors:

1. Make sure the path is within the allowed directories
2. Check that the path exists for read operations
3. Verify you have appropriate filesystem permissions

## 📚 Additional MCP Services

The MCP integration can be extended with other services by uncommenting them in `RIPERsigma.mcp.mdc`:

```markdown
## 🔍 Web Search Services
@file ".cursor/rules/mcp_websearch.mdc" # Web search capabilities

## 💻 GitHub Integration
@file ".cursor/rules/mcp_github.mdc" # GitHub repository operations
```

Each service has its own symbolic notation, permissions, and commands.

## 🗺️ Integration Architecture

The MCP integration follows a modular approach:

1. **Master Configuration**: `RIPERsigma.mcp.mdc` controls which services are enabled
2. **Service Modules**: Individual `.mdc` files in `.cursor/rules/` implement each service
3. **MCP Server Config**: `.cursor/mcp.json` configures the MCP servers

This architecture ensures that:
- Core framework remains unchanged
- Users enable only the services they need
- New services can be added without modifying existing ones
- Permissions and protection are consistent across services

## 🔖 References

- [Model Context Protocol Documentation](https://modelcontextprotocol.github.io/)
- [CursorRIPER♦Σ Symbols Reference]([./symbol-reference-guide.md](https://github.com/johnpeterman72/CursorRIPER.sigma/blob/main/docs/symbol-reference-guide.md)
- [MCP Filesystem Server Documentation](https://www.npmjs.com/package/@modelcontextprotocol/server-filesystem)
