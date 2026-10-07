# localhost プレビュー

## 環境構築

- 対象環境：WSL の Ubuntu
- ネットワーク接続：初回の gem インストール、Remote Theme の取得に必要
- WSL の端末で実行

```bash
sudo apt-get update
sudo apt-get install ruby ruby-dev ruby-bundler build-essential
ruby --version
bundle --version
```

## 実行

- リポジトリのルートで実行

```bash
./bin/preview
```

- ブラウザで [http://localhost:4000/docs/](http://localhost:4000/docs/) を表示
- ページの編集後：自動再生成・ブラウザの自動リロード
- `_config.yml` の変更後：プレビューを再起動
- 終了：起動した端末で `Ctrl+C`
- 起動処理・依存定義の参照先：[bin/preview](../bin/preview)、[Gemfile](../Gemfile)、[Gemfile.lock](../Gemfile.lock)

## 確認・公開

- localhost：PC・スマートフォン相当の幅で表示、地図・SNS・メールのリンクを確認
- PR：`main` 宛てに作成、CI の成功を確認
- 本番：レビュー・マージ後に Pages のデプロイ結果と公開ページを確認

## 起動できない場合

- apt の取得先が 404：`sudo apt-get update` 後にインストールを再実行
- ポート 4000 が使用中：既存のプレビューを終了して再実行
- 公開設定・生成対象の参照先：[_config.yml](../_config.yml)
