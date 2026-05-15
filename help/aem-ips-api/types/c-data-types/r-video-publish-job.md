---
description: 設定されたビデオ公開サーバーにファイルを公開します。
solution: Experience Manager
title: VideoPublishJob
feature: Dynamic Media Classic,SDK/API,Video
role: Developer,Admin
exl-id: 4b295025-6e8d-4329-87c1-63633bf26129
TQID: 'https://experienceleague.adobe.com/4JE8narY9liZMaPyfM1sQz1kWLqPIDcWij1uoNGhFN8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 40
ht-degree: 10%

---

# [!DNL VideoPublishJob]{#videopublishjob}

設定されたビデオ公開サーバーにファイルを公開します。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| emailSetting | `xsd:string` | メール設定の選択。 |
| httpCompletionUrl | `xsd:string` | 完了通知を送信するURL。 |
| contextHandle | `xsd:string` | 公開コンテキストに対応します。 |
