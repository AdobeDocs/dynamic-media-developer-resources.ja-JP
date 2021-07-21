---
description: 以前にアップロードされたファイルの承認済み書き出しを許可するジョブタイプ。
solution: Experience Manager
title: ExportJob
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: f0266b9f-c6e0-4843-b002-0bc068d43424
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 10%

---

# ExportJob{#exportjob}

以前にアップロードされたファイルの承認済み書き出しを許可するジョブタイプ。

ExportJobは次のアセットタイプをサポートしていません。

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
   <td colname="col2"> <p> <span class="codeph"> 型：HandleArray[がた：HandleArray]</span> </p> </td> 
   <td colname="col3" valign="top"> <p>書き出しが必要な<span class="codeph"> assetHandle</span>のリスト。 <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>を参照してください。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p><span class="codeph">の書き出しのタイプを指定します。使用可能な値</span>:[orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9"><span class="codeph"> fmt=orig</span>の場合、アセットは元のアセットとして書き出されます </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564"><span class="codeph"> fmt=convert</span>の場合、アセットは<span class="codeph"> is_modifer</span>または<span class="codeph">マクロ</span>の入力パラメーターで指定された形式に変換されます </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p><span class="codeph"> ImageServer</span>レンダリングURL文字列を指定します。この文字列は、 ExportJob <span class="codeph"> convert</span>リクエストに追加されます。 </p> <p>IS修飾子の送信について詳しくは、 <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/home.html" scope="external" format="html"> ISのドキュメント</a>を参照してください。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> マクロ</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>電子メールの設定の選択。 可能な値： </p> <p> 
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
   <td colname="col3"> <p>エクスポート要求を開始したクライアントまたは顧客のIPアドレスを指定します。 </p> <p> <p>注意： このパラメーターは現在は有効には設定されておらず、以降の使用にのみ厳密に予約されています。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

`fmt=convert`と、`is_modifier`と`macro`の両方が指定されたExportJobリクエストの場合、宛先ファイルは`macro`で指定された形式に従います。 例：

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```
