---
title: タイプ
description: 静的コンテンツタイプフィルター： /is/contentを介して配信される静的コンテンツのフィルター文字列を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
TQID: 'https://experienceleague.adobe.com/YudohKBdOo08A1MLfQuILLVhe9mXTAcuzWs5z6zrh-g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 4%

---

# タイプ{#type}

静的コンテンツタイプフィルター： /is/contentを介して配信される静的コンテンツのフィルター文字列を指定します。

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>フィルター文字列を入力します。 </p></td> 
 </tr> 
</table>

サーバーは、`val`を、リクエストされた静的コンテンツ項目の`catalog::Type`の値と比較します。 値が一致する（大文字と小文字を区別する）場合、項目はクライアントに返され、そうでない場合はエラーが返されます。

## プロパティ {#section-529b088434a44a9f86a64ef548d2925b}

の方法で提供される静的コンテンツ（画像でない）要求でのみサポートされます。 `catalog::Type`が空であるか、定義されていないかは無視されます。

## 初期設定 {#section-e9e8f51d0a01452183ccb510efd87d46}

`type=`が指定されていないか空の場合、型の一致は適用されません。

## 関連項目 {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[静的（画像でない）コンテンツを提供しています](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da)、[ カタログ：::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
