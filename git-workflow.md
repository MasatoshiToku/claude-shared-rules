# Git Workflow

## Commit Message Format

```
<type>: <description>

<optional body>
```

Types: feat, fix, refactor, docs, test, chore, perf, ci

## Pull Request Workflow

When creating PRs:
1. Analyze full commit history (not just latest commit)
2. Use `git diff [base-branch]...HEAD` to see all changes
3. Draft comprehensive PR summary
4. Include test plan with TODOs
5. Push with `-u` flag if new branch

## Feature Implementation Workflow

0. **GitHub Issue 作成**
   - 作業開始と同じセッション内に Issue を作成する
   - 完了条件（チェックリスト）を必ず記載

1. **Plan First**
   - Implementation plan を作成
   - Identify dependencies and risks

2. **TDD Approach**
   - Write tests first (RED)
   - Implement to pass tests (GREEN)
   - Refactor (IMPROVE)
   - Verify 80%+ coverage

3. **Code Review**
   - CRITICAL/HIGH問題は必ず修正
   - MEDIUM問題も可能な限り対応

4. **Commit & Push**
   - Detailed commit messages
   - Follow conventional commits format

5. **GitHub Issue クローズ**
   - 完了条件が全て満たされていることを確認してからクローズ
