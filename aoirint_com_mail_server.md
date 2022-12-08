---
title: aoirint.com メールサーバについて
description: 
published: true
date: 2022-12-08T22:08:51.358Z
tags: 
editor: markdown
dateCreated: 2022-12-08T21:35:02.630Z
---

# aoirint.com メールサーバ

2022-12-09より、aoirint.comにて、メールサーバの運用を始めました。

aoirint.comアドレス宛てにメールが送信できない、受信できない、不正中継されている、セキュリティ上の問題などがあれば、TwitterやMastodonなどにご連絡ください。

## 更新履歴

- 2022-12-09 運用開始

## セキュリティ対策

本サーバとMUA間の通信は、STARTTLS/暗黙的TLSにより暗号化されます（必須）。

本サーバとMTA間の通信は、STARTTLS/暗黙的TLSにより暗号化されます（必須）。
2022年12月現在、STARTTLS/暗黙的TLSのいずれにも対応しないMTAとの通信はしない方針です。

2022年12月現在、PGP鍵によるE2E暗号化の導入を検討中です。


## 構成

### DNS

DNSでは、MXレコード、SPFレコードを設定しています。

### 外部からのメールを内部に転送するSMTPサーバ mx01.aoirint.com

#### SMTP

|||
|:--|:--|
|暗号化|STARTTLS（必須）|
|認証|なし|
|ホスト名（TLS証明書のコモンネーム）|mx01.aoirint.com|
|ポート番号|25|
|外部へのメール送信|禁止|

#### SMTPS

|||
|:--|:--|
|暗号化|暗黙的TLS|
|認証|なし|
|ホスト名（TLS証明書のコモンネーム）|mx01.aoirint.com|
|ポート番号|465|
|外部へのメール送信|禁止|


### 外部にメールを送信するSMTPサーバ smtp.aoirint.com

#### Submission

|||
|:--|:--|
|暗号化|STARTTLS（必須）|
|認証|平文パスワード|
|ホスト名（TLS証明書のコモンネーム）|smtp.aoirint.com|
|ポート番号|587|
|外部へのメール送信|許可（認証必須）|


### IMAPサーバ imap.aoirint.com

##### IMAPS

|||
|:--|:--|
|暗号化|暗黙的TLS|
|認証|平文パスワード|
|ホスト名（TLS証明書のコモンネーム）|imap.aoirint.com|
|ポート番号|993|

### POP3サーバ pop.aoirint.com

#### POP3S

|||
|:--|:--|
|暗号化|暗黙的TLS|
|認証|平文パスワード|
|ホスト名（TLS証明書のコモンネーム）|pop.aoirint.com|
|ポート番号|995|

