---
description: 以前にアップロードされたファイルの承認されたエクスポートを許可するジョブタイプ。
seo-description: 以前にアップロードされたファイルの承認されたエクスポートを許可するジョブタイプ。
seo-title: ExportJob
solution: Experience Manager
title: ExportJob
topic: Scene7 Image Production System API
uuid: 439e3dd8-85b8-4f5b-abf8-8cc5a3f59fe6
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 型：HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>書き出す必 <span class="codeph"> 要があ</span> るassetHandleのリスト。 HandleArrayを参 <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> 照</a>。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>書き出しのタイプを指 <span class="codeph"> 定します。可能な値</span>:[orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">fmt=orig <span class="codeph"> の場合</span>、アセットは元のアセットとして書き出されます </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">fmt=convert <span class="codeph"> (</span>fmt=convert <span class="codeph"> )の場合、アセットは、</span> is_modiferまたはマクロ入力パラメータで指定された形式に変 <span class="codeph"> 換されます</span> 。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>ExportJobの変換要 <span class="codeph"> 求に追加される</span> 、ImageServerレンダリングURL文字列を <span class="codeph"> 指定します</span> 。 </p> <p>IS修飾子の送信の詳細については、 <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/" scope="external" format="html"> ISのドキュメント</a> （英語のみ）を参照してください。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> マク <span class="varname"> ロ</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 電子メ <span class="varname"> ール設定</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> clientId</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>エクスポート要求を開始したクライアントまたは顧客のIPアドレスを指定します。 </p> <p> <p>注意： このパラメーターは、現在は有効には設定されておらず、今後の使用のみを目的として厳密に予約されています。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

との両方が指定され `fmt=convert` ているExportJobリクエ `is_modifier` スト `macro` の場合、宛先ファイルはで指定された形式に従いま `macro`す。 例：

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```

