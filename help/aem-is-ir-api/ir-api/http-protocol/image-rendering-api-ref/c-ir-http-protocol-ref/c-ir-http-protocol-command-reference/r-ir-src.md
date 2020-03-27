---
description: マテリアルファイル 単一のマテリアルカタログ参照の形式、または1つまたは2つのイメージまたはマテリアルデータファイルとして、マテリアルデータをコンマで区切って指定します。
seo-description: マテリアルファイル 単一のマテリアルカタログ参照の形式、または1つまたは2つのイメージまたはマテリアルデータファイルとして、マテリアルデータをコンマで区切って指定します。
seo-title: src
solution: Experience Manager
title: src
topic: Scene7 Image Serving - Image Rendering API
uuid: 52751bcc-a65d-4441-a3b5-802d27b54b54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# src{#src}

マテリアルファイル 単一のマテリアルカタログ参照の形式、または1つまたは2つのイメージまたはマテリアルデータファイルとして、マテリアルデータをコンマで区切って指定します。

`src = *``*|{{ *``*| *``*}[, *`catalogEntrymaterialFileembeddedReqmaterialFile`*]`

`srcE= *`name`*`

`srcN= *`索引`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]recId<span class="varname"></span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">{'is{'<span class="varname"> isReq</span>'}'}|{'ir{'<span class="varname"> irReq</span>'}'|{'{'<span class="varname"> foreignReq</span>'}'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>マテリアルカタロ<span class="codeph"> グID(属性：:RootId</span>) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>マテリアルカタログエ<span class="codeph"> ントリ(catalog::Id</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>材料スタイルファ<span class="filepath"> イル(.vnc</span> ま <span class="filepath"> たは.vnw</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>画像データファイル </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>画像サービングへの要求。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>イメージレンダリングの要求を参照してください。 </p></td> 
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

繰り返し可能なテクスチャ、デカール、壁紙のマテリアルには、1つのイメージが必要です。このイメージは、ファイルまたは埋め込み要求として指定できます。

キャビネットマテリアルにはキャビネットスタイルのファ [!DNL .vnc]イル()が必要で、ネストされた要求として指定することはできません。 テクスチャイメージファイルはキャビネットのオプションで、指定する場合はファイルまたは埋め込み要求のいずれかです。

窓カバリングマテリアルには窓カバリングスタイルファイル( [!DNL .vnw])が必要ですが、これはネストされたリクエストとして指定できません。 テクスチャファイルはオプションで、指定する場合はファイルまたは埋め込み要求です。

画像レンダリングでは、画像サービングと同じ規則を使用して、マテリアルカタログ、カタログエントリ、データファイルを検索します。 詳しくは、画像サービングのドキュメ *`object`* ントのデータタイプの説明を参照してください。

*`materialFile`* はを基準とする相対パスで `attribute::RootPath`す。

*`foreignReq`* は、を基準とする相対URLか、設定さ `attribute::RootUrl`れている場合は絶対URLを指 `attribute::AllowDirectUrls` 定できます。

指定し *`catId`* なかった場合、セッションカタログが使用されます。

`srcE=` ビネット `srcN=` に埋め込まれたマテリアルにアクセスできます。

## サポートされるファイル形式 {#section-f2186d3eef834fc8bbecb2bc68daacad}

画像レンダリングは、Scene7画像サービングと同じソース画像形式をサポートします。

複数の異なる解像度の画像データを必要とするアプリケーションは、Scene7 Pyramid TIFF(PTIFF)の複数解像度形式を使用する場合に最適です。 画像サービングには、サポートされている任意の形式からPTIFF画像を作成するImage Converter(IC)ユーティリティが含まれています。

サポートされるファイル形式の完全なリストについては、画像サービングのドキュメントのICユーティリティの説明を参照してください。

## プロパティ {#section-e68d03788d534e2184147987d51dfd0f}

マテリアル属性。 べた塗り以外のすべてのマテリアルに対して必須です（べた塗りマテリアルには使用できません）。 すべての文字列では大文字と小文字が区別されます。 *`index`* は0以上に設定する必要があります。

## 初期設定 {#section-dde549c1917540dc8f9555962202da3c}

なし

## 例 {#section-675865444f8a4d35b9fc6e58b36e3438}

繰り返し可能な独立したテクスチャを持つ、色付きのキャビネットのMSS:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

同じ材料をレコード&#39;&#39;の材料カタ `'cat`ログ&#39;に配置でき `12-3-2`ます。

`…&obj=cabinets&src=cat/12-3-2&…`

テクスチャ画像を取得するための画像サービングへのネストされた要求：

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## 関連項目 {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[マテリア](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)ルカタログ、attribute [::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)、 [attribute::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
