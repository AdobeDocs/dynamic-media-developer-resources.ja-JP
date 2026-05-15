---
description: 画像レンダリングのソースデータファイルには、ビネットファイル、マテリアルファイル（繰り返し可能なテクスチャやデカール用の画像、キャビネットやウィンドウをカバーするスタイルファイル）、ICC プロファイルなどがあります。
solution: Experience Manager
title: Source data
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
TQID: 'https://experienceleague.adobe.com/lvrZxGOZbo6ORttqcBhCTuYPzbiD9xei5qkRwnapIh8'
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
source-wordcount: 258
ht-degree: 0%

---

# Source data{#source-data}

画像レンダリングのソースデータファイルには、ビネットファイル、マテリアルファイル（繰り返し可能なテクスチャやデカール用の画像、キャビネットやウィンドウをカバーするスタイルファイル）、ICC プロファイルなどがあります。

すべてのソースデータファイルは、Image Renderingのネイティブコードコンポーネント（Image Serverと共同で配置）からアクセスできる必要があります。

マテリアル カタログが含まれている場合、マテリアル カタログで指定されたファイル（`vignette::Path`、`catalog::Path`または`icc::ProfilePath`）は、次のようにレンダーサーバーによって検索されます。

* パスが絶対パスの場合は、そのまま使用されます。
* パスが相対パスの場合は、先頭に`catalog::RootPath`が付きます（名前の付いたマテリアル カタログから）。
* パスが絶対パスの場合は、そのパスが使用されます。それ以外の場合は、（デフォルトのカタログから）先頭に`default::RootPath`が付けられます。
* パスが絶対パスの場合は、そのパスが使用されます。そうでない場合、サーバーは[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)で指定されたパスとパスを組み合わせます。
* パスが絶対パスの場合は使用されます。そうでない場合は、[!DNL *[!DNL install_folder]*]に対する相対パスと見なされます。

画像カタログが含まれていない場合、パスは`default::RootPath`と組み合わされ、上記のように処理されます。

ソースデータファイルの物理的な場所は、通常、[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)で指定します。 ソースデータファイルを複数のファイルシステムに分散できるように、複数の値を指定できます。 レンダーサーバーは、データファイルが見つかるまで、指定された順序で各パスを試行します。

サーバーを停止することなく、いつでも任意の種類の新しいデータファイルを追加できます。
