---
description: SSLの場合は、次のサーバー設定を使用します。
seo-description: SSLの場合は、次のサーバー設定を使用します。
seo-title: SSL
solution: Experience Manager
title: SSL
uuid: dec9bd09-8191-4010-8898-2890ffbe9ca7
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 6%

---


# SSL{#ssl}

SSLの場合は、次のサーバー設定を使用します。

## TC::SslPort — リスニングポート{#section-c80eb582bf684b3fa7313a77cc606769}

SSL接続用のプラットフォームサーバーのリスニングポートを指定します。 初期設定は 8443 です

## TC::keystoreFile — キーストアファイルのパス{#section-0cdf9b3cfcf249818b22221d01bafebe}

SSLキーストアファイルのパスまたは名前を指定します。 絶対パスまたは[!DNL *[!DNL install_folder]*/conf]に対する相対パスを指定できます。 初期設定は&#x200B;*install_folder*/conf/scene7keystoreです。

## TC::keystorePass — キーストアパスワード{#section-e7e9bfb7df584a248c0e3ee46803c3b1}

キーストアファイルのパスワードです。 初期設定は `scene7`.

## TC::keystoreType — キーストアの種類{#section-8f263e1ba67740728cd39181960d7c7d}

キーストアのタイプを選択します。 &#39; `Java'` （デフォルト）と&#39; `PKCS12`&#39;がサポートされます。
