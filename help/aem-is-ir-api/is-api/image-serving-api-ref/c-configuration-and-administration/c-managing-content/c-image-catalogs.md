---
description: 画像カタログには、多くのサーバー設定設定のほか、フォント、ICC プロファイル、コマンドマクロが用意されています。
solution: Experience Manager
title: 画像カタログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
TQID: 'https://experienceleague.adobe.com/kfojwk0K5RfRtZdxJmdojqsLirnP6LoXbtFRJ5272lg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# 画像カタログ{#image-catalogs}

画像カタログには、多くのサーバー設定設定のほか、フォント、ICC プロファイル、コマンドマクロが用意されています。

リクエストで使用される画像と静的コンテンツ idを実際のファイルパスにマッピングし、画像マップなどのさまざまな画像メタデータを保存し、テンプレートと画像セットのコンテナを提供します。

画像カタログには、[!DNL Platform Server]のみがアクセスでき、Image Serverからはアクセスできません。 カタログ属性ファイルには.ini サフィックスを付け、[!DNL Platform Server]のカタログフォルダー（`PS::CatalogFolder`）に配置する必要があります。 少なくともデフォルトの画像カタログが必要です。[!DNL Platform Server]を正しく機能させるには、すべての属性を入力する必要があります。
