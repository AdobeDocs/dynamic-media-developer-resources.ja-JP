---
description: SSL 用に次のサーバー設定を使用します。
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 6%

---

# SSL{#ssl}

SSL 用に次のサーバー設定を使用します。

## TC::SslPort — リスニングポート {#section-c80eb582bf684b3fa7313a77cc606769}

リスニングポートを [!DNL Platform Server] （SSL 接続用） 初期設定は 8443 です

## TC::keystoreFile — キーストアのファイルパス {#section-0cdf9b3cfcf249818b22221d01bafebe}

SSL キーストアファイルのパスまたは名前を指定します。 [!DNL *[!DNL install_folder]*/conf] を設定します。 デフォルトはです。 *install_folder*/conf/scene7keystore.

## TC::keystorePass — キーストアのパスワード {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

キーストアファイルのパスワード。 初期設定は `scene7`.

## TC::keystoreType — キーストアの種類 {#section-8f263e1ba67740728cd39181960d7c7d}

キーストアのタイプを選択します。 &#39; `Java'` （デフォルト）と&#39; `PKCS12`&#39;はサポートされています。
