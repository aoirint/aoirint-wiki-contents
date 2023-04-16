---
title: Gitの改行コード自動置換機能を無効化する
description: 
published: true
date: 2023-04-16T06:58:39.196Z
tags: 
editor: markdown
dateCreated: 2023-04-16T06:58:39.196Z
---


## Git for WindowsのCRLF自動置換機能のためにDocker Buildに失敗する例

改行コードCRLFで以下のようなDockerfileを作成すると、

```dockerfile
# syntax=docker/dockerfile:1.4

FROM ubuntu:22.04

RUN <<EOF
    set -eux

    echo "OK"
EOF
```

```
#0 0.604 /bin/sh: 1: set: Illegal option -
```


