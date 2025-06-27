# 🚀 CursorRIPER Σ Quick Start Guide

## 📋 Prerequisites

1. **Cursor IDE** installed and configured
2. **Node.js** v14+ for MCP services
3. **Project folder** initialized

## 🎯 Quick Setup (5 minutes)

### Step 1: Install Framework
```bash
# Clone or download CursorRIPER Σ
# Copy to your project root
```

### Step 2: Enable Core Framework
1. Open Cursor IDE
2. Go to Settings → Cursor Rules
3. Enable `RIPERsigma1.0.5.mdc`

### Step 3: Initialize Memory Bank
```
/start
```
This creates:
- `/memory-bank/` folder
- 6 memory files (σ₁-σ₆)
- Symbol reference guide

## 🔥 Basic Usage

### Mode Switching
- `/r` or `/research` - Research mode 🔍
- `/i` or `/innovate` - Innovate mode 💡
- `/p` or `/plan` - Plan mode 📝
- `/e` or `/execute` - Execute mode ⚙️
- `/rev` or `/review` - Review mode 🔎

### Code Protection
```javascript
// !cp PROTECTED - Never modify
function criticalFunction() {
  // Core business logic
}
// !cp END-P

// !cg GUARDED - Ask before changing
function importantFunction() {
  // Important logic
}
// !cg END-G
```

### Context Management
```
!af src/main.js        # Add file to context
!ac validateUser()     # Add code reference
!cm                    # Set mode-appropriate context
!cc                    # Clear all context
```

## 🔌 Optional: MCP Services

### Enable Services (Choose what you need)

1. **GitHub Integration**
   ```bash
   npm install -g @modelcontextprotocol/server-github
   export GITHUB_TOKEN=your_token
   ```
   - Uncomment in `CursorRIPER.sigma.mcp.mdc`
   - Use: `!gr pytorch` to search repos

2. **Web Search**
   ```bash
   npm install -g @modelcontextprotocol/server-brave-search
   export BRAVE_SEARCH_API_KEY=your_key
   ```
   - Uncomment in `CursorRIPER.sigma.mcp.mdc`
   - Use: `!ws AI frameworks` to search

3. **Browser Automation**
   ```bash
   npm install -g @executeautomation/playwright-mcp-server
   ```
   - Uncomment in `CursorRIPER.sigma.mcp.mdc`
   - Use: `!pn https://example.com` to navigate

4. **Docker**
   ```bash
   npm install -g docker-mcp
   # Ensure Docker Desktop is running
   ```
   - Uncomment in `CursorRIPER.sigma.mcp.mdc`
   - Use: `!dls` to list containers

## 🏢 Optional: BMAD Enterprise

### Soft Migration (Recommended for start)
1. Keep using memory banks
2. Uncomment BMAD components in `.cursor/bmad.json`:
   - `bmad_roles.mdc` - Role system
   - `prd_system.mdc` - PRD management

### Commands
```
!br Developer      # Switch to Developer role
!prdn             # Create new PRD
!kg               # Check current quality gate
```

## 📚 Cheat Sheets

### Essential Commands
| Action | Command | Mode Required |
|--------|---------|---------------|
| Read files | automatic | Any |
| Write code | automatic | EXECUTE |
| Create plan | automatic | PLAN |
| Search web | !ws query | NOT EXECUTE |
| Take screenshot | !ps name | Any |

### Mode Permissions
| Mode | Can Do | Cannot Do |
|------|--------|-----------|
| RESEARCH 🔍 | Read, analyze | Write, modify |
| INNOVATE 💡 | Read, suggest | Implement |
| PLAN 📝 | Read, design | Execute |
| EXECUTE ⚙️ | All operations | Deviate from plan |
| REVIEW 🔎 | Read, verify | Modify |

## 🚨 Common Issues

### "Operation not permitted"
- Check current mode with `[MODE: X]` 
- Switch to the appropriate mode
- EXECUTE mode has most permissions

### "MCP service not available"
- Service not installed
- Environment variable not set
- Check `/docs/mcp/` for setup guides

### "No search in EXECUTE mode"
- This is intentional! 
- Maintains focus during implementation
- Switch to RESEARCH/PLAN to search

## 💡 Pro Tips

1. **Start Simple**: Use the core framework first, add MCP/BMAD later
2. **Mode Discipline**: Let modes guide your workflow
3. **Protection Markers**: Use them for critical code
4. **Context Awareness**: Keep context focused and relevant
5. **Gradual Adoption**: Enable features as needed

## 🎓 Next Steps

1. Read complete documentation in `/docs/`
2. Review the symbol reference guide
3. Try a simple project with RIPER modes
4. Enable MCP services one at a time
5. Consider BMAD for team projects

---
*Framework Version: 1.0.5 | Quick Start v1.0*
