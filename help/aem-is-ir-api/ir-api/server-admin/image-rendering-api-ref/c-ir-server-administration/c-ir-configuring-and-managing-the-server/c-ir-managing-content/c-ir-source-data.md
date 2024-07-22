---
description: イメージ レンダリングのソース データ ファイルには、ビネット ファイル、マテリアル ファイル（繰り返し可能なテクスチャおよびデカールのイメージ、スタイル ファイルをカバーするキャビネットおよびウィンドウのイメージ）、および ICC プロファイルが含まれます。
solution: Experience Manager
title: Source データ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Source データ{#source-data}

イメージ レンダリングのソース データ ファイルには、ビネット ファイル、マテリアル ファイル（繰り返し可能なテクスチャおよびデカールのイメージ、スタイル ファイルをカバーするキャビネットおよびウィンドウのイメージ）、および ICC プロファイルが含まれます。

すべてのソースデータファイルは、画像レンダリングのネイティブコードコンポーネント（画像サーバーと共存）にアクセスできる必要があります。

材料カタログが関係する場合、材料カタログで指定されたファイル（`vignette::Path`、`catalog::Path`、または `icc::ProfilePath`）が Render Server によって次のように検索されます。

* パスが絶対パスの場合は、そのまま使用されます。
* 相対パスの場合は、先頭に `catalog::RootPath` が付きます（名前付きマテリアル カタログから）。
* パスが絶対パスの場合は、このパスが使用されます。絶対パスの場合は、（デフォルトのカタログから） `default::RootPath` というプレフィックスが付きます。
* パスが絶対パスの場合は、そのパスが使用されます。パスが絶対パスの場合は、[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2) で指定されたパスと組み合わされます。
* この時点でパスが絶対パスの場合は、このパスが使用されます。それ以外の場合は、[!DNL *[!DNL install_folder]*] に対する相対パスと見なされます。

画像カタログが関係しない場合、パスは `default::RootPath` と結合され、上記のように処理されます。

ソース データ ファイルの物理的な場所は、通常 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2) で指定します。 複数の値を指定して、ソース・データ・ファイルを複数のファイル・システムに分散させることができます。 Render Server は、データ ファイルが見つかるまで、指定された順序で各パスを試行します。

任意の種類の新しいデータファイルは、サーバーを停止せずにいつでも追加できます。
