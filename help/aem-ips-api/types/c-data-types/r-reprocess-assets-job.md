---
description: PDFのリッピングや画像の再最適化など、以前にアップロードしたマスターファイルの再処理を許可するジョブタイプ。
seo-description: PDFのリッピングや画像の再最適化など、以前にアップロードしたマスターファイルの再処理を許可するジョブタイプ。
seo-title: ReprocessAssetsJob
solution: Experience Manager
title: ReprocessAssetsJob
topic: Scene7 Image Production System API
uuid: 5b4aa838-0fb4-4ae8-be5a-8ce1e1487127
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ReprocessAssetsJob{#reprocessassetsjob}

PDFのリッピングや画像の再最適化など、以前にアップロードしたマスターファイルの再処理を許可するジョブタイプ。

構文

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>アセットハンドル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>ファイルが公開準備完了とマークされているかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> preservePublishState <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>既存のアセットを上書きする際に、そのアセットの公開状態を保持するかどうかを制御します。 設定しない場合は、会社のデフォルト設定が使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>マスクを作成するかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 切り抜 <span class="varname"> きを保</span> 存 </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3">既存の作物定義の保存を制御します。 デフォルトは <span class="codeph"> trueです</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> manualCropOptions <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>手動切り抜きオプション </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> autoColorCropOptions <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>色に基づいて画像を自動的に切り抜くオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> autoTransparentCropOptions <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>透明度に基づいて、画像の端の余白を削除します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>PhotoshopファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postScriptOptions <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>PostScriptファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>PDFファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>音声ビデオメディアファイルのオプション </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustrator Options</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>IllustratorファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>アップロード時に指定できるオプション。 このセットは、アップロードのカラーの管理方法に影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> autoSetCreationOptions <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>アップロードされたファイルに適用する自動セット生成スクリプトの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>プロジェクトハンドルの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 電子メ <span class="varname"> ール設定</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>電子メール設定のオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postJobOnlyIfFiles <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>ファイルのみをアップロードするかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>ファイルのアップロード場所のURL。 </p> </td> 
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
   <td colname="col3"> <p>InDesignファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ノックアウト <span class="varname"> の背景</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>選択した画像の背景をマスクします。 これにより、他のレイヤーの被写体画像の外側に透明部分を重ね合わせることができます。 </p> <p>（オプション） </p> <p>KnockoutBackgroundOptionsを参照してください<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 。</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> unsharpMaskOptions <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 種類：UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>最適化されたピラミッドTIFファイルを作成する際に、アンシャープマスクの設定を制御するオプション。 これらの設定を使用して、画像のシャープさを改善します。 </p> <p>UnsharpMaskOptionsを参 <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_unsharp_mask_options.html"> 照してください</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**説明**

選択肢は次のとお `*CropOptions` りです。

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

選択肢は次のとお `*PublishJob` りです。

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

