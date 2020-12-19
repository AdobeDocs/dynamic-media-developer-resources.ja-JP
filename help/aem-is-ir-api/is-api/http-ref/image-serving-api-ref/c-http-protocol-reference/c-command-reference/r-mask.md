---
description: 画像マスク 関連付けられていないマスクとして使用する別のマスク画像を指定します。
seo-description: 画像マスク 関連付けられていないマスクとして使用する別のマスク画像を指定します。
seo-title: mask
solution: Experience Manager
title: mask
topic: Scene7 Image Serving - Image Rendering API
uuid: 2dc14d20-f02a-4a77-9b73-0c01e10d448d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 1%

---


# mask{#mask}

画像マスク 関連付けられていないマスクとして使用する別のマスク画像を指定します。

`mask= *`objectnestedRequest`*|{[is|ir]'{' *``*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> オブジェクト</span> </p></td> 
  <td class="stentry"> <p>画像またはレイヤーマスクとして使用する画像オブジェクト。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>ネストされた画像サービング、画像レンダリングまたは外部要求。 </p></td> 
 </tr> 
</table>

*`object`* は、カタログエントリまたは画像/SVGファイルのいずれかです。画像レイヤーとべた塗りレイヤーに対して指定できます。

*`object`*&#x200B;が画像カタログエントリに解決される場合は`catalog::MaskPath`が使用され、`catalog::MaskPath`が定義されない場合は`catalog::Path`が使用されます。 *`object`*&#x200B;がカタログエントリに解決されない場合は、ファイルパスとして解釈されます。

どのような場合でも、ソース画像にアルファチャネルが含まれている場合は、その画像が使用されます。 それ以外の場合は、必要に応じて画像がグレースケールに変換された後で、レイヤーマスクとして使用します。

マスクをべた塗りのレイヤーにアタッチすると、画像レイヤーの画像と同じ規則を使用して、マスクを切り抜き、拡大/縮小できます。 `size=`、 `scale=`またはを使用し `res=` てマスクをスケールできます。

レイヤーマスクは、*`nestedRequest`*&#x200B;の形式で指定することもできます。 入れ子のリクエストや埋め込みのリクエストは、中括弧で囲みます。 埋め込み画像サービング要求の先頭に`is`を、埋め込み画像レンダリング要求の先頭に`ir`を付けます。 プレフィックスが指定されていない場合、外部サーバーへの要求と見なされます。 詳しくは、[リクエストの入れ子と埋め込み](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)を参照してください。

## プロパティ {#section-a093043dc249423b8ae322cefb0d545d}

画像またはレイヤーの属性。 `layer=comp`の場合にレイヤー0に適用されます。 エフェクトレイヤーでは無視されます。

*`object`* または `src=` コマンドを含むカタログレコードに解決できない `mask=` ようにする必要があり `catalog::Modifier`ます。

`is`と`ir`のプリフィックスでは、大文字と小文字が区別されません。

## 初期設定 {#section-10cf793c665f49deb1b248faa3b618a9}

`mask=`を明示的に指定せず、レイヤー画像がカタログエントリに関連付けられている場合は、`catalog::MaskPath`が使用されます。 それ以外の場合は、レイヤー画像のアルファチャネルが使用されます（存在する場合）。 アルファチャネルがない場合、レイヤーにはマスクがなく、レイヤーの長方形は完全に不透明にレンダリングされます。

## 例 {#section-1bbe623f7c744bdf97b596458d8e7ea3}

複数の個別のマスクを使用して、画像の様々な領域に色を付けます。 色付きのマスク領域は、元の変更されていない画像の上に重ねて表示されます。

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## 関連項目 {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) ,  [Request Nesting and Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
