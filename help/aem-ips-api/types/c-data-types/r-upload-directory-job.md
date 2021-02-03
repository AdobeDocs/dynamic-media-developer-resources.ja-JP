---
description: 指定したサーバーディレクトリからファイルを定期的にアップロードします。
seo-description: 指定したサーバーディレクトリからファイルを定期的にアップロードします。
seo-title: UploadDirectoryJob
solution: Experience Manager
title: UploadDirectoryJob
topic: Dynamic Media Image Production System API
uuid: 6e6ae415-7c54-4bbb-aa98-ff9a77d956b0
translation-type: tm+mt
source-git-commit: d38df1eb4713c034727ad0eb10834dc156122beb
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 1%

---


# UploadDirectoryJob{#uploaddirectoryjob}

指定したサーバーディレクトリからファイルを定期的にアップロードします。

構文

## パラメータ {#section-69c07f4e7b2e4a0fba143ffaa9f4d48f}

<table id="table_6E40A78846F444BDB8E437413B90CFCE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名前 </p> </th> 
   <th colname="col2" class="entry"> <p>種類 </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：AutoColorOptions</span> </td> 
   <td colname="col3"> <p>画像の自動切り抜きオプション（色に基づく） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>アップロードされたファイルに適用する自動セット生成スクリプトの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>透明度に基づいて、画像の端から空白を削除します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>アップロード中に指定できるオプション。 このセットは、アップロード時のカラーの管理方法に影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>アップロード時にマスクを作成するかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>ファイルのIPSフォルダ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>電子メールの設定の選択。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：IllustratorOptions</span> </td> 
   <td colname="col3"> <p>IllustratorファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>アップロード時にサブフォルダを含めるかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：InDesignOptions</span> </td> 
   <td colname="col3"> <p>InDesignファイルをサーバーにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>選択した画像の背景をマスクします。 これにより、他のレイヤーの中で、被写体の画像の外側に透明部分を持つレイヤーを重ね合わせることができます。 </p> <p>（オプション） </p> <p><a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ManualCropOptions</span> </td> 
   <td colname="col3"> <p>手動による画像切り抜きオプション </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：MediaOptions</span> </td> 
   <td colname="col3"> <p>ビデオのサムネール画像を設定するためのオプション。 </p> <p><a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 上書き</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>ファイルのアップロードの上書きオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PDFOptions</span> </td> 
   <td colname="col3"> <p>PDFファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>PhotoshopファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>ファイルのアップロード先のURL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ImageRendingPublishJob</span> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行される画像レンダリング公開ジョブの詳細です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ImageServingPublishJob</span> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行される画像サービング公開ジョブの詳細です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>ファイルのみをアップロードするかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PostScriptOptions</span> </td> 
   <td colname="col3"> <p>投稿スクリプトファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：VideoPublishJob</span> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行されるビデオ公開ジョブの詳細です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>既存の切り抜き定義の保存を制御します。 デフォルトはtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>既存のアセットを上書きする際に、そのアセットの公開状態を保持するかどうかを制御します。 設定されていない場合は、会社のデフォルト設定が使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processMetadataFiles</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>このジョブ用に個別のメタデータXMLファイルを処理するかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：HandleArray</span> </td> 
   <td colname="col3"> <p>プロジェクトハンドルの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>ファイルが公開準備完了とマークされるかどうかを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDir</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>ソースアップロードディレクトリ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：UnCompressOptions</span> </td> 
   <td colname="col3"> <p>アップロードしたTAR/ZIPファイルの内容を抽出し、次のオプション設定で処理します。 </p> <p><a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>最適化されたピラミッドTIFファイルを作成する際に、アンシャープマスクの設定を制御するためのオプション。 これらの設定を使用して、画像のシャープさを向上させます。 </p> <p><a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnsharpMaskOptions</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>アップロードジョブ内のすべての項目に対する追加のメタデータオプション </p> </td> 
  </tr> 
 </tbody> 
</table>

## 説明 {#section-637405ff7e0b4a71b83fd359b92fa0c2}

`CropOptions`の場合は、次のいずれかを選択できます。

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

`PublishJob`の場合は、次のいずれかを選択できます。

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`

