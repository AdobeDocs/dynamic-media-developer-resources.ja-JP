---
description: これらのサーバー設定を SSL に使用します。
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---

# SSL{#ssl}

これらのサーバー設定を SSL に使用します。

## TC::SslPort - リスニングポート {#section-c80eb582bf684b3fa7313a77cc606769}

SSL 接続用の [!DNL Platform Server] のリスニング ポートを指定します。 初期設定は 8443。

## TC::keystoreFile - キーストアファイルのパス {#section-0cdf9b3cfcf249818b22221d01bafebe}

SSL キーストアファイルのパスと名前を指定します。 絶対パスまたは [!DNL *[!DNL install_folder]*/conf] からの相対パスを指定できます。 デフォルトは *install_folder*/conf/scene7keystore です。

## TC::keystorePass - キーストアのパスワード {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

キーストアファイルのパスワード。 デフォルトは `scene7` です。

## TC::keystoreType - キーストアタイプ {#section-8f263e1ba67740728cd39181960d7c7d}

キーストアのタイプを選択します。 「`Java'` （デフォルト）」と「`PKCS12`」がサポートされています。
