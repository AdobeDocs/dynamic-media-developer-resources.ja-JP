---
title: マスク
description: 画像マスク： 関連付けられていないマスクとして使用する別のマスクイメージを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
TQID: 'https://experienceleague.adobe.com/QV2kCpSVhXdG59s5WjrQ7ENp-F5qkDuHCJeL-nkwuP4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 342
ht-degree: 1%

---

# マスク{#mask}

画像マスク： 関連付けられていないマスクとして使用する別のマスクイメージを指定します。

`mask= *` オブジェクト `*|{[is|ir]'{' *`nestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> オブジェクト </span> </p></td> 
  <td class="stentry"> <p>画像またはレイヤーマスクとして使用する画像オブジェクト。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>ネストされた画像サービング、画像レンダリング、または外部リクエスト。 </p></td> 
 </tr> 
</table>

*`object`*&#x200B;は、カタログ項目または画像/SVG ファイルのいずれかである可能性があります。 画像レイヤーと単色レイヤーに指定できます。

*`object`*&#x200B;が画像カタログのエントリに解決する場合は、`catalog::MaskPath`が使用されるか、`catalog::MaskPath`が定義されていない場合は、`catalog::Path`が使用されます。 *`object`*&#x200B;がカタログ エントリに解決されない場合、ファイル パスとして解釈されます。

いずれの場合も、ソース画像にアルファチャンネルがある場合は、それを使用します。 それ以外の場合、画像はレイヤーマスクとして使用する前に、必要に応じてグレースケールに変換されます。

マスクを単色レイヤーにアタッチした場合、画像レイヤーの画像に使用するのと同じルールを使用して、マスクを切り抜いて拡大・縮小できます。 `size=`、`scale=`または`res=`を使用して、マスクを拡大・縮小できます。

レイヤーマスクは&#x200B;*`nestedRequest`*&#x200B;の形式で指定することもできます。 ネストされたリクエストまたは埋め込まれたリクエストは、中括弧で囲まれます。 埋め込み画像サービングリクエストの先頭に`is`を付け、埋め込み画像レンダリングリクエストに`ir`を付けます。 接頭辞が指定されていない場合、外部サーバーへのリクエストが想定されます。 詳しくは、[ ネストと埋め込みのリクエスト ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)を参照してください。

## プロパティ {#section-a093043dc249423b8ae322cefb0d545d}

画像またはレイヤー属性： `layer=comp`の場合、レイヤー0に適用されます。 エフェクトレイヤーでは無視されます。

*`object`*&#x200B;は、`src=`または`mask=` コマンドを`catalog::Modifier`に含むカタログ レコードに解決できません。

`is`と`ir`の接頭辞は大文字と小文字を区別しません。

## 初期設定 {#section-10cf793c665f49deb1b248faa3b618a9}

`mask=`が明示的に指定されておらず、レイヤー画像がカタログエントリに関連付けられている場合は、`catalog::MaskPath`が使用されます。 それ以外の場合は、レイヤー画像のアルファチャンネルが使用されます（存在する場合）。 アルファチャンネルがない場合、レイヤーにはマスクがなく、レイヤーの長方形は完全に不透明になります。

## 例 {#section-1bbe623f7c744bdf97b596458d8e7ea3}

複数の個別のマスクを使用して、画像の異なる領域を色付けします。 カラー化されたマスクされた領域は、元の変更されていない画像の上にレイヤー化されます。

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## 関連項目 {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464)、[ カタログ：:MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)、[ オブジェクト ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)、[ ネストと埋め込み](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
