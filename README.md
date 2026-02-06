# github-jekyll-prac
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



## 参考URL

- https://docs.github.com/ja/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll
