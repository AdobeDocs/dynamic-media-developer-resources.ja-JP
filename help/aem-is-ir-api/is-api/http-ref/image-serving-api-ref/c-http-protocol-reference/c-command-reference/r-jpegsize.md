---
description: JPEGサイズ（キロバイト）。 JPEG応答の最大サイズをキロバイト単位で指定します。
solution: Experience Manager
title: jpegSize
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 08cecb09-100f-4671-b335-d59c88b0e1ef
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---

# jpegSize{#jpegsize}

JPEGサイズ（キロバイト）。 JPEG応答の最大サイズをキロバイト単位で指定します。

`jpegSize= *`サイズ`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> size</span></span> </p> </td> 
  <td class="stentry"> <p>サイズ(KB)。 </p></td> 
 </tr> 
</table>

これが正の値に設定され、指定されたJPEG画質のJPEG応答がこの値を超えない場合、その画像が応答として返されます。 そうしないと、JPEGの画質が低下し、指定したサイズに合う画像が生成されるか、または指定したサイズに合わないと判断されるまで低下します。 後者の場合、リクエストはエラーで失敗します。

値0は、応答がサイズに制限されないことを意味します。

負の値は使用できません。

## プロパティ {#section-19e544e77d35478b98fe8666f27d6968}

リクエスト属性。 現在の画層設定に関係なく適用されます。 出力画像形式がJPEGでない場合は無視されます。

## 初期設定 {#section-198b798ed187453197e0969c641d6fb5}

0

## 例 {#section-46bf806fd3ef4875b7726df32b6f834d}

保証サイズが大きすぎて、メモリ容量が限られたデバイスに配信できない。

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## 関連項目 {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) 、  [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
