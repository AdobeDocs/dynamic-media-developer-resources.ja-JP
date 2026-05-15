---
title: jpegSize
description: Jpeg サイズ （KiloBytes）。 JPEG応答の最大サイズをキロバイト単位で指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08cecb09-100f-4671-b335-d59c88b0e1ef
TQID: 'https://experienceleague.adobe.com/FXPTcUoMZP-mA-PyuaLqLFqqY9ITLWkjWgezRFUDiHI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 3%

---

# jpegSize{#jpegsize}

Jpeg サイズ （KiloBytes）。 JPEG応答の最大サイズをキロバイト単位で指定します。

`jpegSize= *` サイズ `*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> サイズ </span></span> </p> </td> 
  <td class="stentry"> <p>サイズ（キロバイト）。 </p></td> 
 </tr> 
</table>

これが正の値に設定され、指定されたJPEG画質のJPEG応答がこの値を超えない場合、その画像が応答として返されます。 それ以外の場合、JPEGの画質は、指定したサイズに合う画像が生成されるか、合わないと判断されるまで低下します。 後者の場合、リクエストはエラーで失敗します。

値が0の場合、応答がサイズによって制限されないことを意味します。

負の値は使用できません。

## プロパティ {#section-19e544e77d35478b98fe8666f27d6968}

リクエスト属性： 現在のレイヤー設定に関係なく適用されます。 出力画像のフォーマットがJPEGでない場合は無視されます。

## 初期設定 {#section-198b798ed187453197e0969c641d6fb5}

0

## 例 {#section-46bf806fd3ef4875b7726df32b6f834d}

メモリが限られているデバイスに配信するには、保証サイズが大きすぎません。

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## 関連項目 {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)、[属性：:JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
