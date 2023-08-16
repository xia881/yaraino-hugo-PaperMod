---
title: "Hugo + GitHub Pages を用いたサーバーレスな静的サイトの作り方"
date: 2023-06-20T16:00:29+09:00
tags: ["Hugo","GitHub Pages"]
showToc: true
TocOpen: false
draft: false
ShowBreadCrumbs: true
ShowPostNavLinks: true
UseHugoToc: true
description: "記事の新規追加が劇的に楽になりました"
---

- Hugo + GitHub Pages + テキストメイン

GitHubActionsの設定でつまずいたが、まあできた

- Hugo + vercel & テキストメイン

爆速

- Python Flask + vercel & 画像データ

apiディレクトリすぐ満タンになる問題、htmlとmd増えるストレス

- Gatsby ( + Gatsby cloud)

処理が遅い、記事ごとにディレクトリが増えてストレス

## chips

新記事追加のとき、つまり
`hugo new ...md`するとき、に便利

例えば
`echo "How to create a serverless static site" | sed -e 's/ /-/g'`
