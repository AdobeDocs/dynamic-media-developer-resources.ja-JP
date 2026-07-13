---
description: PDFのリッピングや画像の再最適化など、以前アップロードしたプライマリファイルの再処理を可能にするジョブタイプ。
solution: Experience Manager
title: ReprocessAssetsJob
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6078246-54e1-4119-b4f8-ba6a28577cff
TQID: 'https://experienceleague.adobe.com/soVm4QrX3QSTIstkVAdeQlKPOB3ri38pcHOV51roczI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 453
ht-degree: 1%

---

# [!DNL ReprocessAssetsJob]{#reprocessassetsjob}

PDFのリッピングや画像の再最適化など、以前アップロードしたプライマリファイルの再処理を可能にするジョブタイプ。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

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
   <td colname="col2"> <p><span class="codeph">種類：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>アセットのハンドル： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>ファイルが公開可能にマークされているかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>上書き時に既存アセットの公開状態を保持するかどうかを制御します。 設定しない場合は、会社のデフォルト設定が使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>マスクを作成するかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>既存の切り抜き定義の保存を制御します。 初期設定は true。</p> <p>manualCropOptions パラメーターと対応する値を指定すると、preserveCropの値に関係なく、新しい値（0,0,0,0を除く）がアセットに適用されます。</p><p>manualCropOptions パラメーターを<i>not</i>指定した場合、preserveCropの値は維持されます。 また、trueの場合は既存のpreserveCrop値が保持され、falseの場合はpreserveCrop値が削除されます。</p><p>例：</p><p><p>&lt;preserveCrop&gt;false&lt;/preserveCrop&gt;<br />&lt;manualCropOptions&gt;<br />&lt;left&gt;190&lt;/left&gt;<br /> &lt;right&gt;310&lt;/right&gt;<br /> &lt;top&gt;160&lt;/top&gt;<br /> &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualCropOptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>手動切り抜きオプション： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>色に基づいて画像を自動的に切り抜くオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>透明度に基づいて、画像のエッジから余白を削除します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Photoshop ファイルをImage Serverにアップロードするためのオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>PostScript ファイルをImage Serverにアップロードするためのオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>PDF ファイルをImage Serverにアップロードするためのオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>A/V メディアファイルオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Illustrator ファイルをImage Serverにアップロードするためのオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>アップロード時に指定できるオプション。 設定は、アップロードのカラーの管理方法に影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>アップロードされたファイルに適用する自動セット生成スクリプトの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>プロジェクトハンドルの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>メール設定のオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>ファイルのみをアップロードするかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>ファイルのアップロード場所へのURL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>アップロード完了後に実行される画像サービング公開ジョブのジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>アップロード完了後に実行される画像レンダリング公開ジョブのジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>アップロード完了後に実行されるビデオ公開ジョブのジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>InDesign ファイルをイメージサーバーにアップロードするためのオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>選択した画像の背景をマスク これにより、被写体の画像以外の透明度を持つ他のレイヤーでオーバーレイできます。 </p> <p>オプション。 </p> <p>「<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>」を参照してください </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">種類：UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>最適化されたピラミッド TIF ファイルを作成する際に、アンシャープマスク設定を制御できるオプション。 これらの設定を使用して、画像のシャープネスを向上させます。 </p> <p><a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnsharpMaskOptions</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**メモ**

`*CropOptions`の選択肢は次のとおりです。

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

`*PublishJob`の選択肢は次のとおりです。

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

