---
description: 画像カタログの管理に関する設定が含まれています。
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
TQID: 'https://experienceleague.adobe.com/GdtVY3WMO9F6C5vzkOHdVoMW-f6-L1cJGUt1KUCvLJ8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

画像カタログの管理に関する設定が含まれています。

このファイルはJAVA プロパティファイルです。 適切な規則に従うように注意する必要があります。そうしないと、[!DNL Platform Server]を開始できない可能性があります。 Windows ファイルパスでは、バックスラッシュ「\」の代わりに、ダブルバックスラッシュ「\\」または1つのフォワードスラッシュ「/」を使用します。 バックスラッシュは、このタイプのファイルではエスケープ文字として使用されます。

このファイルへの変更は、ファイルが保存された直後に有効になります。

[!DNL catalog-service.conf]で変更できるのは、以下に示す設定のみです。 特定の設定がない場合は、ファイル内の任意の場所に追加できます。 各設定のインスタンスは1つだけ存在できます。

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
