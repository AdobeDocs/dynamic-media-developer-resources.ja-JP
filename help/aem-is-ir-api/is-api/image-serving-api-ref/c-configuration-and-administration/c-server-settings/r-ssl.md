---
description: SSLの場合は、次のサーバー設定を使用します。
seo-description: SSLの場合は、次のサーバー設定を使用します。
seo-title: SSL
solution: Experience Manager
title: SSL
topic: Scene7 Image Serving - Image Rendering API
uuid: dec9bd09-8191-4010-8898-2890ffbe9ca7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 7%

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
