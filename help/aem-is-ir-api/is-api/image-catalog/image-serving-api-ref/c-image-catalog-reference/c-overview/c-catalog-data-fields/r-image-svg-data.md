---
description: 次のフィールドは、画像およびSVGデータファイルで認識されます。
seo-description: 次のフィールドは、画像およびSVGデータファイルで認識されます。
seo-title: Image_SVGデータ
solution: Experience Manager
title: Image_SVGデータ
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f9595b3-d448-4aa1-87fe-edddfdd48873
translation-type: tm+mt
source-git-commit: 93c8d3016b21b0ea5689d79115588f13e702cf9f

---


# Image_SVGデータ{#image-svg-data}

次のフィールドは、画像およびSVGデータファイルで認識されます。

## Catalog management {#section-1056bcc3b6d04166b3aa6ec48913b6b2}

<table id="table_823F89CAD494441690D28F18005F774C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md" type="reference" format="dita" scope="local"> ID</a></span> </p> </td> 
   <td colname="col2"> <p>カタログレコード識別子（インデックスキー）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Request attributes {#section-cfe69bcdcd4b4d129e99d11b9078ae4a}

<table id="table_C070C676835F49918E1B3BBF81471B09"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba" type="reference" format="dita" scope="local"> DigimarcInfo</a></span> </p> </td> 
   <td colname="col2"> <p>Digimarc埋め込みの画像固有の情報。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a" type="reference" format="dita" scope="local"> 有効期限</a></span> </p> </td> 
   <td colname="col2"> <p>返信画像のキャッシュの有効期限（有効期間）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 修 <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md" type="reference" format="dita" scope="local"> 飾子</a></span> </p> </td> 
   <td colname="col2"> <p>プレフィックスリクエスト修飾子 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md" type="reference" format="dita" scope="local"> PostModifier</a></span> </p> </td> 
   <td colname="col2"> <p>接尾辞リクエスト修飾子 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Time <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded" type="reference" format="dita" scope="local"> Stamp</a></span> </p> </td> 
   <td colname="col2"> <p>ファイル変更のタイムスタンプ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Image attributes {#section-74c4d124255d4218ade87d7d1677c76d}

<table id="table_F2A33C2EB17A4EACB00DDEF7FB1BB0D4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md" type="reference" format="dita" scope="local"> アンカー</a></span> </p> </td> 
   <td colname="col2"> <p>画像のアンカーポイント </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> MaskPath <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md" type="reference" format="dita" scope="local"></a></span> </p> </td> 
   <td colname="col2"> <p>マスクファイルパス </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> パ <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md" type="reference" format="dita" scope="local"> ス</a></span> </p> </td> 
   <td colname="col2"> <p>画像/SVGファイルのパス </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> PrintResolution <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5" type="reference" format="dita" scope="local"></a></span> </p> </td> 
   <td colname="col2"> <p>印刷解像度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 解 <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1" type="reference" format="dita" scope="local"> 像度</a></span> </p> </td> 
   <td colname="col2"> <p>オブジェクトの解像度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> サイ <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-size-cat.md" type="reference" format="dita" scope="local"> ズ</a></span> </p> </td> 
   <td colname="col2"> <p>画像サイズ. </p> </td> 
  </tr> 
 </tbody> 
</table>

## サムネールの属性 {#section-c5ac27bcd4224a80b7f42ead249027b1}

<table id="table_E07909B6C16F4D9686ADA381A4178E25"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> サム <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69" type="reference" format="dita" scope="local"> 解像度</a></span> </p> </td> 
   <td colname="col2"> <p>サムネールの解像度 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ThumbType <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03" type="reference" format="dita" scope="local"></a></span> </p> </td> 
   <td colname="col2"> <p>サムネールの種類 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 補助データ {#section-bff4e1f9af9d45f1872abac3b414a629}

<table id="table_B6A9A702F533494E85CEC1AD42EC728A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> AssetType <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-assettype-cat.md" type="reference" format="dita" scope="local"></a></span> </p> </td> 
   <td colname="col2"> <p>アセットタイプ. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 画像セ <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md" type="reference" format="dita" scope="local"> ット</a></span> </p> </td> 
   <td colname="col2"> <p>画像セットデータ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> マッ <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md" type="reference" format="dita" scope="local"> プ</a></span> </p> </td> 
   <td colname="col2"> <p>画像マップデータ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ターゲ <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md" type="reference" format="dita" scope="local"> ット</a></span> </p> </td> 
   <td colname="col2"> <p>ズームターゲットデータ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> UserData <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md" type="reference" format="dita" scope="local"></a></span> </p> </td> 
   <td colname="col2"> <p>ユーザー定義データ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

