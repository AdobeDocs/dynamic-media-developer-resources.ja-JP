---
description: 画像セット. req=set応答を生成する際に使用する画像セット値を指定します。
seo-description: 画像セット. req=set応答を生成する際に使用する画像セット値を指定します。
seo-title: imageSet
solution: Experience Manager
title: imageSet
topic: Scene7 Image Serving - Image Rendering API
uuid: ecfb3905-e3ef-4ab8-a2c4-2c3f200e0f0f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# imageSet{#imageset}

画像セット. req=set応答を生成する際に使用する画像セット値を指定します。

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>画像セット文字列 </p></td> 
 </tr> 
</table>

値をエスケープし、含まれる修飾子がURLクエリ文字列の一部として解釈されないようにするには、値全体を波括弧で囲む必要があります。 カタログレコードがネットパスで指定されている場合、この修飾子の値はメインレコ `catalog::ImageSet` ードの値より優先されます。 有効な画像セットの構文について詳しくは、ドキュメントを参照して `catalog::ImageSet` ください。

## プロパティ {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

リクエスト属性。 （オプション）メインレコ `catalog::ImageSet` ードからの上書き。

## 初期設定 {#section-e8622ff40408450fb79d028f8d37fa6b}

なし

## 例 {#section-68513d3c601f477399602a0741dab390}

要求で使用する画像セットを指 `req=set` 定します：

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## 関連項目 {#section-7e0320b2e09d475897082711a8f023a9}

[catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) 、 [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、メディ [アセット要求](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
