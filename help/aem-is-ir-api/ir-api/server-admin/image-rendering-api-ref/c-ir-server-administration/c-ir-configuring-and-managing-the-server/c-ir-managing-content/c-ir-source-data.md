---
description: 画像レンダリングソースデータファイルには、ビネットファイル、マテリアルファイル（繰り返し可能なテクスチャやデカルの画像、キャビネットやウィンドウカバリングのスタイルファイル）、ICCプロファイルが含まれます。
seo-description: 画像レンダリングソースデータファイルには、ビネットファイル、マテリアルファイル（繰り返し可能なテクスチャやデカルの画像、キャビネットやウィンドウカバリングのスタイルファイル）、ICCプロファイルが含まれます。
seo-title: ソースデータ
solution: Experience Manager
title: ソースデータ
topic: Scene7 Image Serving - Image Rendering API
uuid: 76c6419c-613e-4eff-b30f-9fea2a7daf5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---


# ソースデータ{#source-data}

画像レンダリングソースデータファイルには、ビネットファイル、マテリアルファイル（繰り返し可能なテクスチャやデカルの画像、キャビネットやウィンドウカバリングのスタイルファイル）、ICCプロファイルが含まれます。

すべてのソースデータファイルは、画像レンダリングのネイティブコードコンポーネントからアクセスできる必要があります（Image Serverと相互に配置）。

マテリアルカタログが関係する場合、マテリアルカタログで指定されているファイル（`vignette::Path`、`catalog::Path`、または`icc::ProfilePath`を含む）は、次のようにRender Serverによって検索されます。

* 絶対パスの場合は、そのまま使用されます。
* パスが相対パスの場合は、（名前の付いたマテリアルカタログから）`catalog::RootPath`というプリフィックスが付きます。
* 絶対パスの場合は、そのパスが使用されます。それ以外の場合は、（デフォルトのカタログから）「`default::RootPath`」というプリフィックスが付きます。
* 絶対パスの場合は、そのパスが使用されます。それ以外の場合、サーバは[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)で指定されたパスとこのパスを結合します。
* パスが絶対パスになった場合は、そのパスが使用されます。それ以外の場合は、[!DNL *[!DNL install_folder]*]に対する相対値と見なされます。

画像カタログが関係しない場合、パスは`default::RootPath`と組み合わされ、上記のように処理されます。

通常、ソースデータファイルの物理的な場所は、[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)で指定します。 複数の値を指定して、ソース・データ・ファイルを複数のファイル・システムに分散させることができます。 Render Serverは、データファイルが見つかるまで、指定された順序で各パスを試します。

任意の種類の新しいデータファイルを、サーバを停止しなくてもいつでも追加できます。
