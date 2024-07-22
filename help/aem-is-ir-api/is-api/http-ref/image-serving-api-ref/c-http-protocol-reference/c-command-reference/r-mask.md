---
title: マスク
description: 画像マスク。 関連付けられていないマスクとして使用する個別のマスク イメージを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 1%

---

# マスク{#mask}

画像マスク。 関連付けられていないマスクとして使用する個別のマスク イメージを指定します。

`mask= *`object`*|{[is|ir]'{' *`nestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> オブジェクト </span> </p></td> 
  <td class="stentry"> <p>画像またはレイヤーマスクとして使用する画像オブジェクト。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>ネストされた画像サービング、画像レンダリングまたは外部リクエスト。 </p></td> 
 </tr> 
</table>

カタログエントリまたは画像/SVGファイルのい *`object`* れかです。 イメージレイヤーとベタ塗りのレイヤーに指定できます。

*`object`* が画像カタログエントリを解決する場合は `catalog::MaskPath` が使用され、`catalog::MaskPath` が定義されていない場合は `catalog::Path` が使用されます。 *`object`* がカタログエントリに解決されない場合、ファイルパスとして解釈されます。

いずれの場合も、ソース イメージにアルファ チャンネルがある場合に使用されます。 それ以外の場合は、必要に応じて、レイヤーマスクとして使用する前に画像がグレースケールに変換されます。

マスクがソリッドカラーレイヤーにアタッチされている場合、イメージレイヤー内の画像に使用されるのと同じルールを使用して、マスクを切り抜いたり拡大縮小したりできます。 `size=`、`scale=`、または `res=` を使用して、マスクをスケールできます。

レイヤーマスクは、レイ *`nestedRequest`* ーの形式で指定することもできます。 ネストされたリクエストまたは埋め込まれたリクエストは、中括弧で囲まれます。 埋め込み画像サービングリクエストの前に `is` を、埋め込み画像レンダリングリクエストの前に `ir` を付けます。 プレフィックスが指定されていない場合、外部サーバーへのリクエストが想定されます。 詳しくは、[ リクエストのネストと埋め込み ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) を参照してください。

## プロパティ {#section-a093043dc249423b8ae322cefb0d545d}

イメージまたはレイヤ アトリビュート。 `layer=comp` の場合はレイヤー 0 に適用されます。 エフェクトレイヤーで無視されます。

*`object`* は、`catalog::Modifier` に `src=` または `mask=` コマンドを含むカタログ レコードに解決しないでください。

`is` と `ir` のプレフィックスでは、大文字と小文字が区別されません。

## 初期設定 {#section-10cf793c665f49deb1b248faa3b618a9}

`mask=` が明示的に指定されていない場合、および画層イメージがカタログ エントリに関連付けられている場合は、`catalog::MaskPath` が使用されます。 それ以外の場合は、レイヤーイメージのアルファチャンネルが使用されます（存在する場合）。 アルファチャンネルがない場合、レイヤーにはマスクがなく、レイヤーの長方形は完全に不透明にレンダリングされます。

## 例 {#section-1bbe623f7c744bdf97b596458d8e7ea3}

複数の個別のマスクを使用して、画像の異なる領域に色を付けます。 カラー化され、マスクされた領域は、元の変更されていない画像の上に重ねられます。

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## 関連項目 {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md) , [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , [ ネストと埋め込みのリクエスト ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
