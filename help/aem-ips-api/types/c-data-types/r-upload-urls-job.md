---
description: ファイルを取得する場所から URL をアップロードします。
solution: Experience Manager
title: UploadUrlsJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 28bca473-670f-4588-93fb-a6d6a692ce30
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 1%

---

# [!DNL UploadUrlsJob]{#uploadurlsjob}

ファイルを取得する場所から URL をアップロードします。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutoColorCropOptions</span> </td> 
   <td colname="col3"> 色に基づいて画像が自動的に切り抜かれるオプションです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AutoSetCreationOptions</span> </td> 
   <td colname="col3"> アップロードされたファイルに適用する自動セット生成スクリプトの配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> 透明度に基づいて、画像の端から空白を削除します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> マスクを作成するかどうか。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ColorManagementOptions</span> </td> 
   <td colname="col3"> アップロード中に指定できるオプション。 セットは、アップロードでのカラーの管理方法に影響します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> メール設定の選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：IllustratorOptions</span> </td> 
   <td colname="col3"> Illustratorファイルを Image Server にアップロードするためのオプションです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：InDesignOptions</span> </td> 
   <td colname="col3"> サーバーにInDesignファイルをアップロードするオプション。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3">選択した画像の背景をマスクします。 これにより、他のレイヤーに、被写体の画像の外側に透明度を付けてオーバーレイできます。 （オプション）詳しくは、<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ManualCropOptions</span> </td> 
   <td colname="col3"> 画像の手動切り抜きのオプションです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：MediaOptions</span> </td> 
   <td colname="col3">ビデオからサムネール画像を設定できるオプション。 詳しくは、 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numUrls</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3">ジョブで送信された URL の数を返します。 使用者 <a href="../../operations/c-operations-intro/c-methods/r-get-active-jobs.md#reference-67483cbd71d04042b48434d886e8a7a0" format="dita" scope="local"> getActiveJobs</a> および <a href="../../operations/c-operations-intro/c-methods/r-get-scheduled-jobs.md#reference-2bab1861325f4bff84c879d1efa9146e" format="dita" scope="local"> getScheduledJobs</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 上書き</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> アップロード時にファイルを上書きするかどうか。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PDFOptions</span> </td> 
   <td colname="col3"> Image Server にPDFファイルをアップロードするためのオプション。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PhotoshopOptions</span> </td> 
   <td colname="col3"> Photoshopファイルを Image Server にアップロードするためのオプションです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ファイルがアップロードされる URL。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> アップロードの完了後に実行される画像レンダリング公開ジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageServingPublishJob</span> </td> 
   <td colname="col3"> すべてのメディアオプション。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PostScriptOptions</span> </td> 
   <td colname="col3"> Post スクリプトファイルを Image Server にアップロードするためのオプションです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：VideoPublishJob</span> </td> 
   <td colname="col3"> アップロードの完了後に実行されるビデオ公開ジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 既存の切り抜き定義の保存を制御します。 デフォルトは true です </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 上書き時に既存のアセットの公開状態を保持するかどうかを制御します。 設定されていない場合は、会社のデフォルト設定が使用されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> プロジェクトハンドルの配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> ファイルの公開準備ができたとマークされているかどうか。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：UnCompressOptions</span> </td> 
   <td colname="col3">アップロードした TAR/ZIP ファイルの内容を、以下のオプション設定で抽出して処理します。 詳しくは、 <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UnsharpMaskOptions</span> </td> 
   <td colname="col3">最適化されたピラミッド TIF ファイルを作成する際に、アンシャープマスク設定を制御するオプションです。 これらの設定を使用すると、画像のシャープネスを改善できます。 詳しくは、 <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:UrlArray</span> </td> 
   <td colname="col3"> アップロードする URL の配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>アップロードジョブ内のすべての項目に対する追加のメタデータオプション。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 説明 {#section-637405ff7e0b4a71b83fd359b92fa0c2}

の場合 `CropOptions`を使用する場合、次のいずれかを選択できます。

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

の場合 `PublishJob`を使用する場合、次のいずれかを選択できます。

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`
