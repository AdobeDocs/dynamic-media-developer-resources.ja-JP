---
title: src
description: 材料ファイル。 単一のマテリアル カタログ リファレンスの形式で、または 1 つまたは 2 つのイメージ データ ファイルまたはマテリアル データ ファイルとして、カンマで区切ってマテリアル データを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 1%

---

# src{#src}

材料ファイル。 単一のマテリアル カタログ リファレンスの形式で、または 1 つまたは 2 つのイメージ データ ファイルまたはマテリアル データ ファイルとして、カンマで区切ってマテリアル データを指定します。

`src = *`catalogEntry`*|{{ *`materialFile`*| *`embeddedReq`*}[, *`materialFile`*]`

`srcE= *`name`*`

`srcN= *` インデックス `*`

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
  <td class="stentry"> <p><span class="codeph">&lbrace;'is&lbrace;'<span class="varname"> isReq</span>'&rbrace;'&rbrace;'&rbrace;|&lbrace;'ir&lbrace;'<span class="varname"> irReq</span>'&rbrace;'|&lbrace;'&lbrace;'<span class="varname"> foreignReq</span>'&rbrace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>マテリアル カタログ ID （<span class="codeph"> 属性：:RootId</span>） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>マテリアル カタログ エントリ（<span class="codeph"> catalog::Id</span>） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>材料スタイル ファイル（.vnc</span> または.vnw</span><span class="filepath"> な <span class="filepath">） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>画像データファイル。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>画像サービングのリクエスト。 </p></td> 
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
  <td class="stentry"> <p><span class="varname"> 名 </span> </p></td> 
  <td class="stentry"> <p>埋め込まれたマテリアルの名前。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 指数 </span> </p></td> 
  <td class="stentry"> <p>埋め込みマテリアルのインデックス番号（0 から始まります）。 </p></td> 
 </tr> 
</table>

繰り返し可能なテクスチャ、デカル転写、壁紙のマテリアルには単一のイメージが必要で、このイメージはファイルまたは埋め込み要求として指定できます。

キャビネット マテリアルにはキャビネット スタイル ファイル（[!DNL .vnc]）が必要ですが、ネストされた要求として指定することはできません。 テクスチャ イメージ ファイルは、キャビネットではオプションです。指定した場合は、ファイルまたは埋め込み要求のいずれかになります。

窓隠蔽マテリアルには窓隠蔽スタイル ファイル（[!DNL .vnw]）が必要です。このファイルはネストされた要求として指定できません。 テクスチャファイルはオプションであり、指定した場合はファイルまたは埋め込みリクエストのいずれかになります。

画像レンダリングでは、画像サービングと同じルールを使用して、材料カタログ、カタログエントリおよびデータファイルの検索を行います。 詳しくは、画像サービングドキュメントの *`object`* データタイプの説明を参照してください。

*`materialFile`* は、`attribute::RootPath` に対する相対パスです。

*`foreignReq`* `attribute::RootUrl` に対する相対 URL、または `attribute::AllowDirectUrls` が設定されている場合は絶対 URL を指定できます。

*`catId`* を指定しない場合、セッションカタログが使用されます。

`srcE=` と `srcN=` は、ビネットに埋め込まれた材料へのアクセスを提供します。

## サポートされているファイル形式 {#section-f2186d3eef834fc8bbecb2bc68daacad}

画像レンダリングは、Dynamic Media画像サービングと同じソース画像形式をサポートします。

複数の解像度の画像データを必要とするアプリケーションは、Scene7 Pyramid Format （PTIFF）の多解像度TIFFを使用する場合に最も高いパフォーマンスを発揮します。 画像サービングには、サポートされている任意の形式から PTIFF 画像を作成する画像コンバーター（IC）ユーティリティが含まれています。

サポートされるファイル形式の完全なリストについては、画像サービングドキュメントの IC ユーティリティの説明を参照してください。

## プロパティ {#section-e68d03788d534e2184147987d51dfd0f}

マテリアル アトリビュート。 単色を除くすべてのマテリアルに必要です（単色マテリアルには許可されません）。 すべての文字列では大文字と小文字が区別されます。 *`index`* 0 以上にする必要があります。

## 初期設定 {#section-dde549c1917540dc8f9555962202da3c}

なし

## 例 {#section-675865444f8a4d35b9fc6e58b36e3438}

別の繰り返し可能なテクスチャを持つ色付きキャビネットの MSS:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

レコード「`12-3-2`」の材料カタログ「`'cat`」に同じ材料が含まれている可能性があります：

`…&obj=cabinets&src=cat/12-3-2&…`

テクスチャ画像を取得するための画像サービングへのネストされたリクエスト：

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## 関連項目 {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[ マテリアル カタログ ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)、[attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)、[attribute::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
