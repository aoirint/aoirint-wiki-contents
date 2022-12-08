---
title: aoirint.com メールサーバについて
description: 
published: true
date: 2022-12-08T21:42:38.099Z
tags: 
editor: markdown
dateCreated: 2022-12-08T21:35:02.630Z
---

# aoirint.com メールサーバ

2022-12-09より、aoirint.comにて、メールサーバの運用を始めました。

aoirint.comアドレス宛てにメールが送信できない、受信できない、スパムメールなどがあれば、TwitterやMastodonなどにご連絡ください。

## 設定

### 外部からのメールを内部に転送するSMTPサーバ mx01.aoirint.com

#### SMTP

|||
|:--|:--|
|暗号化|STARTTLS（必須）|
|認証|なし|
|ホスト名（TLS証明書のコモンネーム）|mx01.aoirint.com|
|ポート番号|25|

#### SMTPS

|||
|:--|:--|
|暗号化|暗黙的TLS|
|認証|なし|
|ホスト名（TLS証明書のコモンネーム）|mx01.aoirint.com|
|ポート番号|465|


### 外部にメールを送信するSMTPサーバ smtp.aoirint.com

|||
|:--|:--|
|暗号化|STARTTLS（必須）|
|認証|平文パスワード|
|ホスト名（TLS証明書のコモンネーム）|smtp.aoirint.com|
|ポート番号|587|

### IMAPサーバ imap.aoirint.com


### POP3サーバ pop3.aoirint.com

