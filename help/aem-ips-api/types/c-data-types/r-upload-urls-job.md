---
description: ファイルを取得する場所からURLをアップロードします。
seo-description: ファイルを取得する場所からURLをアップロードします。
seo-title: UploadUrlsJob
solution: Experience Manager
title: UploadUrlsJob
topic: Scene7 Image Production System API
uuid: 6140e969-bf61-4b62-9a60-29609626b0b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UploadUrlsJob{#uploadurlsjob}

ファイルを取得する場所からURLをアップロードします。

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
   <td colname="col1"> <span class="codeph"> autoColorCropOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：AutoColorCropOptions</span> </td> 
   <td colname="col3"> 色に基づいて画像を自動的に切り抜くオプションです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> autoSetCreationOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AutoSetCreationOptions</span> </td> 
   <td colname="col3"> アップロードされたファイルに適用する自動セット生成スクリプトの配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> autoTransparentCropOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> 透明度に基づいて、画像の端の余白を削除します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> マスクを作成するかどうか。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ColorManagementOptions</span> </td> 
   <td colname="col3"> アップロード時に指定できるオプション。 このセットは、アップロードのカラーの管理方法に影響します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 電子メ <span class="varname"> ール設定</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 電子メールの設定の選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：IllustratorOptions</span> </td> 
   <td colname="col3"> IllustratorファイルをImage Serverにアップロードするためのオプションです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：InDesignOptions</span> </td> 
   <td colname="col3"> InDesignファイルをサーバーにアップロードするためのオプションです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> ノックアウト <span class="varname"> の背景</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：KnockoutBackgroundOptions</span> </td> 
   <td colname="col3">選択した画像の背景をマスクします。 これにより、他のレイヤーの被写体画像の外側に透明部分を重ね合わせることができます。 （オプション）KnockoutBackgroundOptionsを参照<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"></a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> manualCropOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ManualCropOptions</span> </td> 
   <td colname="col3"> 画像の手動切り抜きのオプション。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：MediaOptions</span> </td> 
   <td colname="col3">ビデオのサムネール画像を設定するオプション。 詳しくは、MediaOptionsを参 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> 照してくださ</a>い。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numUrls</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3">ジョブで送信されたURLの数を返します。 getActiveJobsおよび <a href="../../operations/c-operations-intro/c-methods/r-get-active-jobs.md#reference-67483cbd71d04042b48434d886e8a7a0" format="dita" scope="local"> getScheduledJobs</a> で使用 <a href="../../operations/c-operations-intro/c-methods/r-get-scheduled-jobs.md#reference-2bab1861325f4bff84c879d1efa9146e" format="dita" scope="local"> されます</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 上書 <span class="varname"> き</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> アップロード時にファイルを上書きするかどうか。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PDFOptions</span> </td> 
   <td colname="col3"> PDFファイルをImage Serverにアップロードするためのオプションです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：PhotoshopOptions</span> </td> 
   <td colname="col3"> PhotoshopファイルをImage Serverにアップロードするためのオプションです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ファイルがアップロードされるURL。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postImageRenderingPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ImageRendingPublishJob</span> </td> 
   <td colname="col3"> アップロードの完了後に実行される画像レンダリング公開ジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postImageServingPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：ImageServingPublishJob</span> </td> 
   <td colname="col3"> すべてのメディアオプション。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postScriptOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PostScriptOptions</span> </td> 
   <td colname="col3"> Image Serverに投稿スクリプトファイルをアップロードするためのオプションです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postVideoPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：VideoPublishJob</span> </td> 
   <td colname="col3"> アップロードの完了後に実行されるビデオ公開ジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 切り抜 <span class="varname"> きを保</span> 存 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 既存の作物定義の保存を制御します。 デフォルトはtrueです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> preservePublishState <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 既存のアセットを上書きする際に、そのアセットの公開状態を保持するかどうかを制御します。 設定しない場合は、会社のデフォルト設定が使用されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：HandleArray</span> </td> 
   <td colname="col3"> プロジェクトハンドルの配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> ファイルが公開準備完了とマークされているかどうか。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> UnCompressOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：UnCompressOptions</span> </td> 
   <td colname="col3">アップロードしたTAR/ZIPファイルの内容を抽出し、次のオプション設定で処理します。 UnCompressOptionsを参 <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> 照してください</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> unsharpMaskOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：UnsharpMaskOptions</span> </td> 
   <td colname="col3">最適化されたピラミッドTIFファイルを作成する際に、アンシャープマスクの設定を制御するオプション。 これらの設定を使用して、画像のシャープさを改善します。 UnsharpMaskOptionsを参 <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> 照してください</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:UrlArray</span> </td> 
   <td colname="col3"> アップロードするURLの配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>アップロードジョブ内のすべてに対する追加のメタデータオプション。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 説明 {#section-637405ff7e0b4a71b83fd359b92fa0c2}

の場 `CropOptions`合、次のいずれかを選択できます。

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

の場 `PublishJob`合、次のいずれかを選択できます。

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`

