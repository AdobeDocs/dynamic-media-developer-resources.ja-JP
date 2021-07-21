---
description: 既存のPDFアセットを再リップするプロセス。
solution: Experience Manager
title: RipPdfsJob
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 7a787b45-3cda-44f2-8357-8b6217b679e0
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 2%

---

# RipPdfsJob{#rippdfsjob}

既存のPDFアセットを再リップするプロセス。

>[!NOTE]
>
>このジョブタイプは非推奨です。 今後のすべての統合のために`ReprocessAssetsJob`に移行します。

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名前 </p> </th> 
   <th colname="col2" class="entry"> <p>種類 </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：HandleArray[がた：HandleArray]</span> </p> </td> 
   <td colname="col3"> <p>切り取るPDFファイルの配列に対する処理。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>マスクを作成するかどうかを決定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>手動切り抜きオプション </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>自動切り抜きオプション </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：PostTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：PostScriptOptions[たいぷ：PostScriptOptions]</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：PDFOptions[たいぷ：PDFOptions]</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：IllustratorOptions[たいぷ：IllustratorOptions]</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：ColorManagementOptions[がた：ColorManagementOptions]</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：HandleArray[がた：HandleArray]</span> </p> </td> 
   <td colname="col3"> <p>プロジェクトハンドルの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>電子メールの設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>ファイルのアップロード先のURL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：ImageServingPublishJob[がた：ImageServingPublishJob]</span> </p> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行される画像サービング公開ジョブのジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行される画像レンダリング公開ジョブのジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行されるビデオ公開ジョブのジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：InDesignOptions[がた：InDesignOptions]</span> </p> </td> 
   <td colname="col3"> <p>Adobe InDesignファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>選択した画像の背景をマスクします。 これにより、他のレイヤーに、被写体の画像の外側の透明度でオーバーレイできます。 </p> <p>（オプション） </p> <p><a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 説明 {#section-0822e70fa4784131baa5ad0ba8c0fb3b}

`*CropOptions`の選択肢は次のとおりです。

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

`*PublishJob`の選択肢は次のとおりです。

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
