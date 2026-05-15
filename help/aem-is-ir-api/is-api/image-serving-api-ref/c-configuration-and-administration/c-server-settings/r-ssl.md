---
description: これらのサーバー設定をSSLに使用します。
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
TQID: 'https://experienceleague.adobe.com/VOdDIzV6b9J9AZ-qZyAj3AI77MukT1BbSzM-UM-B5N4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 2%

---

# SSL{#ssl}

これらのサーバー設定をSSLに使用します。

## TC::SslPort - リスニングポート {#section-c80eb582bf684b3fa7313a77cc606769}

SSL接続の[!DNL Platform Server]のリッスン ポートを指定します。 デフォルトは8443です。

## TC::keystoreFile - キーストアファイルパス {#section-0cdf9b3cfcf249818b22221d01bafebe}

SSL キーストアファイルのパスと名前を指定します。 [!DNL *[!DNL install_folder]*/conf]に対する絶対パスまたは相対パスである可能性があります。 デフォルトは&#x200B;*install_folder*/conf/scene7keystoreです。

## TC::keystorePass - キーストアパスワード {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

キーストアファイルのパスワード。 デフォルトは`scene7`です。

## TC::keystoreType - キーストアタイプ {#section-8f263e1ba67740728cd39181960d7c7d}

キーストアのタイプを選択します。 &#39;`Java'` （既定値）と&#39; `PKCS12`&#39;がサポートされています。
