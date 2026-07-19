# Scrapling Agent Workspace

Codex用のプロジェクト基盤に、D4Vinci/ScraplingのAgent Skillと実行環境を追加したワークスペースです。

## セットアップ済み

- Python仮想環境: `.venv/`
- Scrapling: `0.4.11`（`scrapling[all]`）
- Playwright / Patchrightブラウザ依存関係
- Agent Skill: `agent-skill/Scrapling-Skill/`
- プロジェクトルール: `AGENTS.md`
- エージェント設定用ディレクトリ: `.agents/`、`.codex/`

## 使い方（PowerShell）

```powershell
.\.venv\Scripts\Activate.ps1
scrapling --help
```

Pythonコードから使う場合も、同じ仮想環境を有効化して実行します。

```powershell
python -c "from scrapling import Selector; print(Selector('<h1>Hello</h1>').css('h1::text').get())"
```

## リポジトリ構成

- `.agents/` — プロジェクト固有のエージェントメタデータ
- `.codex/` — Codex固有の設定
- `agent-skill/Scrapling-Skill/` — ScraplingのAgent Skill
- `AGENTS.md` — このプロジェクトで作業するエージェント向けルール
- `work/Scrapling-source/` — 参照用に取得した公式リポジトリ（作業用）

## 注意

`.venv/`、`work/`、キャッシュ、秘密情報はGitにコミットしません。変更を共有する場合は、必要な設定・Skill・ドキュメントだけをコミットしてください。
