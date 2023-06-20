---
title: "How to Create a Serverless Static Site"
date: 2023-06-20T16:00:29+09:00
# weight: 1
# aliases: ["/first"]
tags: ["first"]
# author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Desc Text."
# canonicalURL: "https://canonical.url/to/page"
# disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true

# cover:
#    image: "<image path/url>" # image path/url
#    alt: "<alt text>" # alt text
#    caption: "<text>" # display caption under cover
#    relative: false # when using page bundles set this to true
#    hidden: true # only hide on current single page

# editPost:
#    URL: "https://github.com/<path_to_repo>/content"
#    Text: "Suggest Changes" # edit text
#    appendFilePath: true # to append file path to Edit link
---

- hugo + GitHub Pages + テキストメイン

GitHubActionsの設定でつまずいたが、まあできた

- hugo + vercel & テキストメイン

爆速

- Python Flask + vercel & 画像データ

apiディレクトリすぐ満タンになる問題、htmlとmd増えるストレス

- Gatsby ( + Gatsby cloud)

処理が遅い、記事ごとにディレクトリが増えてストレス

## byproduct

新記事追加のとき、つまり
`hugo new ...md`するとき、に便利

例えば
`echo "How to create a serverless static site" | sed -e 's/ /-/g'`
