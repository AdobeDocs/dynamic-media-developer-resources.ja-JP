---
description: 以前にアップロードしたファイルの承認済みエクスポートを許可するジョブタイプ。
solution: Experience Manager
title: ExportJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f0266b9f-c6e0-4843-b002-0bc068d43424
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 10%

---

# [!DNL ExportJob]{#exportjob}

以前にアップロードしたファイルの承認済みエクスポートを許可するジョブタイプ。

ExportJob は、次のアセットタイプをサポートしていません。

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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL assetHandleArray]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 型：HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>書き出 <span class="codeph"> 必要な assetHandle</span> リストです。 HandleArray</a> を参照 <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> てください。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL fmt]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>書き出しの種類 <span class="codeph"> 指定します。可能な値 </span>: [orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">fmt=orig</span><span class="codeph"> 場合、アセットはオリジナルとしてエクスポートされます </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">fmt=convert</span> の場 <span class="codeph">、アセットは <span class="codeph"> is_modifer</span> またはマクロの入力パラメーターで指定された形式 <span class="codeph"> 変換 </span> れます </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL is_modifier]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>ExportJob <span class="codeph"> convert</span> リクエストに追加される <span class="codeph"> ImageServer</span> レンダリング URL 文字列を指定します。 </p> <p>IS 修飾子の送信について詳しくは </a><a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/homeisir.html" scope="external" format="html"> IS のドキュメントを参照してください。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL macro]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>メール設定の選択。 使用可能な値： </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> 全 </span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> エラー </span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> JobCompletion</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> なし </span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL clientId]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>書き出しリクエストを開始したクライアントまたは顧客の IP アドレスを指定します。 </p> <p> <p>メモ：このパラメーターは現在アクティブには入力されておらず、今後の使用のためにのみ厳密に予約されています。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

`fmt=convert` と `is_modifier` と `macro` の両方が指定されている ExportJob リクエストの場合、宛先ファイルは `macro` によって提供される形式に従います。 以下に例を挙げます。

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```
