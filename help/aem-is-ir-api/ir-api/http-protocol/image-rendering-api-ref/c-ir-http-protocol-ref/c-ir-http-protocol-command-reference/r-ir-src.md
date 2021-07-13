---
description: マテリアルファイル。 マテリアルデータは、単一のマテリアルカタログ参照の形式、または1つまたは2つのイメージまたはマテリアルデータファイルとして、コンマで区切って指定します。
solution: Experience Manager
title: src
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 2%

---

# src{#src}

マテリアルファイル。 マテリアルデータは、単一のマテリアルカタログ参照の形式、または1つまたは2つのイメージまたはマテリアルデータファイルとして、コンマで区切って指定します。

`src = *``*|{{ *``*| *``*}[, *`catalogEntrymaterialFileembeddedReqmaterialFile`*]`

`srcE= *`name`*`

`srcN= *`索引`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span> | <span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'ir&amp;lbrace;'<span class="varname"> irReq</span>'&amp;rbrace;'|&amp;lbrace;'&amp;brace;'<span class="varname"> foreignReq</span>'&amp;rbrbrbrace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>マテリアルカタログID（<span class="codeph">属性：RootId</span>）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>マテリアルカタログエントリ(<span class="codeph"> catalog::Id</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>マテリアルスタイルファイル（<span class="filepath"> .vnc</span>または<span class="filepath"> .vnw</span>）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>画像データファイル。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>画像サービングに対する要求。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>イメージレンダリングのリクエスト。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>外部サーバーにリクエストします。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p></td> 
  <td class="stentry"> <p>埋め込みマテリアルの名前。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 索引</span> </p></td> 
  <td class="stentry"> <p>埋め込みマテリアルの0を基準とするインデックス番号。 </p></td> 
 </tr> 
</table>

繰り返し可能なテクスチャ、デカール、壁紙のマテリアルには、1つの画像が必要です。画像は、ファイルまたは埋め込み要求として指定できます。

キャビネットマテリアルにはキャビネットスタイルのファイル([!DNL .vnc])が必要です。このファイルはネストされた要求として指定できません。 テクスチャイメージファイルはキャビネット用にオプションで、指定した場合は、ファイルまたは埋め込み要求のいずれかになります。

窓の覆いのマテリアルには窓の覆いのスタイルファイル([!DNL .vnw])が必要です。これはネストされた要求としては指定できません。 テクスチャファイルはオプションで、指定する場合は、ファイルまたは埋め込み要求です。

画像レンダリングでは、マテリアルカタログ、カタログエントリ、データファイルを検索する際に、画像サービングと同じ規則が使用されます。 詳しくは、画像サービングのドキュメントの&#x200B;*`object`*&#x200B;データタイプの説明を参照してください。

*`materialFile`* は、に対する相対パスで `attribute::RootPath`す。

*`foreignReq`* には、からの相対URLを指定できま `attribute::RootUrl`す。が設定されている場合は、絶対URLを `attribute::AllowDirectUrls` 指定できます。

*`catId`*&#x200B;を指定しない場合は、セッションカタログが使用されます。

`srcE=` ビネット `srcN=` に埋め込まれたマテリアルへのアクセスを提供します。

## サポートされているファイル形式 {#section-f2186d3eef834fc8bbecb2bc68daacad}

画像レンダリングは、Dynamic Media画像サービングと同じソース画像形式をサポートします。

複数の異なる解像度の画像データを必要とするアプリケーションは、Scene7 Pyramid TIFF(PTIFF)多解像度形式を使用する場合に最適です。 画像サービングには、サポートされている任意の形式からPTIFF画像を作成するImage Converter(IC)ユーティリティが含まれています。

サポートされているファイル形式の完全なリストについては、画像サービングのドキュメントのICユーティリティの説明を参照してください。

## プロパティ {#section-e68d03788d534e2184147987d51dfd0f}

マテリアル属性。 べた塗りを除くすべてのマテリアルに必須です（べた塗りのマテリアルには使用できません）。 すべての文字列では大文字と小文字が区別されます。 *`index`* は0以上に設定する必要があります。

## 初期設定 {#section-dde549c1917540dc8f9555962202da3c}

なし

## 例 {#section-675865444f8a4d35b9fc6e58b36e3438}

繰り返し可能なテクスチャを別々に持つ色付きキャビネット用のMSS:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

同じマテリアルを、レコード&#39; `12-3-2`&#39;のマテリアルカタログ`'cat`&#39;に配置できます。

`…&obj=cabinets&src=cat/12-3-2&…`

テクスチャ画像を取得するための、画像サービングに対するネストされた要求：

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## 関連項目 {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[マテリアルカタログ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)、 [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)、 [attribute::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
