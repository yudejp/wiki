---
title: 現在開いているページを Twitter にシェアするブックマークレット
description: 
published: true
date: 2022-01-27T05:02:24.390Z
tags: javascript
editor: markdown
dateCreated: 2022-01-27T05:02:24.390Z
---

## コード
```javascript
javascript: (function () {window.open("https://twitter.com/intent/tweet?url=" + encodeURIComponent(location.href) + "&text=" + encodeURIComponent(document.title),"_blank", "width=600,height=300");})(); 
```
* 参考: [JavaScript  ブックマークレット 現在のページをTwitterにシェアする用のブックマークレットを作成 - Qiita](https://qiita.com/koara-local/items/3e4bdcf1f929e619344c)