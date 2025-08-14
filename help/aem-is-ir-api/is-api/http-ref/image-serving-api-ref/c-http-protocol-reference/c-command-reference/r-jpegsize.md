---
title: jpegSize
description: Jpeg サイズ（キロバイト単位）。 JPEGの応答の最大サイズを KB 単位で指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08cecb09-100f-4671-b335-d59c88b0e1ef
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# jpegSize{#jpegsize}

Jpeg サイズ（キロバイト単位）。 JPEGの応答の最大サイズを KB 単位で指定します。

`jpegSize= *` サイズ `*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> サイズ </span></span> </p> </td> 
  <td class="stentry"> <p>サイズ（キロバイト単位）。 </p></td> 
 </tr> 
</table>

これが正の値に設定され、指定されたJPEG画質を持つJPEGの応答がこの値を超えない場合、その画像が応答として返されます。 そうでない場合、JPEGの画質は、指定したサイズに収まる画像が生成されるか、収まらないと判断されるまで低下します。 後者の場合、リクエストはエラーで失敗します。

値が 0 の場合、応答はサイズによる制限を受けません。

負の値は使用できません。

## プロパティ {#section-19e544e77d35478b98fe8666f27d6968}

リクエスト属性。 現在のレイヤ設定に関係なく適用されます。 出力画像の形式がJPEGでない場合は無視されます。

## 初期設定 {#section-198b798ed187453197e0969c641d6fb5}

0

## 例 {#section-46bf806fd3ef4875b7726df32b6f834d}

メモリ容量が限られているデバイスに配信するには、保証サイズが大きすぎません。

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## 関連項目 {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
