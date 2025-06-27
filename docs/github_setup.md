# 🐙 GitHub MCP Setup Guide

## Prerequisites

1. **GitHub Account**: You need a GitHub account
2. **Personal Access Token**: Create one with appropriate permissions

## Creating a GitHub Personal Access Token

1. Go to GitHub Settings → Developer settings → Personal access tokens
2. Click "Generate new token (classic)"
3. Select scopes:
   - `repo` (Full control of private repositories)
   - `workflow` (Update GitHub Action workflows)
   - `write:packages` (Upload packages to GitHub Package Registry)
   - `delete:packages` (Delete packages from GitHub Package Registry)
   - `admin:org` (Full control of orgs and teams, read and write org projects)
   - `admin:public_key` (Full control of user public keys)
   - `admin:repo_hook` (Full control of repository hooks)
   - `gist` (Create gists)
   - `notifications` (Access notifications)
   - `user` (Update ALL user data)
   - `project` (Full control of projects)

4. Copy the generated token

## Installation

```bash
npm install -g @modelcontextprotocol/server-github
```

## Configuration

### Windows
```cmd
set GITHUB_TOKEN=your_token_here
```

### macOS/Linux
```bash
export GITHUB_TOKEN=your_token_here
```

### Or add to your shell profile:
```bash
echo 'export GITHUB_TOKEN=your_token_here' >> ~/.bashrc
```

## Verify Installation

1. Restart Cursor IDE
2. Check MCP is loaded: Look for GitHub operations in available tools
3. Test with: `!gr pytorch` (search for pytorch repositories)

## Available Operations

- **Repository Management**: create, fork, search
- **Branch Operations**: create, list branches
- **File Operations**: create, update, push files
- **Pull Requests**: create, review, merge
- **Issues**: create, update, comment

## Mode Restrictions

- **RESEARCH (Ω₁)**: Read-only operations
- **INNOVATE (Ω₂)**: Read + fork repositories  
- **PLAN (Ω₃)**: All operations available
- **EXECUTE (Ω₄)**: Write operations (push, merge)
- **REVIEW (Ω₅)**: Read-only verification

## Troubleshooting

1. **Token not found**: Ensure GITHUB_TOKEN is set in environment
2. **Permission denied**: Check token has required scopes
3. **Rate limits**: GitHub API has rate limits (5000 requests/hour with token)
