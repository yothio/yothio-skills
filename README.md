# yothio-skills

個人で育てている Claude Code スキルを、Claude Code の plugin marketplace 経由で他の PC（仕事用 PC など）に配布するためのリポジトリ。

## 構成

```
.claude-plugin/marketplace.json   # マーケットプレイスのカタログ
plugins/yothio/
├─ .claude-plugin/plugin.json     # プラグインのマニフェスト
└─ skills/<スキル名>/SKILL.md      # 各スキル
```

スキルは `/yothio:<スキル名>` で呼び出せる。

## インストール

```bash
claude plugin marketplace add yothio/yothio-skills
claude plugin install yothio@yothio-skills
```

更新を自動で受け取るには、`/plugin` → Marketplaces → `yothio-skills` → **Enable auto-update** を有効にする。手動で更新する場合は `/plugin marketplace update yothio-skills` を実行する。

## スキルを追加・編集したとき

```bash
claude plugin validate .
```

`plugin.json` に `version` を書いていないため、push したコミットがそのまま更新として配布される。
