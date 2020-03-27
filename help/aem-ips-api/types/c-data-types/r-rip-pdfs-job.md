---
description: 既存のPDFアセットを再リッピングするプロセス。
seo-description: 既存のPDFアセットを再リッピングするプロセス。
seo-title: RipPdfsJob
solution: Experience Manager
title: RipPdfsJob
topic: Scene7 Image Production System API
uuid: 95990d53-4baf-44a2-8d84-3cab2b5c9105
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# RipPdfsJob{#rippdfsjob}

既存のPDFアセットを再リッピングするプロセス。

>[!NOTE]
>
>このジョブタイプは非推奨です。 今後のすべての `ReprocessAssetsJob` 統合に対してに移行します。

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>取り込むPDFファイルの配列へのハンドル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>マスクを作成するかどうかを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> manualCropOptions <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>手動切り抜きオプション </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> autoColorCropOptions <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>自動切り抜きオプション </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> autoTransparentCropOptions <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：PostTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postScriptOptions <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：PDFOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustrator Options</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>プロジェクトハンドルの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 電子メ <span class="varname"> ール設定</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>電子メールの設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>ファイルのアップロード先のURL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postImageServingPublishJob <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行される画像サービング公開ジョブのジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postImageRenderingPublishJob <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行される画像レンダリング公開ジョブのジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postVideoPublishJob <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行されるビデオ公開ジョブのジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Adobe InDesignファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ノックアウト <span class="varname"> の背景</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>選択した画像の背景をマスクします。 これにより、他のレイヤーの被写体画像の外側に透明部分を重ね合わせることができます。 </p> <p>（オプション） </p> <p>KnockoutBackgroundOptionsを参照してください<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 。</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 説明 {#section-0822e70fa4784131baa5ad0ba8c0fb3b}

選択肢は次のとお `*CropOptions` りです。

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

選択肢は次のとお `*PublishJob` りです。

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

