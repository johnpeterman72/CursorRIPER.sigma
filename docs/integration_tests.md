# 🧪 CursorRIPER Σ Integration Test Suite

## 📋 Overview
Comprehensive test scenarios for MCP services and BMAD integration.

## 🔧 MCP Service Tests

### GitHub Integration (Θ) Tests

#### Test 1: Mode Restrictions
```javascript
// Test: RESEARCH mode should only allow read operations
test('GitHub RESEARCH mode restrictions', () => {
  setMode('Ω₁'); // RESEARCH
  
  // Should succeed
  expect(!gr('tensorflow')).toBe(true); // search repos
  expect(!gi_list()).toBe(true); // list issues
  
  // Should fail
  expect(!gc('new-repo')).toBe(false); // create repo
  expect(!gp()).toBe(false); // push files
});
```

#### Test 2: Cross-Service Integration
```javascript
// Test: Search and Clone workflow (Λ×Θ)
test('Search to GitHub workflow', async () => {
  setMode('Ω₁'); // RESEARCH
  
  // Search for framework
  const results = await !ws('machine learning frameworks');
  
  // Extract GitHub URLs
  const githubUrls = extractGitHubUrls(results);
  
  // Switch to PLAN mode to fork
  setMode('Ω₃');
  const forked = await !fork(githubUrls[0]);
  
  expect(forked).toBeDefined();
});
```

### Web Search Integration (Λ) Tests

#### Test 3: EXECUTE Mode Block
```javascript
// Test: No search allowed in EXECUTE mode
test('Web search EXECUTE mode block', () => {
  setMode('Ω₄'); // EXECUTE
  
  // All search operations should fail
  expect(() => !ws('anything')).toThrow('No search in EXECUTE mode!');
  expect(() => !wl('restaurants')).toThrow('No search in EXECUTE mode!');
  expect(() => !wf('http://example.com')).toThrow('No search in EXECUTE mode!');
});
```

#### Test 4: Search Context Tracking
```javascript
// Test: Context tracking for searches
test('Search context persistence', async () => {
  setMode('Ω₁'); // RESEARCH
  
  // Perform searches
  await !ws('CursorRIPER framework');
  await !ws('AI development tools');
  
  // Check context
  const context = getContext();
  expect(context.Γ₁₀.length).toBe(2); // 2 search results
  expect(context.Γ₁₁.queries).toContain('CursorRIPER framework');
});
```

### Puppeteer Integration (Υ) Tests

#### Test 5: Test Recording Workflow
```javascript
// Test: Complete test recording cycle
test('Browser test recording', async () => {
  setMode('Ω₃'); // PLAN mode required
  
  // Start recording
  const session = await !pt();
  
  // Perform actions
  await !pn('https://example.com');
  await !pc('button[type="submit"]');
  await !pf('input[name="email"]', 'test@example.com');
  
  // End recording
  const testFile = await !pe();
  
  expect(testFile).toMatch(/playwright test/);
  expect(testFile).toContain('click');
  expect(testFile).toContain('fill');
});
```

### Docker Integration (Ξ) Tests

#### Test 6: Container Lifecycle
```javascript
// Test: Container management workflow
test('Docker container lifecycle', async () => {
  setMode('Ω₄'); // EXECUTE mode
  
  // Create container
  const container = await !dc({
    image: 'nginx:alpine',
    name: 'test-nginx',
    ports: {'80': '8080'}
  });
  
  // Get logs
  const logs = await !dl('test-nginx');
  expect(logs).toContain('nginx');
  
  // Cleanup (with confirmation)
  setMode('Ω₃'); // PLAN mode for deletion
  await !dr('test-nginx');
});
```

## 🏢 BMAD Integration Tests

### Role System (Β) Tests

#### Test 7: Role-Mode Affinity
```javascript
// Test: Role affinity enforcement
test('Role-mode affinity validation', () => {
  // Developer in RESEARCH mode (low affinity)
  !br('Developer');
  setMode('Ω₁');
  
  expect(getWarnings()).toContain('Role Developer not optimal for mode RESEARCH');
  
  // Developer in EXECUTE mode (perfect affinity)
  setMode('Ω₄');
  expect(getWarnings()).toHaveLength(0);
});
```

#### Test 8: Role Permission Matrix
```javascript
// Test: Role-specific permissions
test('Role permission enforcement', () => {
  // QA cannot delete production
  !br('QA');
  
  expect(canDelete('production')).toBe(false);
  
  // DevOps can delete non-production
  !br('DevOps');
  expect(canDelete('staging')).toBe(true);
  expect(canDelete('production')).toBe(false);
});
```

### PRD System (Ρ) Tests

#### Test 9: PRD Creation and Validation
```javascript
// Test: Complete PRD workflow
test('PRD lifecycle', async () => {
  !br('ProductOwner');
  setMode('Ω₁');
  
  // Create PRD
  const prdId = await !prdn();
  
  // Fill components
  await updateComponent('Ρ₁', 'Business objectives...');
  await updateComponent('Ρ₂', 'Functional requirements...');
  
  // Validate
  const validation = await !prdv();
  expect(validation.complete).toBe(false); // Not all components filled
  
  // Complete remaining components
  await fillAllComponents();
  
  const validation2 = await !prdv();
  expect(validation2.complete).toBe(true);
  expect(validation2.percentage).toBe(100);
});
```

### Quality Gates (Κ) Tests

#### Test 10: Gate Progression
```javascript
// Test: Sequential gate enforcement
test('Gate sequence validation', async () => {
  // Cannot skip to Κ₃ without completing Κ₁
  expect(() => approveGate('Κ₃')).toThrow('Must complete PRD Approval Gate');
  
  // Complete gates in sequence
  await completeGate('Κ₁');
  await completeGate('Κ₂');
  
  // Now Κ₃ is accessible
  expect(() => checkGate('Κ₃')).not.toThrow();
});
```

#### Test 11: Gate Approver Validation
```javascript
// Test: Only authorized roles can approve
test('Gate approver authorization', () => {
  !br('Developer');
  
  // Developer cannot approve Κ₁ (PRD gate)
  expect(() => !kga()).toThrow('Role cannot approve this gate');
  
  // Product Owner can approve Κ₁
  !br('ProductOwner');
  expect(() => !kga()).not.toThrow();
});
```

### Enterprise Features (Ε) Tests

#### Test 12: Documentation Generation
```javascript
// Test: Auto-documentation after gate
test('Documentation automation', async () => {
  // Complete code review gate
  await completeGate('Κ₃');
  
  // Docs should auto-generate
  const docs = await checkGeneratedDocs();
  
  expect(docs.technical).toExist();
  expect(docs.api).toExist();
  expect(docs.updated).toBe(today());
});
```

## 🔗 Integration Scenarios

### Scenario 1: Full Development Cycle
```javascript
test('Complete development workflow', async () => {
  // 1. Product Owner creates PRD
  !br('ProductOwner');
  setMode('Ω₁');
  await !prdn();
  await fillPRD();
  await !kga(); // Approve Κ₁
  
  // 2. Architect designs system
  !br('Architect');
  setMode('Ω₂');
  await createArchitecture();
  setMode('Ω₃');
  await !kga(); // Approve Κ₂
  
  // 3. Developer implements
  !br('Developer');
  setMode('Ω₃');
  await createPlan();
  setMode('Ω₄');
  await implement();
  
  // 4. QA tests
  !br('QA');
  await runTests();
  setMode('Ω₅');
  await !kga(); // Approve Κ₄
  
  // 5. DevOps deploys
  !br('DevOps');
  await !dd(); // Docker deploy
  await !kga(); // Approve Κ₅
  
  expect(getProjectStatus()).toBe('released');
});
```

### Scenario 2: GitHub-Docker Pipeline
```javascript
test('GitHub to Docker deployment', async () => {
  setMode('Ω₃'); // PLAN
  
  // Get files from GitHub
  const files = await !θ.get_file_contents({
    owner: 'company',
    repo: 'app',
    path: 'docker-compose.yml'
  });
  
  // Deploy with Docker
  setMode('Ω₄'); // EXECUTE
  const deployment = await !dd({
    compose_yaml: files.content,
    project_name: 'app'
  });
  
  // Verify deployment
  const containers = await !dls();
  expect(containers).toContain('app_web_1');
});
```

## 📊 Performance Tests

### Test 13: Mode Transition Speed
```javascript
test('Mode transition performance', () => {
  const start = performance.now();
  
  // Rapid mode switches
  for (let i = 0; i < 100; i++) {
    setMode('Ω₁');
    setMode('Ω₂');
    setMode('Ω₃');
    setMode('Ω₄');
    setMode('Ω₅');
  }
  
  const duration = performance.now() - start;
  expect(duration).toBeLessThan(1000); // < 1 second for 500 transitions
});
```

### Test 14: Context Operation Performance
```javascript
test('Context management performance', () => {
  const start = performance.now();
  
  // Add many context items
  for (let i = 0; i < 1000; i++) {
    !af(`file${i}.js`);
  }
  
  // Clear and measure
  !cc();
  
  const duration = performance.now() - start;
  expect(duration).toBeLessThan(500); // < 0.5 seconds
});
```

## 🚨 Error Handling Tests

### Test 15: Graceful Degradation
```javascript
test('MCP service unavailability', () => {
  // Disable GitHub MCP
  disableService('github');
  
  // Should warn but not crash
  const result = !gr('test');
  expect(result).toBeNull();
  expect(getWarnings()).toContain('GitHub MCP not available');
});
```

### Test 16: Permission Violations
```javascript
test('Permission violation handling', () => {
  setMode('Ω₁'); // RESEARCH
  
  // Attempt write operation
  const violation = attemptWrite('file.js', 'content');
  
  expect(violation.blocked).toBe(true);
  expect(violation.severity).toBe('CRITICAL');
  expect(getBackups()).toHaveLength(1); // Auto-backup created
  expect(getCurrentMode()).toBe('Ω₃'); // Reverted to PLAN
});
```

## 🎯 Test Execution

### Running Tests
```bash
# All tests
npm test

# Specific service
npm test -- --grep "GitHub"

# Integration only
npm test -- --grep "Integration"

# Performance suite
npm test -- --grep "Performance"
```

### CI/CD Integration
```yaml
# .github/workflows/test.yml
name: CursorRIPER Tests
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - run: npm install
      - run: npm test
      - run: npm run coverage
```

---
*Test Suite v1.0 | Framework v1.0.5*
