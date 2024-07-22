---
title: imageSet
description: 画像セット。 req=set レスポンスを生成するときに使用するイメージ セット値を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 4%

---

# imageSet{#imageset}

画像セット。 req=set レスポンスを生成するときに使用するイメージ セット値を指定します。

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>画像セット文字列。 </p></td> 
 </tr> 
</table>

値をエスケープし、含まれる修飾子が URL クエリ文字列の一部として解釈されないようにするには、値全体を中括弧で囲む必要があります。 カタログ レコードがネット パスで指定されている場合、この修飾子の値がメイン レコードの `catalog::ImageSet` をオーバーライドします。 有効な画像セット構文の説明については、ドキュメント `catalog::ImageSet` 参照してください。

## プロパティ {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

リクエスト属性。 オプション。 メインレコードの `catalog::ImageSet` を上書きします。

## 初期設定 {#section-e8622ff40408450fb79d028f8d37fa6b}

なし

## 例 {#section-68513d3c601f477399602a0741dab390}

リクエストで使用する画像セット `req=set` 指定：

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## 関連項目 {#section-7e0320b2e09d475897082711a8f023a9}

[catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)、[req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、[Media Set Requests](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
