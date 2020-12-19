---
description: マテリアルファイル マテリアルデータは、1つのマテリアルカタログ参照の形式で指定するか、1つまたは2つのイメージまたはマテリアルデータファイルとして指定し、カンマで区切ります。
seo-description: マテリアルファイル マテリアルデータは、1つのマテリアルカタログ参照の形式で指定するか、1つまたは2つのイメージまたはマテリアルデータファイルとして指定し、カンマで区切ります。
seo-title: src
solution: Experience Manager
title: src
topic: Scene7 Image Serving - Image Rendering API
uuid: 52751bcc-a65d-4441-a3b5-802d27b54b54
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 2%

---


# src{#src}

マテリアルファイル マテリアルデータは、1つのマテリアルカタログ参照の形式で指定するか、1つまたは2つのイメージまたはマテリアルデータファイルとして指定し、カンマで区切ります。

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
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;brace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'ir&amp;lbrace;'<span class="varname"> ir&amp;brace</span>'&amp;rbrace;'&amp;lbrace;'<span class="varname"> foreignReq</span>'&amp;rbracace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>マテリアルカタログID （<span class="codeph">属性：:RootId</span>） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>マテリアルカタログエントリ（<span class="codeph">カタログ：:Id</span>） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>材料スタイルファイル（<span class="filepath"> .vnc</span>または<span class="filepath"> .vnw</span>） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>画像データファイル </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>画像サービングに対する要求 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>イメージレンダリングの要求を参照してください。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>外部サーバーへのリクエスト。 </p></td> 
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

繰り返し可能なテクスチャ、デカール、壁紙のマテリアルには、1つのイメージが必要です。イメージは、ファイルまたは埋め込みリクエストとして指定できます。

キャビネットマテリアルにはキャビネットスタイルのファイル([!DNL .vnc])が必要で、ネストされた要求として指定できません。 テクスチャイメージファイルはキャビネットではオプションで、指定する場合はファイルまたは埋め込み要求のどちらかです。

窓カバリングマテリアルにはウィンドウカバリングスタイルファイル( [!DNL .vnw])が必要です。これはネストされた要求として指定できません。 テクスチャファイルはオプションで、指定する場合はファイルまたは埋め込み要求になります。

画像レンダリングでは、マテリアルカタログ、カタログエントリ、データファイルを検索する場合に、画像サービングと同じ規則が使用されます。 詳しくは、画像サービングのドキュメントの&#x200B;*`object`*&#x200B;データタイプの説明を参照してください。

*`materialFile`* は、を基準とする相対パスで `attribute::RootPath`す。

*`foreignReq`* は、を基準とする相対URL `attribute::RootUrl`か、設定されている場合は絶対URL `attribute::AllowDirectUrls` です。

*`catId`*&#x200B;を指定しない場合は、セッションカタログが使用されます。

`srcE=` ビネットに埋め込まれたマテリアルにアクセスで `srcN=` きます。

## サポートされるファイル形式{#section-f2186d3eef834fc8bbecb2bc68daacad}

画像レンダリングは、Scene7画像サービングと同じソース画像形式をサポートします。

複数の異なる解像度の画像データを必要とするアプリケーションは、Scene7ピラミッドTIFF(PTIFF)マルチ解像度形式を使用する場合に最適です。 画像サービングには、サポートされている任意の形式からPTIFF画像を作成するImage Converter(IC)ユーティリティが含まれています。

サポートされるファイル形式の完全なリストについては、画像サービングのドキュメントのICユーティリティの説明を参照してください。

## プロパティ {#section-e68d03788d534e2184147987d51dfd0f}

マテリアル属性 べた塗り以外のすべてのマテリアルに対して必須です（べた塗りマテリアルには使用できません）。 すべての文字列では大文字と小文字が区別されます。 *`index`* は0以上に設定する必要があります。

## 初期設定 {#section-dde549c1917540dc8f9555962202da3c}

なし

## 例 {#section-675865444f8a4d35b9fc6e58b36e3438}

繰り返し可能なテクスチャが独立した、色彩の統一されたキャビネットのMSS:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

レコード&#39; `12-3-2`&#39;のマテリアルカタログ`'cat`&#39;に同じマテリアルを配置できます。

`…&obj=cabinets&src=cat/12-3-2&…`

テクスチャ画像を取得するための画像サービングへのネストされた要求：

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## 関連項目 {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[マテリアルカタログ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)、 [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)、 [attribute::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
