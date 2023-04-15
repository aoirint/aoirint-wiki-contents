---
title: NovelAI Leak Model
description: 
published: true
date: 2023-04-15T05:43:46.205Z
tags: 
editor: markdown
dateCreated: 2023-04-15T05:27:01.754Z
---

NovelAIは、2022年10月に独自のStable Diffusion派生モデルによる画像生成サービスをリリースした。

- [Image Generation has arrived, NovelAI Diffusion is here! | Medium](https://blog.novelai.net/image-generation-announcement-807b3cf0afec)

しかし、このサービスに使われているとみられる生成モデルが流出してしまった。

- `animefull-final-pruned`: sha256 `925997e9`
- `animesfw-final-pruned`: sha256 `1d4a34af`
- `animevae.pt`: sha256 `f921fb3f`

Stable Diffusion派生の異なるモデルを合成する、モデルマージと呼ばれる手法など、
様々な手法により生まれた「NAIリーク派生モデル」とみられるモデルが流通してしまっている。

## 関連項目

- [AIアート](/aiart)
