---
title: "Data convert from html to Markdown by Node.js"
date: 2022-04-18
tags: ["tools","Node.js"]
showToc: true
TocOpen: false
draft: false
ShowBreadCrumbs: true
ShowPostNavLinks: true
UseHugoToc: true
description: "ローカル環境で、Node.jsを用いて、htmlをMarkdownに変換する方法"
---

In the local environment,  
convert each html file  
to a Markdown file  
and save it under a different name.

## Things necessary

Prepare in the same directory.

- index.js
- directory: convert_from
- directory: convert_after
- directory: node_modules

### directory: convert_from

Store the source html files here.

### directory: convert_after

Here, the converted Markdown files will be generated.

### directory: node_modules

The modules that require `npm install` are:

- turndown
- glob

### index.js

```js
const fs = require("node:fs");
const path = require('node:path');

const TurndownService = require('turndown');
const glob = require('glob');

const html2md = (html) => {
    const turndownService = new TurndownService({
      headingStyle: "atx",
      bulletListMarker: "-",
      codeBlockStyle: "fenced",
    });
return turndownService.turndown(html);
};

const main = () => {
    
    glob('./convert_from/*.html', (err, files) => {
        files.forEach(file => {
            const filename= path.basename(file, '.html');
            const html = fs.readFileSync(file, 'utf-8');
            const md = html2md(html);
            fs.writeFileSync(`./convert_after/${filename}.md`, md, 'utf-8');
        });
    });

};

main();
```