---
description: 指定したサーバーディレクトリから定期的にファイルをアップロードします。
seo-description: 指定したサーバーディレクトリから定期的にファイルをアップロードします。
seo-title: UploadDirectoryJob
solution: Experience Manager
title: UploadDirectoryJob
topic: Scene7 Image Production System API
uuid: 6e6ae415-7c54-4bbb-aa98-ff9a77d956b0
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# UploadDirectoryJob{#uploaddirectoryjob}

指定したサーバーディレクトリから定期的にファイルをアップロードします。

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
   <td colname="col1"> <span class="codeph"> autoColorOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：AutoColorOptions</span> </td> 
   <td colname="col3"> <p>画像の自動切り抜きオプション（色に基づく） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> autoSetCreationOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>アップロードされたファイルに適用する自動セット生成スクリプトの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> autoTransparentCropOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>透明度に基づいて、画像の端の余白を削除します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>アップロード時に指定できるオプション。 このセットは、アップロードのカラーの管理方法に影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>アップロード時にマスクを作成するかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>ファイルのIPSフォルダ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 電子メ <span class="varname"> ール設定</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>電子メールの設定の選択。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustrator Options</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：IllustratorOptions</span> </td> 
   <td colname="col3"> <p>IllustratorファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>アップロード時にサブフォルダを含めるかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：InDesignOptions</span> </td> 
   <td colname="col3"> <p>InDesignファイルをサーバーにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> ノックアウト <span class="varname"> の背景</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>選択した画像の背景をマスクします。 これにより、他のレイヤーの被写体画像の外側に透明部分を重ね合わせることができます。 </p> <p>（オプション） </p> <p>KnockoutBackgroundOptionsを参照し <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> てください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> manualCropOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ManualCropOptions</span> </td> 
   <td colname="col3"> <p>手動の画像切り抜きオプション </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：MediaOptions</span> </td> 
   <td colname="col3"> <p>ビデオのサムネール画像を設定するオプション。 </p> <p>詳しくは、MediaOptionsを参 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> 照してくださ</a>い。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 上書 <span class="varname"> き</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>ファイルのアップロードの上書きオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PDFOptions</span> </td> 
   <td colname="col3"> <p>PDFファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>PhotoshopファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>ファイルのアップロード先のURL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postImageRenderingPublish <span class="varname"></span></span>Job </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ImageRendingPublishJob</span> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行される画像レンダリング公開ジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postImageServingPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：ImageServingPublishJob</span> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行される画像サービング公開ジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postJobOnlyIfFiles <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>ファイルのみをアップロードするかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postScriptOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PostScriptOptions</span> </td> 
   <td colname="col3"> <p>投稿スクリプトファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postVideoPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：VideoPublishJob</span> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行されるビデオ公開ジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 切り抜 <span class="varname"> きを保</span> 存 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>既存の作物定義の保存を制御します。 デフォルトはtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> preservePublishState <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>既存のアセットを上書きする際に、そのアセットの公開状態を保持するかどうかを制御します。 設定しない場合は、会社のデフォルト設定が使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> processMetadataFiles <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>このジョブの個別のメタデータXMLファイルを処理するかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：HandleArray</span> </td> 
   <td colname="col3"> <p>プロジェクトハンドルの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>ファイルが公開準備完了とマークされるかどうかを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDir</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>ソースアップロードディレクトリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> UnCompressOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：UnCompressOptions</span> </td> 
   <td colname="col3"> <p>アップロードしたTAR/ZIPファイルの内容を抽出し、次のオプション設定で処理します。 </p> <p>UnCompressOptionsを参 <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> 照してください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> unsharpMaskOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>最適化されたピラミッドTIFファイルを作成する際に、アンシャープマスクの設定を制御するオプション。 これらの設定を使用して、画像のシャープさを改善します。 </p> <p>UnsharpMaskOptionsを参 <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_unsharp_mask_options.html"> 照してください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> xmpKeywords</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>アップロードジョブ内のすべてに対する追加のメタデータオプション </p> </td> 
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

