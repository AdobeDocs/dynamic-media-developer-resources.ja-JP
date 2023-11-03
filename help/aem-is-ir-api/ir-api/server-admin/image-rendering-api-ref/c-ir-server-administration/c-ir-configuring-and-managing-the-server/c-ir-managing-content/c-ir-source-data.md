---
description: 画像レンダリングのソースデータファイルには、ビネットファイル、マテリアルファイル（繰り返し可能なテクスチャとデカールの画像、キャビネットとウィンドウカバーのスタイルファイル）、ICC プロファイルが含まれます。
solution: Experience Manager
title: ソースデータ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# ソースデータ{#source-data}

画像レンダリングのソースデータファイルには、ビネットファイル、マテリアルファイル（繰り返し可能なテクスチャとデカールの画像、キャビネットとウィンドウカバーのスタイルファイル）、ICC プロファイルが含まれます。

すべてのソースデータファイルは、画像レンダリングのネイティブコードコンポーネント（Image Server と共に配置）からアクセスできる必要があります。

マテリアルカタログが含まれる場合、マテリアルカタログで指定されたファイル ( `vignette::Path`, `catalog::Path`または `icc::ProfilePath`) は、次のように Render Server によって検索されます。

* 絶対パスの場合は、そのまま使用されます。
* パスが相対パスの場合は、先頭に「 」が付きます。 `catalog::RootPath` （名前付きのマテリアルカタログから）。
* 絶対パスの場合は、そのパスが使用されます。それ以外の場合は、というプレフィックスが付きます。 `default::RootPath` （デフォルトのカタログから）。
* 絶対パスの場合は、そのパスが使用されます。それ以外の場合は、サーバがそのパスを [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* 絶対パスになった場合は、そのパスが使用されます。それ以外の場合は、[!DNL  *[!DNL install_folder]*].

画像カタログが関係しない場合、パスは `default::RootPath` その後、上記のように処理されます。

通常、ソースデータファイルの物理的な場所は、 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). 複数の値を指定して、ソースデータファイルを複数のファイルシステムに分散させることができます。 Render Server は、データファイルが見つかるまで、指定された順序で各パスを試みます。

任意の種類の新しいデータファイルは、サーバーを停止することなく、いつでも追加できます。
