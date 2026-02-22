# claude-shared-rules

共有Claude Codeルール。全リポジトリの `.claude/rules/shared/` にsubmoduleとして追加することで、
ローカルCLI・Claude Code on the web 両環境でルールを共有できる。

## 使い方

```bash
# 各リポジトリへの追加
git submodule add https://github.com/MasatoshiToku/claude-shared-rules .claude/rules/shared

# 更新
git submodule update --remote --merge
```

## ファイル構成

| ファイル | 内容 |
|---------|------|
| `coding-style.md` | イミュータビリティ、ファイル構成、エラーハンドリング |
| `git-workflow.md` | コミット規約、PRワークフロー、TDD |
| `testing.md` | テストカバレッジ要件、TDDワークフロー |

## 仕組み

Claude Codeは `.claude/rules/` 配下の `.md` ファイルを自動読み込みする（CLI・Web両対応）。
submoduleとして追加することで、Web環境のVMにもファイルが物理的に展開される。
