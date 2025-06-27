# 🎭 Puppeteer/Playwright MCP Setup Guide

## Prerequisites

1. **Node.js**: Version 14 or higher
2. **Chrome/Chromium**: Automatically downloaded during installation
3. **Sufficient Disk Space**: ~200MB for browser binaries

## Installation Options

### Option 1: Puppeteer (Simpler)
```bash
npm install -g @modelcontextprotocol/server-puppeteer
```

### Option 2: Playwright (Recommended - More Features)
```bash
npm install -g @executeautomation/playwright-mcp-server
```

## Why Playwright?

- ✅ Multi-browser support (Chrome, Firefox, Safari)
- ✅ Better test recording capabilities  
- ✅ More reliable selectors
- ✅ Built-in waiting strategies
- ✅ Network interception

## Configuration

No environment variables required! Browser automation works out of the box.

## Verify Installation

1. Restart Cursor IDE
2. Check MCP is loaded: Look for browser operations
3. Test with: `!pn https://example.com` (navigate)
4. Test screenshot: `!ps homepage` (take screenshot)

## Available Operations

### Browser Control
- **Navigate**: Go to URLs
- **Screenshot**: Capture pages or elements
- **Close**: Clean up browser instance

### Page Interaction  
- **Click**: Click buttons, links, elements
- **Fill**: Enter text in forms
- **Select**: Choose dropdown options
- **Hover**: Mouse over elements

### Testing
- **Record**: Start test recording session
- **Assert**: Verify page behavior
- **Generate**: Create test files

### Data Extraction
- **Get Text**: Extract visible content
- **Get HTML**: Retrieve page structure
- **Evaluate**: Run JavaScript in page context

## Mode Restrictions

- **RESEARCH (Ω₁)**: Screenshots, content extraction
- **INNOVATE (Ω₂)**: Navigation, exploration
- **PLAN (Ω₃)**: All operations available
- **EXECUTE (Ω₄)**: Test recording and execution
- **REVIEW (Ω₅)**: Verification and screenshots

## Test Recording Workflow

```javascript
// 1. Start recording (PLAN or EXECUTE mode)
!pt  // Start test recording

// 2. Perform actions
!pn https://yourapp.com
!pc button[type="submit"]
!pf input[name="email"] user@example.com

// 3. End recording  
!pe  // Generates test file
```

## Best Practices

1. **Headless Mode**: Default for performance
2. **Selectors**: Use data-testid when possible
3. **Waits**: Let Playwright handle waiting
4. **Screenshots**: Name them descriptively
5. **Cleanup**: Browser closes automatically

## Common Issues

1. **Browser Download Failed**
   ```bash
   # Manually install browsers
   npx playwright install
   ```

2. **Timeout Errors**
   - Increase timeout in navigation
   - Check if page is actually loading

3. **Selector Not Found**
   - Use Playwright inspector
   - Try more specific selectors

4. **Permission Denied**
   - Run as administrator (Windows)
   - Check file write permissions

## Advanced Features

### Custom User Agent
```javascript
playwright_custom_user_agent("MyBot/1.0")
```

### Console Log Capture
```javascript
playwright_console_logs({ type: "error" })
```

### PDF Generation
```javascript
playwright_save_as_pdf({
  filename: "report.pdf",
  format: "A4"
})
```
