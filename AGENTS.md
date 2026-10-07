# 作業ワークフロー

- 着手前：既存ファイル・Git の変更状況を確認、作業途中の変更を保持
- 環境構築・プレビューの起動時：[docs/local-preview.md](docs/local-preview.md) を参照
- ページ更新時：localhost で表示・リンクを確認、PC・スマートフォン相当の幅で確認
- GitHub 操作時：Sandbox 外の対話シェルを使用、同じシェルで `gh api user --hostname github.com --jq .login` が `keyakisepak` であることを確認
- 変更提出時：`main` 宛ての PR を作成、CI の成功を確認
- 公開検証時：Pages の公開元は `main`、検証ブランチを公開対象に追加しない
- マージ後：Pages のデプロイ結果と公開ページを確認
- 開発用資料：`docs/` と `AGENTS.md` を Pages の生成対象から除外
- 文書化：作業履歴・経緯メモは保存せず、実装の詳細はコードを参照
