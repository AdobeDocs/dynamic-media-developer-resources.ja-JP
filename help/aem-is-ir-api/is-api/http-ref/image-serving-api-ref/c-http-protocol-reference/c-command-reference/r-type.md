---
title: タイプ
description: 静的コンテンツタイプフィルター。 /is/content を使用して配信される静的コンテンツのフィルター文字列を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# タイプ{#type}

静的コンテンツタイプフィルター。 /is/content を使用して配信される静的コンテンツのフィルター文字列を指定します。

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>フィルター文字列を入力します。 </p></td> 
 </tr> 
</table>

サーバーは、`val` を、リクエストされた静的コンテンツ項目の `catalog::Type` の値と比較します。 値が一致する場合（大文字と小文字を区別）、項目がクライアントに返されます。一致しない場合は、エラーが返されます。

## プロパティ {#section-529b088434a44a9f86a64ef548d2925b}

経由で処理される静的コンテンツ（画像以外）リクエストでのみサポートされます。 `catalog::Type` が空であるか、定義されていない場合、無視されます。

## 初期設定 {#section-e9e8f51d0a01452183ccb510efd87d46}

`type=` が指定されていないか、空の場合、タイプの一致は適用されません。

## 関連項目 {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[ 静的（非画像）コンテンツの提供 ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da)、[catalog:::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
