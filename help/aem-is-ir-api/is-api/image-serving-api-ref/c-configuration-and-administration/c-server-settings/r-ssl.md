---
description: SSL用の次のサーバー設定を使用します。
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 6%

---

# SSL{#ssl}

SSL用の次のサーバー設定を使用します。

## TC::SslPort — リッスンポート {#section-c80eb582bf684b3fa7313a77cc606769}

SSL接続用のPlatform Serverのリスニングポートを指定します。 初期設定は 8443 です

## TC::keystoreFile — キーストアのファイルパス {#section-0cdf9b3cfcf249818b22221d01bafebe}

SSLキーストアファイルのパスまたは名前を指定します。 絶対パスまたは[!DNL *[!DNL install_folder]*/conf]に対する相対パスを指定できます。 初期設定は&#x200B;*install_folder*/conf/scene7keystoreです。

## TC::keystorePass — キーストアのパスワード {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

キーストアファイルのパスワード。 初期設定は `scene7`.

## TC::keystoreType — キーストアの種類 {#section-8f263e1ba67740728cd39181960d7c7d}

キーストアのタイプを選択します。 「 `Java'` 」（デフォルト）と「 `PKCS12` 」がサポートされています。
