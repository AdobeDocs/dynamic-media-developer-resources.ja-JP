---
description: 静的コンテンツタイプフィルター。 /is/content経由で配信される静的コンテンツのフィルター文字列を指定します。
seo-description: 静的コンテンツタイプフィルター。 /is/content経由で配信される静的コンテンツのフィルター文字列を指定します。
seo-title: タイプ
solution: Experience Manager
title: タイプ
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 44906190-516c-481c-9714-bb19d77af33c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 5%

---


# タイプ{#type}

静的コンテンツタイプフィルター。 /is/content経由で配信される静的コンテンツのフィルター文字列を指定します。

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>フィルター文字列を入力します。 </p></td> 
 </tr> 
</table>

サーバーはvalと、要求された静的コンテンツ項目の`catalog::Type`の値を比較します。 値が一致する（大文字と小文字が区別される）場合は項目がクライアントに返され、それ以外の場合はエラーが返されます。

## プロパティ {#section-529b088434a44a9f86a64ef548d2925b}

で提供される静的コンテンツ（画像以外の）要求に対してのみサポートされます。 `catalog::Type`が空の場合、または定義されていない場合は無視されます。

## 初期設定 {#section-e9e8f51d0a01452183ccb510efd87d46}

`type=`が指定されていない場合や空の場合は、型の一致は適用されません。

## 関連項目 {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[静的な（画像以外の）コンテンツのサービング](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da)、 [catalog::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
