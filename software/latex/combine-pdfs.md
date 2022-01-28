---
title: 複数の PDF ファイルを結合する
description: 
published: true
date: 2022-01-28T07:08:51.884Z
tags: latex, pdf
editor: markdown
dateCreated: 2022-01-28T07:08:51.884Z
---

1. 以下の内容を適宜変更する。 (英数字じゃないとダメかも)
```
\documentclass[flegn]{article}
\usepackage{pdfpages}
\begin{document}
\includepdf[pages=-]{1.pdf}
\includepdf[pages=-]{2.pdf}
\includepdf[pages=-]{3.pdf}
\includepdf[pages=-]{4.pdf}
\includepdf[pages=-]{5.pdf}
\includepdf[pages=-]{6.pdf}
\includepdf[pages=-]{7.pdf}
\includepdf[pages=-]{8.pdf}
\includepdf[pages=-]{9.pdf}
\end{document}
```
2. LaTeX のファイル形式 `.tex` で保存する。
3. `pdflatex (filename).tex` を実行する。