---
title: src
description: マテリアルファイル。 マテリアル データを、単一のマテリアル カタログ参照の形式で、または1つまたは2つの画像またはマテリアル データ ファイルとしてコンマで区切って指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
TQID: 'https://experienceleague.adobe.com/-PushPHP2ZvNu2IFmB-1akxSvlXtDvxStXgFTAw1t-w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 444
ht-degree: 1%

---

# src{#src}

マテリアルファイル。 マテリアル データを、単一のマテリアル カタログ参照の形式で、または1つまたは2つの画像またはマテリアル データ ファイルとしてコンマで区切って指定します。

`src = *`catalogEntry`*|{{ *`materialFile`*| *`embeddedReq`*}[, *`materialFile`*]`

`srcE= *`name`*`

`srcN= *`index`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&brace;'is&brace;'<span class="varname"> isReq</span>'&rbrace;'&brace;'&brace;'&amp;ir&brace;'<span class="varname"> irReq</span>'&brace;'|&lbrace;'&lbrace;'&lbrace;'<span class="varname"> foreignReq</span>'&rbrace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>マテリアルカタログ ID （<span class="codeph">属性：:RootId</span>）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>マテリアル カタログ エントリ （<span class="codeph"> カタログ：:Id</span>）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>マテリアルスタイルファイル （<span class="filepath"> .vnc</span>または<span class="filepath"> .vnw</span>）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>画像データファイル。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>画像サービングへのリクエスト。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>画像レンダリングへのリクエスト。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>外部サーバーへのリクエスト。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">名</span> </p></td> 
  <td class="stentry"> <p>埋め込まれたマテリアルの名前。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> インデックス </span> </p></td> 
  <td class="stentry"> <p>埋め込まれたマテリアルの0から始まるインデックス番号。 </p></td> 
 </tr> 
</table>

繰り返し可能なテクスチャ、デカール、壁紙のマテリアルには、1つの画像が必要です。この画像はファイルまたは埋め込みリクエストとして指定できます。

キャビネット マテリアルには、キャビネット スタイル ファイル （[!DNL .vnc]）が必要です。これは、ネストされたリクエストとして指定することはできません。 テクスチャ画像ファイルはキャビネットに対してオプションであり、指定した場合はファイルまたは埋め込みリクエストのいずれかになります。

ウィンドウ カバリング マテリアルには、ウィンドウ カバリング スタイル ファイル （[!DNL .vnw]）が必要です。これは、ネストされたリクエストとして指定することはできません。 テクスチャファイルはオプションであり、指定した場合はファイルまたは埋め込みリクエストのいずれかになります。

画像レンダリングでは、マテリアル カタログ、カタログ エントリ、データ ファイルを検索するために、画像サービスと同じルールを使用します。 詳しくは、画像サービングドキュメントの&#x200B;*`object`* データタイプの説明を参照してください。

*`materialFile`*&#x200B;は`attribute::RootPath`に対する相対パスです。

*`foreignReq`* `attribute::RootUrl`に対する相対URLまたは`attribute::AllowDirectUrls`が設定されている場合は絶対URLを指定できます。

*`catId`*&#x200B;が指定されていない場合は、セッションカタログが使用されます。

`srcE=`と`srcN=`は、ビネットに埋め込まれたマテリアルへのアクセスを提供します。

## サポートされるファイル形式 {#section-f2186d3eef834fc8bbecb2bc68daacad}

画像レンダリングでは、Dynamic Media Image Servingと同じソース画像形式をサポートしています。

Scene7 ピラミッドTIFF（PTIFF）の多解像度フォーマットを使用する場合、複数の異なる解像度の画像データを必要とするアプリケーションが最も効果的に機能します。 Image Servingには、サポートされている任意の形式からPTIFF画像を作成するImage Converter （IC）ユーティリティが含まれています。

サポートされているファイル形式の完全なリストについては、「画像サービング」ドキュメントのIC ユーティリティの説明を参照してください。

## プロパティ {#section-e68d03788d534e2184147987d51dfd0f}

マテリアル属性： 単色を除くすべてのマテリアルに必要です（単色のマテリアルには使用できません）。 すべての文字列では大文字と小文字が区別されます。*`index`* 0以上でなければなりません。

## 初期設定 {#section-dde549c1917540dc8f9555962202da3c}

なし

## 例 {#section-675865444f8a4d35b9fc6e58b36e3438}

別の繰り返し可能なテクスチャを持つカラーキャビネット用のMSS:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

同じマテリアルをレコード &#39;`12-3-2`&#39;のマテリアル カタログ `'cat`&#39;に含めることができます：

`…&obj=cabinets&src=cat/12-3-2&…`

テクスチャ画像を取得するためのImage Servingへのネストされたリクエスト：

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## 関連項目 {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[&#x200B; マテリアルカタログ &#x200B;](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)、[属性：:RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)、[属性：:AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)

