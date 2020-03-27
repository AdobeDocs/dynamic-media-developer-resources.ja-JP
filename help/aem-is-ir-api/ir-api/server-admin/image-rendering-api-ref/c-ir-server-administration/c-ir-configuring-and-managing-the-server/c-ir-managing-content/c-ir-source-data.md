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

---


# ソースデータ{#source-data}

画像レンダリングソースデータファイルには、ビネットファイル、マテリアルファイル（繰り返し可能なテクスチャやデカルの画像、キャビネットやウィンドウカバリングのスタイルファイル）、ICCプロファイルが含まれます。

すべてのソースデータファイルは、画像レンダリングのネイティブコードコンポーネント（Image Serverと共に配置）からアクセスできる必要があります。

マテリアルカタログが含まれる場合、マテリアルカタログで指定されたファイル(、、また `vignette::Path`はを含む `catalog::Path`)が、次のよ `icc::ProfilePath`うにRender Serverによって参照されます。

* 絶対パスの場合は、そのまま使用されます。
* パスが相対パスの場合は、(名前の付いたマテリアルカ `catalog::RootPath` タログの)プリフィックスが付きます。
* 絶対パスの場合は、パスが使用されます。それ以外の場合は、(デフォルトのカタロ `default::RootPath` グの)プリフィックスが付きます。
* 絶対パスの場合は、パスが使用されます。それ以外の場合、サーバーは [ir.resourceRootPathsで指定されたパスとそのパスを結合します](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)。
* パスが絶対パスになった場合は、そのパスが使用されます。それ以外の場合は、[!DNL *[!DNL install_folder]*]を基準とした相対パスと見なされます。

画像カタログが含まれない場合、パスは上記と組み合わ `default::RootPath` され、処理されます。

通常、ソースデータファイルの物理的な場所は [ir.resourceRootPathsで指定します](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)。 複数の値を指定して、ソース・データ・ファイルを複数のファイル・システムに分散させることができます。 Render Serverは、データファイルが見つかるまで、指定された順序で各パスを試みます。

任意の種類の新しいデータファイルを、サーバーを停止しなくてもいつでも追加できます。
