# Claude Skills インストールガイド

## コマンドの書式について

`npx skills@latest add owner/repo/skill-name` という書き方は非対話環境（このコンテナなど）では
「No skills found」になり失敗します。正しくは次の書式です。

```
npx skills@latest add <owner>/<repo> -s <skill-name> -y
```

- `-s, --skill <skills>` : インストールするスキル名を指定
- `-y, --yes` : 確認プロンプトをスキップ

利用可能なスキル一覧は `npx skills@latest add <owner>/<repo> -l` で確認できます。
以下のコマンドは全て動作確認済みです（2026-07 時点、リポジトリの構成変更により
一部のスキル名は元のガイドから変更・削除されています。変更点は各項目に注記）。

## Meta Skills（最初に入れるべき）
```
npx skills@latest add anthropics/skills -s skill-creator -y
npx skills@latest add mattpocock/skills -s writing-great-skills -y
```
※ `write-a-skill` は `writing-great-skills` にリネームされています。

## Planning & Design
```
npx skills@latest add mattpocock/skills -s grill-me -y
npx skills@latest add mattpocock/skills -s to-prd -y
npx skills@latest add mattpocock/skills -s to-issues -y
npx skills@latest add mattpocock/skills -s design-an-interface -y
npx skills@latest add mattpocock/skills -s request-refactor-plan -y
```
※ `write-a-prd` → `to-prd`、`prd-to-issues` → `to-issues` にリネーム。
`prd-to-plan` は廃止され現在は提供されていません。

## Code Development
```
npx skills@latest add mattpocock/skills -s tdd -y
npx skills@latest add mattpocock/skills -s triage -y
npx skills@latest add mattpocock/skills -s qa -y
npx skills@latest add mattpocock/skills -s improve-codebase-architecture -y
npx skills@latest add obra/superpowers -s systematic-debugging -y
```
※ `triage-issue` → `triage` にリネーム。`obra/superpowers` は
`owner/repo` のみ指定し `-s systematic-debugging` で選択する。
`anthropics/skills/auto-commit` は現在 anthropics/skills に存在しないため削除しました。

## Tooling & Setup
```
npx skills@latest add mattpocock/skills -s setup-pre-commit -y
npx skills@latest add mattpocock/skills -s git-guardrails-claude-code -y
```

## Writing & Knowledge
```
npx skills@latest add mattpocock/skills -s edit-article -y
npx skills@latest add mattpocock/skills -s ubiquitous-language -y
npx skills@latest add mattpocock/skills -s obsidian-vault -y
```

## Frontend & Design
```
npx skills@latest add anthropics/skills -s frontend-design -y
npx skills@latest add anthropics/skills -s theme-factory -y
npx skills@latest add anthropics/skills -s web-artifacts-builder -y
```

## Office & Documents
```
npx skills@latest add anthropics/skills -s pdf -y
npx skills@latest add anthropics/skills -s docx -y
npx skills@latest add anthropics/skills -s pptx -y
npx skills@latest add anthropics/skills -s xlsx -y
```
