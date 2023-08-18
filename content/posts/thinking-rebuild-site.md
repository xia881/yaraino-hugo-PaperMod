---
title: "再構築に向け、手持ちサイト構成やサーバー整理について考える"
date: 2022-04-06
tags: ["さくらサーバー","gatsby.js","AdSense","ドメイン管理"]
showToc: true
TocOpen: false
draft: false
ShowBreadCrumbs: true
ShowPostNavLinks: true
UseHugoToc: true
description: "可能な限り安く、多くサイトを運用したい、そして広告運用したい。"
---

## AdSense利用にはオリジナルドメインが必須

gatsby.ioはオリジナルドメインではない

### オリジナルドメインを持っているか？

私は、さくらインターネットを経由して持っている

### gatsby.jsでの操作

メニュー `Use your own domain`

フリープランならオリジナルドメインを1個だけ、追加で接続できる

gatsbyjsマイページトップ＞対象サイト＞site settings＞Hosting＞Domains

`「Please enter a domain (required)」`に従い入力  
saveすると、Aレコードを変更してこい、とのこと

### さくらインターネット

※独自ドメインと思っていたら、さくらのレンタルサーバー契約時に1個サービスで作れた？ドメインを指定するとCNAMEを変更しろ、とのこと

言われるがままにドメインのゾーン情報（私はさくらインターネットの **ドメインコントローパネル** からAレコードを上書き。後に戻した）を変更  
←？この自分のメモ、何かおかしいな…

### ゾーン情報を変更したらgatsbyに戻る

varidateボタン（的な）を押すと、少し待つ。ぐるぐる…varidateとかしている感

完了っぽくなると、サイトURLが2個（www有無で）増えて表示されるようになる

例えば、下記の3種のように。

- ○○○.gatsby.io
- ▲▲▲.com
- www.▲▲▲.com

これらいずれを押しても、○○○.gatsby.io（になると思って開発を始めたはず）の内容が表示される。

### 私のケースで一番感じたこと

さくらインターネットのサブドメインのゾーン編集ができたらなあ。