---
author: "James Zhou"
date: 2023-04-28
linktitle: "Feat: Pangu JS"
menu:
  main:
    parent:
next:
prev:
title: "Feat: Pangu JS"
weight: 10
---

## 简介

我们给hugo-book主题注入了一个新的模组 - Pangu JS。

[![pangu.js Git Card](https://github-readme-stats.jamesflare.com/api/pin/?username=vinta&repo=pangu.js&theme=github_dark_dimmed&show_owner=true)](https://github.com/vinta/pangu.js/)

它的功能很简单，在中文和英文/数字字符中添加一个空格。

```
//输入
不能信任那些Terminal或Editor用白底的人
//输出
不能信任那些 Terminal 或 Editor 用白底的人
```

## 操作

hugo-book在layouts/partials/docs/inject/目录有控制注入的文件。

我们在它下面创建一个body.html，填入：

```
{{- /* PanguJS */ -}}
{{- if eq .Site.Params.pangu.enable true -}}
  <script src="/js/pangu.min.js"></script>
  <script>pangu.spacingPage();</script>
{{- end -}}
```

接下来在static/js/下创建一个叫pangu.min.js的文件，内容就是[pangu.min.js](https://cdnjs.cloudflare.com/ajax/libs/pangu/4.0.7/pangu.min.js)本身。