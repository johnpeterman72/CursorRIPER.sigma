# 🎭 Puppeteer MCP Integration for CursorRIPER Σ
# Symbol: Υ (Upsilon)
# Version: 1.0.0

## 📋 Service Definition
```
service = "Browser Automation Operations"
symbol = "Υ"
requires = ["@modelcontextprotocol/server-puppeteer", "@executeautomation/playwright-mcp-server"]
```

## 🔧 Operation Mapping
```
Υ_ops = {
  browser: {
    launch: "puppeteer_navigate / playwright_navigate",
    close: "puppeteer_close / playwright_close",
    screenshot: "puppeteer_screenshot / playwright_screenshot"
  },
  page: {
    navigate: "puppeteer_navigate / playwright_navigate", 
    click: "puppeteer_click / playwright_click",
    fill: "puppeteer_fill / playwright_fill",
    select: "puppeteer_select / playwright_select",
    hover: "puppeteer_hover / playwright_hover"
  },
  test: {
    record: "start_codegen_session",
    end_record: "end_codegen_session",
    assert: "playwright_expect_response + playwright_assert_response"
  },
  scrape: {
    content: "playwright_get_visible_text",
    html: "playwright_get_visible_html",
    evaluate: "puppeteer_evaluate / playwright_evaluate"
  }
}
```

## 🔒 Mode Restrictions
```
MΥ = {
  Ω₁: [scrape_*, screenshot],                    # RESEARCH: data gathering
  Ω₂: [navigate, screenshot, scrape_*],          # INNOVATE: exploration
  Ω₃: [all_ops],                                # PLAN: all operations
  Ω₄: [test_*, navigate, click, fill, assert],   # EXECUTE: testing focus
  Ω₅: [screenshot, scrape_*, get_console_logs]   # REVIEW: verification
}
```

## 🔑 Permission Matrix
```
ℙΥ = {
  create: [Ω₃, Ω₄],          # PLAN/EXECUTE can create tests
  read: [Ω₁, Ω₂, Ω₃, Ω₄, Ω₅], # All can read page content
  update: [Ω₃, Ω₄],          # PLAN/EXECUTE can interact
  delete: []                 # No delete operations
}
```

## 📍 Context Integration
```
Γ_browser = {
  active_session: browser_instance,
  current_url: page.url(),
  test_recordings: codegen_sessions[],
  console_logs: captured_logs[],
  screenshots: saved_screenshots[]
}
```

## ⚡ Command Shortcuts
```
SΥ = {
  !pn: "navigate to URL",
  !ps: "take screenshot",
  !pc: "click element",
  !pf: "fill form field",
  !pt: "start test recording",
  !pe: "end test recording",
  !pg: "get page content"
}
```

## 🛡️ Protection Levels
```
ΨΥ = {
  navigate: Ψ₂,        # GUARDED - URL changes
  click: Ψ₃,           # INFO - user actions
  fill: Ψ₂,            # GUARDED - form data
  test_record: Ψ₅,     # TEST - test recording
  evaluate: Ψ₆         # CRITICAL - code execution
}
```

## 🔄 Mode-Specific Behaviors
```
apply_browser_op(op, mode) = {
  check: op ∈ MΥ[mode] ? proceed : deny("Operation not allowed in " + mode),
  protect: op ∈ ΨΥ ? apply_protection(ΨΥ[op]) : continue,
  track: {
    log_action(op, selector, value),
    capture_state(screenshot_if_needed)
  },
  execute: Υ_ops[category][operation]()
}
```

## 🎯 Testing Integration
```
test_workflow = {
  start: {
    mode: require(Ω₃ ∨ Ω₄),
    init: start_codegen_session({
      outputPath: "./tests/",
      includeComments: true
    })
  },
  record: {
    actions: [navigate, click, fill, assert],
    capture: automatic_via_codegen
  },
  end: {
    generate: end_codegen_session(sessionId),
    output: test_file_with_playwright_code
  }
}
```

## 📸 Screenshot Management
```
screenshot_policy = {
  Ω₁: "on_demand",
  Ω₂: "key_pages",
  Ω₃: "all_interactions", 
  Ω₄: "test_failures",
  Ω₅: "final_state"
}
```

## 🔌 Feature Detection
```
detect_browser_automation() = {
  puppeteer: tools.find("@modelcontextprotocol-server-puppeteer:*"),
  playwright: tools.find("@executeautomation-playwright-mcp-server:*"),
  preference: playwright > puppeteer,  # Playwright preferred
  fallback: warn("No browser automation available")
}
```

## 🔗 Integration with Other Services
```
Υ×Θ = test_and_commit() = {
  1: Υ.start_test_recording(),
  2: Υ.execute_test_actions(),
  3: Υ.end_test_recording() → test_file,
  4: Θ.create_branch("test/" + test_name),
  5: Θ.push_files([test_file]),
  6: Θ.create_pull_request()
}
```
