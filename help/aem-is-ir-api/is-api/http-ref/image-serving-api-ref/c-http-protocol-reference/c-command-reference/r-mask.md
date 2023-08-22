---
title: マスク
description: 画像マスク。 関連付けられていないマスクとして使用する別のマスクイメージを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 1%

---

# マスク{#mask}

画像マスク。 関連付けられていないマスクとして使用する別のマスクイメージを指定します。

`mask= *`object`*|{[is|ir]'{' *`nestedRequest`*'}'}`

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

*`object`* は、カタログエントリ、または画像/SVGファイルです。 画像レイヤーとべた塗りのレイヤーに指定できます。

次の場合 *`object`* は画像カタログエントリに解決されます。 `catalog::MaskPath` が使用されているか、または `catalog::MaskPath` が定義されていない場合、 `catalog::Path` が使用されます。 次の場合 *`object`* はカタログエントリに解決されず、ファイルパスとして解釈されます。

どのような場合でも、ソース画像にアルファチャンネルがある場合は、そのチャンネルが使用されます。 それ以外の場合は、必要に応じて画像はグレースケールに変換されてから、レイヤーマスクとして使用されます。

マスクをべた塗りのレイヤーにアタッチした場合は、画像レイヤーの画像と同じ規則を使用して、マスクを切り抜いて拡大/縮小できます。 `size=`, `scale=`または `res=` を使用して、マスクをスケーリングできます。

レイヤーマスクは、 *`nestedRequest`*. ネストされたリクエストまたは埋め込みリクエストは中括弧で囲みます。 埋め込み画像サービング要求の先頭にプレフィックスを付けます。 `is` と、を使用した埋め込み画像レンダリングリクエスト `ir`. プレフィックスが指定されていない場合、外部サーバーへの要求が想定されます。 参照： [リクエストのネストと埋め込み](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) 」を参照してください。

## プロパティ {#section-a093043dc249423b8ae322cefb0d545d}

画像またはレイヤの属性。 次の場合にレイヤー 0 に適用 `layer=comp`. 効果画層で無視されます。

*`object`* は、 `src=` または `mask=` コマンドイン `catalog::Modifier`.

The `is` および `ir` プレフィックスでは大文字と小文字が区別されません。

## 初期設定 {#section-10cf793c665f49deb1b248faa3b618a9}

次の場合 `mask=` が明示的に指定されていない場合や、画層イメージがカタログエントリに関連付けられている場合は、 `catalog::MaskPath` が使用されます。 それ以外の場合は、レイヤーイメージのアルファチャンネルが使用されます（存在する場合）。 アルファチャンネルがない場合、レイヤーにはマスクがなく、レイヤーの長方形は完全に不透明にレンダリングされます。

## 例 {#section-1bbe623f7c744bdf97b596458d8e7ea3}

複数の個別のマスクを使用して、画像の様々な領域に色分けします。 カラー化され、マスクされた領域は、元の未変更の画像の上に重ねて表示されます。

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## 関連項目 {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , [リクエストのネストと埋め込み](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
