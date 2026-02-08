# github-jekyll-prac

![img](assets/img/about.jpg)

GitHub Pagesで、Jekyllを利用する練習用リポジトリー

## メモ

https://docs.github.com/ja/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll より。

- _config.yml(https://jekyllrb.com/docs/configuration/)を設定することで、jekyllを有効にできる
- site.githubを追加すると、リポジトリ参照メタデータを追加できる(https://jekyll.github.io/github-metadata/site.github/)
- テーマ https://docs.github.com/ja/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll

## ビルド済みのものをデプロイ

https://jekyllrb.com/docs/deployment/

- rsyncはいいぞ
- 基本は、_siteフォルダーをhttpserverにアップロードすれば表示できる
- GitHub Pagesで表示できないのは、リポジトリーにアップした内容がそのまま公開されるわけでなく、サイト内の相対パスが変化するため
- _config.ymlか、site.githubで調整できるか調査

## _config.yml

https://jekyllrb.com/docs/configuration/

- Site source
  - source: DIR
  - Jekyllが読み取るディレクトリを変更する
- SIte destination
  - destination: DIR
  - Jekyllがファイルを書き込む先のディレクトリ
- Safe
  - safe: BOOL
  - ホワイトリストに載ってないプラグインやディスクへのキャッシュ、シンボリックファイルを無効化する
- Disable disk cache
  - disable_disk_cache: BOOL
  - ディスクやフォルダーへのキャッシュを無効化する
  - safeにすると、自動的に有効になる
- Ignore theme configuration
  - ignore_theme_config: BOOL
  - デフォルトテーマが混じることを防ぐ
- Exclude
  - 除外するもの
- Include
  - 含めるもの
- Keep files
  - keep_files: [DIR, FILE, ...]
  - jekyllで処理しないファイル
  - destinationからの相対パスで示す
- Time zone
- Encoding
  - encoding: utf-8

## GitHub Metadata

https://jekyll.github.io/github-metadata/site.github/

- site.github ファイルで設定する
- GitHub Pagesのネームスペースやデフォルトバリューを設定するプラグイン
- [repository metadata](https://jekyll.github.io/github-metadata/site.github/)
- Gemfileに、以下を設定する

```
gem "jekyll-github-metadata"
```

- _config.ymlに、以下を加える

```
plugins:
  - "jekyll-github-metadata"
```

- bundle installを実行すると、設定できる


## 参考URL

- https://docs.github.com/ja/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll
