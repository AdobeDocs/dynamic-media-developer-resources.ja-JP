---
description: 画像レンダリングのソースデータファイルには、ビネットファイル、マテリアルファイル（繰り返し可能なテクスチャとデカールの画像、キャビネットとウィンドウカバーのスタイルファイル）、ICCプロファイルが含まれます。
solution: Experience Manager
title: ソースデータ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# ソースデータ{#source-data}

画像レンダリングのソースデータファイルには、ビネットファイル、マテリアルファイル（繰り返し可能なテクスチャとデカールの画像、キャビネットとウィンドウカバーのスタイルファイル）、ICCプロファイルが含まれます。

すべてのソースデータファイルは、画像レンダリングのネイティブコードコンポーネント（Image Serverと共に配置）からアクセスできる必要があります。

マテリアルカタログが含まれる場合、マテリアルカタログで指定されたファイル（`vignette::Path`、`catalog::Path`、または`icc::ProfilePath`を含む）は、次のようにRender Serverによって検索されます。

* パスが絶対パスの場合は、そのまま使用されます。
* パスが相対パスの場合は、（名前の付いたマテリアルカタログから）`catalog::RootPath`というプレフィックスが付きます。
* パスが絶対パスの場合は、それ以外の場合は、（デフォルトのカタログの）`default::RootPath`というプレフィックスが付きます。
* パスが絶対パスの場合は、それ以外の場合、サーバは[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)で指定されたパスと結合します。
* パスが絶対パスの場合は、それ以外の場合は、[!DNL *[!DNL install_folder]*]に対する相対パスであると見なされます。

画像カタログが関係しない場合、パスは`default::RootPath`と組み合わされ、上記のように処理されます。

ソースデータファイルの物理的な場所は、通常、[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)で指定します。 複数の値を指定して、ソースデータファイルを複数のファイルシステムに分散できます。 Render Serverは、データファイルが見つかるまで、指定された順序で各パスを試みます。

任意の種類の新しいデータファイルは、サーバーを停止することなくいつでも追加できます。
