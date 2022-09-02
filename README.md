# Rails ToDo アプリ

## Environment

### 開発環境

```
> uname -a
Linux labpixel-vbox 5.15.0-46-generic #49-Ubuntu SMP Thu Aug 4 18:03:25 UTC 2022 x86_64 x86_64 x86_64 GNU/Linux
```

### 環境構築

以下を参考にしました。
https://qiita.com/Gushi_maru/items/f3b5cc43e135e678085f

Fishの場合は`~/.config/fish/config.fish`に以下を書き込む。

```
export PATH="$HOME/.rbenv/bin:$PATH"
eval "$(rbenv init -)"
```

よって必須環境は以下の通り

|APP|INFO|
|---|---|
|rbenv|Rubyパッケージ管理ツール|
|Ruby|Buby本体|
|SQLite|SQLサーバー|
|Node.js|JS|

## ToDo

### master

とりあえず一般機能の実装を急ぐ

- 追加ページのスタイルシート
- 編集ページのスタイルシート

### feat_#1

日付と重要度を追加する

- 日付追加
- 重要度追加

### feat_#2

ログイン機能の実装

## Develop Memo

### プロジェクト作成

```bash
> rails new RailsToDoApp
```

### モデル作成

> モデルはDBとやり取りする

```bash
# モデルを作成する
> rails generate model Task title:string

# モデルをDBに反映させる
> rails db:migrate
```

### コントローラー作成

> コントローラはリクエストとレスポンスの管理をする

```bash
> rails generate controller Tasks
```

注意）コントローラー名は複数形にする
