---
title: src
description: マテリアルファイル。 マテリアルデータは、単一のマテリアルカタログ参照の形式で指定するか、1 つまたは 2 つのイメージまたはマテリアルデータファイルとして指定します。これらは、コンマで区切られます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 2%

---

# src{#src}

マテリアルファイル。 マテリアルデータは、単一のマテリアルカタログ参照の形式で指定するか、1 つまたは 2 つのイメージまたはマテリアルデータファイルとして指定します。これらは、コンマで区切られます。

`src = *`catalogEntry`*|{{ *`materialFile`*| *`embeddedReq`*}[, *`materialFile`*]`

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
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'ir&amp;lbrace;'<span class="varname"> irReq</span>'&amp;rbrace;'|&amp;lbrace;'&amp;lbrace;'<span class="varname"> foreignReq</span>'&amp;rbrace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>マテリアルカタログ ID (<span class="codeph"> attribute::RootId</span>) をクリックします。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>素材カタログエントリ (<span class="codeph"> catalog::Id</span>) をクリックします。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>マテリアルスタイルファイル (<span class="filepath"> .vnc</span> または <span class="filepath"> .vnw</span>) をクリックします。 </p></td> 
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
  <td class="stentry"> <p>画像レンダリングのリクエスト。 </p></td> 
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
  <td class="stentry"> <p>埋め込みマテリアルの 0 を基準とするインデックス番号。 </p></td> 
 </tr> 
</table>

繰り返し可能なテクスチャ、デカール、壁紙のマテリアルには、1 つの画像が必要です。画像は、ファイルまたは埋め込み要求として指定できます。

キャビネットのマテリアルにはキャビネットスタイルのファイル ( [!DNL .vnc]) で始まり、ネストされたリクエストとして指定することはできません。 テクスチャイメージファイルはキャビネット用のオプションで、指定した場合は、ファイルまたは埋め込み要求のどちらかです。

窓カバリングマテリアルには、窓カバリングスタイルファイル ( [!DNL .vnw]) で始まり、ネストされたリクエストとして指定することはできません。 テクスチャファイルはオプションで、指定した場合は、ファイルまたは埋め込み要求のどちらでもかまいません。

画像レンダリングでは、マテリアルカタログ、カタログエントリ、およびデータファイルを検索する際に、画像サービングと同じ規則が使用されます。 詳しくは、 *`object`* 詳しくは、画像サービングドキュメントのデータタイプを参照してください。

*`materialFile`* 次に対する相対パスです： `attribute::RootPath`.

*`foreignReq`* 次に対する相対 URL を指定できます。 `attribute::RootUrl`、または `attribute::AllowDirectUrls` が設定されている。

If *`catId`* が指定されていない場合、セッションカタログが使用されます。

`srcE=` および `srcN=` ビネットに埋め込まれたマテリアルにアクセスできます。

## サポートされているファイル形式 {#section-f2186d3eef834fc8bbecb2bc68daacad}

画像レンダリングは、Dynamic Media画像サービングと同じソース画像形式をサポートします。

複数の異なる解像度の画像データを必要とするアプリケーションは、Scene7 PTIFF(Pyramid Resolution) マルチ解像度形式を使用する場合に最も高いパフォーマンスを発揮します。 画像サービングには、サポートされる任意の形式から PTIFF 画像を作成する画像コンバーター (IC) ユーティリティが含まれています。

サポートされるファイル形式の完全なリストについては、画像サービングドキュメントの IC ユーティリティの説明を参照してください。

## プロパティ {#section-e68d03788d534e2184147987d51dfd0f}

材料属性。 べた塗りを除くすべてのマテリアルに必須です（べた塗りのマテリアルには使用できません）。 すべての文字列では大文字と小文字が区別されます。 *`index`* 0 以上の値を指定する必要があります。

## 初期設定 {#section-dde549c1917540dc8f9555962202da3c}

なし

## 例 {#section-675865444f8a4d35b9fc6e58b36e3438}

色彩を帯びたキャビネットの MSS で、繰り返し可能な別のテクスチャを使用：

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

同じ材料を材料カタログに含めることができます `'cat`「 」 （レコード「 」内） `12-3-2`&#39;:

`…&obj=cabinets&src=cat/12-3-2&…`

テクスチャ画像を取得するための、画像サービングに対するネストされた要求：

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## 関連項目 {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[マテリアルカタログ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402), [attribute::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
