---
description: JPEGサイズ（キロバイト） JPEG応答の最大サイズをキロバイト単位で指定します。
seo-description: JPEGサイズ（キロバイト） JPEG応答の最大サイズをキロバイト単位で指定します。
seo-title: jpegSize
solution: Experience Manager
title: jpegSize
topic: Scene7 Image Serving - Image Rendering API
uuid: 832163ca-0554-481d-b87f-bf322f415274
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# jpegSize{#jpegsize}

JPEGサイズ（キロバイト） JPEG応答の最大サイズをキロバイト単位で指定します。

`jpegSize= *`サイズ`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 大きさ</span></span> </p> </td> 
  <td class="stentry"> <p>サイズ（KB単位）。 </p></td> 
 </tr> 
</table>

これが正の値に設定され、指定したJPEG画質のJPEG応答がこの値を超えない場合、その画像が応答として返されます。 そうしないと、指定したサイズに収まる画像が生成されるか、画像が収まらないと判断されるまで、JPEGの画質が低下します。 後者の場合、要求はエラーで失敗します。

値が0の場合、応答はサイズによって制限されません。

負の値は使用できません。

## プロパティ {#section-19e544e77d35478b98fe8666f27d6968}

リクエスト属性。 現在のレイヤー設定に関係なく適用されます。 出力画像の形式がJPEGでない場合は無視されます。

## 初期設定 {#section-198b798ed187453197e0969c641d6fb5}

0

## 例 {#section-46bf806fd3ef4875b7726df32b6f834d}

保証サイズが大きすぎて、メモリに制限のあるデバイスに配信できない：

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## 関連項目 {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
