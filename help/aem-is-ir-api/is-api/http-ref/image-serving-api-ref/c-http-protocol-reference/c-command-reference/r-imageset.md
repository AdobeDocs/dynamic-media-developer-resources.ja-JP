---
description: 画像セット. req=set応答を生成する際に使用する画像セット値を指定します。
solution: Experience Manager
title: imageSet
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 8%

---

# imageSet{#imageset}

画像セット. req=set応答を生成する際に使用する画像セット値を指定します。

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>画像セット文字列。 </p></td> 
 </tr> 
</table>

値をエスケープし、含まれる修飾子がURLクエリ文字列の一部として解釈されないようにするには、値全体を中括弧で囲む必要があります。 ネットパスでカタログレコードが指定されている場合、この修飾子の値はメインレコードの`catalog::ImageSet`より優先されます。 有効な画像セット構文については、 `catalog::ImageSet`のドキュメントを参照してください。

## プロパティ {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

リクエスト属性。 （オプション）メインレコードから`catalog::ImageSet`を上書きします。

## 初期設定 {#section-e8622ff40408450fb79d028f8d37fa6b}

なし

## 例 {#section-68513d3c601f477399602a0741dab390}

`req=set`要求で使用する画像セットを指定：

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## 関連項目 {#section-7e0320b2e09d475897082711a8f023a9}

[catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) 、 [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、メディアセッ [トの要求](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
