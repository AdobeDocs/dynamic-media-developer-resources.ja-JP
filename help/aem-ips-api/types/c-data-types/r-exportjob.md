---
description: 以前にアップロードされたファイルの承認されたエクスポートを許可するジョブタイプ。
seo-description: 以前にアップロードされたファイルの承認されたエクスポートを許可するジョブタイプ。
seo-title: ExportJob
solution: Experience Manager
title: ExportJob
topic: Dynamic Media Image Production System API
uuid: 439e3dd8-85b8-4f5b-abf8-8cc5a3f59fe6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 10%

---


# ExportJob{#exportjob}

以前にアップロードされたファイルの承認されたエクスポートを許可するジョブタイプ。

ExportJobは、次のアセットタイプをサポートしていません。

* 画像セット
* レンダリングセット
* スピンセット
* メディアセット
* マルチビットレートセット
* ビデオセット
* eCatalog
* オファーセット

<table id="table_D8F3FD30D15648BFA5B980D3DC0A5AB1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 型：HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>書き出す必要がある<span class="codeph"> assetHandle</span>のリスト。 <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>を参照してください。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p><span class="codeph">エクスポートのタイプを指定します。可能な値</span>:[orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9"><span class="codeph"> fmt=orig</span>の場合、アセットは元のアセットとして書き出されます。 </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564"><span class="codeph"> fmt=convert</span>の場合、アセットは、<span class="codeph"> is_modifer</span>または<span class="codeph"> macro</span>の入力パラメーターで指定された形式に変換されます </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p><span class="codeph"> ImageServer</span>レンダリングURL文字列を指定します。このURL文字列は、ExportJob <span class="codeph"> convert</span>リクエストに追加されます。 </p> <p>IS修飾子の送信について詳しくは、<a href="https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-serving-api/home.html" scope="external" format="html"> ISドキュメント</a>を参照してください。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>電子メール設定の選択。 可能な値： </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> すべて</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> エラー</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> JobCompletion</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> なし</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> clientId</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>エクスポート要求を開始したクライアントまたは顧客のIPアドレスを指定します。 </p> <p> <p>注意： このパラメーターは、現在は有効に設定されておらず、将来の使用のみを目的として厳密に予約されています。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

`fmt=convert`と`is_modifier`と`macro`の両方が指定されるExportJobリクエストの場合、宛先ファイルには`macro`が指定する形式が使用されます。 例：

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```

