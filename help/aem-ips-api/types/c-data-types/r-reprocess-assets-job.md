---
description: ジョブタイプ：リッピングPDFの再処理や画像の再最適化を含む、以前にアップロードしたプライマリファイルの再処理を許可するジョブタイプ。
solution: Experience Manager
title: ReprocessAssetsJob
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6078246-54e1-4119-b4f8-ba6a28577cff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 2%

---

# [!DNL ReprocessAssetsJob]{#reprocessassetsjob}

ジョブタイプ：リッピングPDFの再処理や画像の再最適化を含む、以前にアップロードしたプライマリファイルの再処理を許可するジョブタイプ。

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>アセットハンドル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>ファイルの公開準備ができたとマークされているかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>上書き時に既存のアセットの公開状態を保持するかどうかを制御します。 設定されていない場合は、会社のデフォルト設定が使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>マスクを作成するかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>既存の切り抜き定義の保存を制御します。 初期設定は true。</p> <p>manualCropOptions パラメーターと対応する値を指定した場合、preserveCrop の値に関係なく、新しい値（0、0、0、0 を除く）がアセットに適用されます。</p><p>もし <i>not</i> manualCropOptions パラメーターを指定した場合、preserveCrop の値は維持されます。 また、true の場合、既存の preserveCrop 値は保持されます。false の場合、preserveCrop 値は削除されます。</p><p>例：</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>手動切り抜きオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>色に基づいて画像が自動的に切り抜かれるオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>透明度に基づいて、画像の端から空白を削除します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Photoshopファイルを Image Server にアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>PostScript ファイルを Image Server にアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>Image Server にPDFファイルをアップロードするためのオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>音声ビデオメディアファイルオプション </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Illustratorファイルを Image Server にアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>アップロード中に指定できるオプション。 セットは、アップロードでのカラーの管理方法に影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>アップロードされたファイルに適用する自動セット生成スクリプトの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>プロジェクトハンドルの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>電子メール設定のオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>ファイルのみをアップロードするかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>ファイルのアップロード場所の URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行される画像サービング公開ジョブのジョブ詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行される画像レンダリング公開ジョブのジョブ詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>アップロードの完了後に実行されるビデオ公開ジョブのジョブ詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Image Server にInDesignファイルをアップロードするためのオプション </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>選択した画像の背景をマスクします。 これにより、他のレイヤーに、被写体の画像の外側に透明度を付けてオーバーレイできます。 </p> <p>（オプション） </p> <p>詳しくは、<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>最適化されたピラミッド TIF ファイルを作成する際に、アンシャープマスク設定を制御するオプションです。 これらの設定を使用すると、画像のシャープネスを改善できます。 </p> <p>詳しくは、 <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**説明**

選択肢 `*CropOptions` 次を含む：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

選択肢 `*PublishJob` 次を含む：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
