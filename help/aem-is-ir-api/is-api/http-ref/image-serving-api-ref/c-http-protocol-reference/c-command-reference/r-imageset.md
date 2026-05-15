---
title: imageSet
description: 画像セット： req=set応答を生成する際に使用する画像セット値を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
TQID: 'https://experienceleague.adobe.com/uG2ZMLKzhiLvFcfHh8PYHroKETvkdLfBcHWJPgc4-mU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 5%

---

# imageSet{#imageset}

画像セット： req=set応答を生成する際に使用する画像セット値を指定します。

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>画像セット文字列。 </p></td> 
 </tr> 
</table>

値をエスケープし、含まれる修飾子がURL クエリ文字列の一部として解釈されないようにするには、値全体を中括弧で囲む必要があります。 カタログレコードがネットパスで指定されている場合、この修飾子値はメインレコードから`catalog::ImageSet`を上書きします。 有効な画像セット構文の説明については、`catalog::ImageSet` ドキュメントを参照してください。

## プロパティ {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

リクエスト属性： オプション。 メインレコードから`catalog::ImageSet`を上書きします。

## 初期設定 {#section-e8622ff40408450fb79d028f8d37fa6b}

なし

## 例 {#section-68513d3c601f477399602a0741dab390}

`req=set` リクエストで使用する画像セットを指定：

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## 関連項目 {#section-7e0320b2e09d475897082711a8f023a9}

[ カタログ：:ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)、[req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、[ メディアセットリクエスト ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
