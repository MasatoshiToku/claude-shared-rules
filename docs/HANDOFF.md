# Handoff - claude-shared-rules

Last Updated: 2026-03-15T00:00+09:00

## Current State

Claude Code 共有ルールの配布リポジトリ。各リポジトリの `.claude/rules/shared/` に git submodule として追加し、ローカル CLI と Claude Code on the web の両環境でルールを共有する。現在 3 ファイル構成: coding-style.md（イミュータビリティ、ファイル構成、エラーハンドリング）、git-workflow.md（コミット規約、PR ワークフロー、TDD）、testing.md（テストカバレッジ要件、TDD ワークフロー）。

## In Progress

- なし（初期作成）

## Blocked / Needs Attention

- なし

## Recent Decisions

| 日付 | 決定 | 理由 | Ref |
|------|------|------|-----|

## Known Issues

- なし

## For New Team Members

- **技術スタック**: Markdown のみ
- **ローカル開発**: 直接 .md ファイルを編集。各リポジトリでは `git submodule add https://github.com/MasatoshiToku/claude-shared-rules .claude/rules/shared` で追加
- **デプロイ**: git push のみ。消費側は `git submodule update --remote --merge` で更新
- **重要な規約**: Claude Code は `.claude/rules/` 配下の `.md` ファイルを自動読み込みする。ファイル名・構造の変更は全リポジトリに影響する
