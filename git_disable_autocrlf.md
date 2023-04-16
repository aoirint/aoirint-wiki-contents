---
title: Gitの改行コード自動置換機能を無効化する
description: 
published: true
date: 2023-04-16T07:02:30.917Z
tags: 
editor: markdown
dateCreated: 2023-04-16T06:58:39.196Z
---


## GitのCRLF自動置換機能のためにDocker Buildに失敗する例

改行コードCRLFで以下のようなDockerfileを作成すると、

```dockerfile
# syntax=docker/dockerfile:1.4

FROM ubuntu:22.04

RUN <<EOF
    set -eux

    echo "OK"
EOF
```

以下のようなエラーとなり、ビルドに失敗します。

```
------
 > [2/2] RUN <<EOF (set -eux...):
#8 0.294 /bin/sh: 1: set: Illegal option -
------
executor failed running [/bin/sh -c     set -eux

    echo "OK"
]: exit code: 2
```

GitのCRLF自動置換機能によって、Dockerfileの改行コードがCRLFに書き換えられることでも同じことが起きます。
Linuxの仮想化ソフトウェアであるDockerの構成ファイルにCRLFが使われることが想定されないのは理解できます。

`.gitattributes`でリポジトリごとに改行コードのポリシーを変更することができますが、~~令和の時代に改行コードの切り替えができないテキストエディタを使うこともないと思われるので、~~
