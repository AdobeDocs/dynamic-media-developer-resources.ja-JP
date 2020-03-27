---
description: 静的コンテンツタイプフィルター。 /is/content経由で配信される静的コンテンツのフィルター文字列を指定します。
seo-description: 静的コンテンツタイプフィルター。 /is/content経由で配信される静的コンテンツのフィルター文字列を指定します。
seo-title: タイプ
solution: Experience Manager
title: タイプ
topic: Scene7 Image Serving - Image Rendering API
uuid: 44906190-516c-481c-9714-bb19d77af33c
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

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

サーバーは、valと要求された静的コンテンツ `catalog::Type` 項目の値を比較します。 値が一致する場合（大文字と小文字が区別される）、項目はクライアントに返され、一致しない場合はエラーが返されます。

## プロパティ {#section-529b088434a44a9f86a64ef548d2925b}

を介して提供される静的コンテンツ（画像以外の）要求に対してのみサポートされます。 が空の場合、ま `catalog::Type` たは定義されていない場合は無視されます。

## 初期設定 {#section-e9e8f51d0a01452183ccb510efd87d46}

が指定されていない場合や空の場合は、 `type=` 型の一致は適用されません。

## 関連項目 {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[静的（画像以外）コンテンツの提](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da)[供、catalog::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
