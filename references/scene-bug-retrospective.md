# Scene: Bug Retrospective

Turn a painful debugging session into a permanent asset — step on this mine once, never again.

## Detection Signals

Scan the source content for these patterns. Score each match; if total score exceeds **0.6**, classify as Bug Retrospective.

| Signal Pattern | Weight | Examples |
|---------------|--------|----------|
| Error/exception handling | 0.30 | "error", "exception", "traceback", "stack trace", "crash", "failed" |
| Bug fixing actions | 0.25 | "fix", "patch", "hotfix", "resolved", "root cause", "the issue was" |
| Debugging process | 0.20 | "debugging", "breakpoint", "logging", "reproduce", "isolate" |
| Failure patterns | 0.15 | "failed because", "broke when", "didn't work", "unexpected behavior" |
| Prevention discussion | 0.10 | "prevent", "guard", "validate", "check before", "test for" |

## Extraction Dimensions

### 1. Bug Profile

Capture the bug's identity card:
- **Symptom**: What the user/system observed
- **Trigger condition**: Exact steps or conditions to reproduce
- **Impact scope**: What was affected (single function, module, system-wide)
- **Environment**: Language, framework, OS, version if relevant

### 2. Root Cause Chain

Trace from symptom to root cause:
- Surface symptom → direct cause → underlying cause → root cause
- Each link in the chain should explain "why" the previous level happened
- Note any red herrings encountered during investigation

### 3. Quick Diagnosis Method

Distill the fastest path to identify this class of bug next time:
- What to check first (the "5-minute test")
- Key log messages or error patterns to grep for
- Diagnostic commands or code snippets

### 4. Prevention Checklist

Concrete measures to prevent recurrence:
- Code review checklist items
- Test cases to add
- Linter rules or static analysis checks
- Coding conventions to follow

### 5. Transferable Debugging Methodology

Abstract the debugging approach into a reusable method:
- What general strategy was used (binary search, hypothesis testing, etc.)
- What tools were effective
- What mental model helped crack the problem

## Confidence Scoring Guidance

- **high**: Root cause confirmed by fix that resolved the issue, explicit error messages cited
- **medium**: Root cause likely but fix was a workaround, or multiple potential causes remain
- **low**: Suspected cause without confirmation, or fix worked but reason unclear

## Output Structure

```markdown
# <Title: Bug Description>

> **One-line summary**: <What broke and why, in one sentence>

## Bug Profile
- **Symptom**: ...
- **Trigger**: ...
- **Impact**: ...
- **Environment**: ...

## Root Cause Chain
- **[confidence]** Surface: <What was observed>
  → Direct cause: <Why it happened>
  → Root cause: <Fundamental reason>
- Red herrings: ...

## Quick Diagnosis
When you see `<symptom pattern>`, check:
1. ...
2. ...
3. ...

## Prevention Checklist
- [ ] <Code review item>
- [ ] <Test case to add>
- [ ] <Linter/static analysis rule>

## Debugging Methodology
- **Strategy**: ...
- **Key tools**: ...
- **Mental model**: ...

## Related
- [[related-doc-1]]
```

## Section Headers (zh)

When source language is Chinese, use these section headers:
- Bug Profile → Bug 画像
- Root Cause Chain → 根因分析链
- Quick Diagnosis → 快速定位
- Prevention Checklist → 预防清单
- Debugging Methodology → 调试方法论
- Related → 相关文档
