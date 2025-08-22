# 東海サマーワークショップ2025 公式サイト

東海地区の大学研究室有志による研究発表会の公式サイトです。

## サイト構成

- Jekyll + GitHub Pagesで構築
- マテリアルデザインを意識したシンプルで洗練されたデザイン
- レスポンシブ対応

## ディレクトリ構造

```
tsw2025/
├── _data/               # データファイル（YAML形式）
│   ├── event_info.yml   # イベント基本情報
│   ├── schedule.yml     # プログラムスケジュール
│   ├── important_dates.yml # 重要な日程
│   ├── registration_info.yml # 参加登録情報
│   ├── venue_info.yml   # 会場情報
│   └── contact_info.yml # お問い合わせ情報
├── _news/               # お知らせ（Markdownファイル）
├── _layouts/            # レイアウトテンプレート
├── _sass/               # スタイルシート
└── assets/              # 画像、CSS、JSファイル
```

## 情報の編集方法

### 1. カルーセル（スライドショー）の編集
`_data/carousel.yml` を編集してください。
- 画像URL、タイトル、キャプションを設定
- 自動再生の設定（autoplay, interval）
- インジケーターや矢印の表示設定

### 2. イベント基本情報の変更
`_data/event_info.yml` を編集してください。
- 開催日時、参加費、発表形式などの基本情報

### 3. スケジュールの変更
`_data/schedule.yml` を編集してください。
- 各日のセッション情報（時間、タイトル、発表者など）

### 4. お知らせの追加
`_news/` ディレクトリに新しいMarkdownファイルを作成してください。

ファイル名の形式: `YYYY-MM-DD-title.md`

例: `_news/2025-07-01-registration-open.md`
```markdown
---
title: "参加登録を開始しました"
date: 2025-07-01
category: announcement
---

参加登録フォームを公開しました。締切は8月31日です。
```

draftにする場合は `draft: true` を追加してください。

### 5. 各ページの内容変更

各ページはMarkdownファイルとデータファイルの組み合わせで構成されています：

- `index.md` - トップページ（_data/event_info.yml、_data/important_dates.ymlを使用）
- `about.md` - 開催概要（_data/event_info.ymlを使用）
- `program.md` - プログラム（_data/schedule.yml、_data/event_info.ymlを使用）
- `registration.md` - 参加登録（_data/registration_info.yml、_data/event_info.ymlを使用）
- `venue.md` - 会場（_data/venue_info.ymlを使用）
- `contact.md` - お問い合わせ（_data/contact_info.ymlを使用）
- `privacy.md` - プライバシーポリシー

### 6. 重要な日程の変更
`_data/important_dates.yml` を編集してください。

### 7. 参加登録情報の変更
`_data/registration_info.yml` を編集してください。
- 締切日、フォームURL、注意事項など

### 8. 会場情報の更新
`_data/venue_info.yml` を編集してください。
- 会場が決定したら、statusを変更し、詳細情報を追加

### 9. お問い合わせ情報の変更
`_data/contact_info.yml` を編集してください。
- 連絡先、FAQ、お問い合わせ例など

### 10. 過去のワークショップリンクの管理
`_data/past_workshops.yml` を編集してください。
- 年度、名称、URL、開催校を設定
- 新しいワークショップは上に追加（新しい順）
- オンライン開催などの注記も追加可能

## ローカル環境での確認

1. Ruby と bundler をインストール
2. 依存関係をインストール:
   ```bash
   bundle install --path vendor/bundle
   ```
3. サーバーを起動:
   ```bash
   bundle exec jekyll serve
   ```
4. ブラウザで `http://localhost:4000/tsw2025/` にアクセス

## GitHub Pagesへの公開

1. このリポジトリをGitHubにプッシュ
2. Settings > Pages で Source を "Deploy from a branch" に設定
3. Branch を main、フォルダを / (root) に設定

## 注意事項

- `_config.yml` の `baseurl` はリポジトリ名に合わせて変更してください
- 画像を追加する場合は `assets/images/` ディレクトリに配置してください
- スタイルを変更する場合は `_sass/main.scss` を編集してください