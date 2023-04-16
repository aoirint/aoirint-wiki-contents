---
title: Windowsの設定
description: 
published: true
date: 2023-04-16T02:05:11.906Z
tags: 
editor: markdown
dateCreated: 2022-02-07T03:12:18.451Z
---

## タスクバーの日付に曜日を表示する

コントロールパネルを開く。

「表示方法」が「カテゴリ」の場合、「日付、時刻、数値形式の変更」を開く。

「表示方法」が「小さいアイコン」の場合、「地域」を開く。

または、「ファイル名を指定して実行」から、`intl.cpl`を実行する。

「追加の設定」を開き、「日付」タブを開く。

データ形式、短い形式、の欄に`yyyy/MM/dd ddd`を入力して適用する。

- <https://laboradian.com/show-day-of-week-on-taskbar-win10/>
- <https://atmarkit.itmedia.co.jp/ait/articles/1404/25/news058.html>

## シンボリックリンク作成

管理者cmdで実行する。

```cmd
; ファイル
mklink C:\link C:\original

; ディレクトリ
mklink /D C:\link C:\original
```

## hostsファイル編集

管理者PowerShellに以下を貼り付ける。

```powershell
notepad C:\WINDOWS\system32\drivers\etc\hosts
```
