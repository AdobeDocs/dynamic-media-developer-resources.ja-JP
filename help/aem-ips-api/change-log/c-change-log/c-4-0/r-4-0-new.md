---
title: 新しい追加と変更
description: IPS API v4.0 の新しい変更点と実装された変更点について説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 0%

---

# 新しい追加と変更{#new-additions-and-changes}

IPS API v4.0 の新しい変更点と実装された変更点について説明します。

個別の WSDL とスキーマ名前空間を使用して並列処理された API バージョンを実装しました。

* 以前の API バージョン：`IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`。
* SPS 4.0 バージョン：`IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`。

フィールド `PostScriptOptions/alpha` 追加しました。

`VideoRootUrl` 操作に `SwfRootUrl` と `getProperty` のプロパティを追加しました。

呼び出し元のアプリケーションを追跡するために、オプションの `appName` パラメーターと `appVersion` パラメーターを `authHeader` に追加しました。 `ipsApiService.log` にログを追加しました。

WSDL 生成サーブレットにオプションの `serviceUrl` パラメーターを追加しました。 このパラメーターはデバッグプロキシで役立ちます。 例：`http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

操作 `getZipEntries` 実装しました。

システムフィールド条件に検索範囲と型指定された比較値を実装しました。

主 `'Asset'` クロスアセットメタデータフィールドを許可するために、アセットタイプの文字列定数を追加しました。

`trashState` 用 `searchAssets` パラメーターを実装しました。

操作 `getAssetPublishHistory` 実装しました。

Flexでの障害処理を有効にするためのオプションの `faultHttpStatusCode` SOAP ヘッダーを追加しました。 Flexの場合は、`<faultHttpStatusCode>200</faultHttpStatusCode>` を使用します。 障害応答のデフォルトのステータスコードは `500 (Internal Server Error)` です。

ごみ箱からアセットを復元したり、ごみ箱から空のアセットを復元したりする操作を追加しました。

CRUD 操作を実装しました。

`ImageMap` のタイプおよび `saveImageMap` 操作に有効フラグを追加しました。

残りのファイルジョブの最適化のサポートを追加しました。

一括公開状態アップデート用に `setAssetsPublishState` を追加しました。

`ImageServingPublishSettings`、`getImageServingPublishSettings`、`setImageServingPublishSettings` を追加しました。

新しい `saveMetadataField` および `createMetadataField` の操作に置き換えて、`updateMetadataField` の操作を非推奨（廃止予定）としました。

バッチ削除操作 `deleteAssetsParam` 実装しました。

バッチ移動操作 `moveAssetsParam` 実装しました。

操作 `deleteMetadataField` 実装しました。

`get/setImageRenderingPublishSettings`、`get/set/create/updateVignettePublishFormat` 操作を実装しました。

実装 `getAssetCounts`。

アセットに `setImageSetMembers` メンバーを含めるためのサポートを `RenderSet` に追加 `ImageSet` ました。

操作 `replaceImage` 追加しました。

操作 `copyImage` 追加しました。

`setUrlModifier`、`urlModifier/urlPostApplyModifier`、`LayerViewInfo` に `TemplateInfo` 操作フィールドと `WatermarkInfo` フィールドを追加しました。

操作 `createDerivedAsset` 追加しました。 現在、`ownerHandle` は画像アセットを参照する必要があり、タイプは `AdjustedView` または `LayerView` です。

操作 `createTemplate` 追加しました。 テンプレートまたは透かしアセットを作成するための呼び出し。

Web サービス API に移植される、`CompanySettings` の IPS 会社設定。

操作 `excludeByproducts` フィルターフラグ `searchAssets` 追加しました。 このフラグを true に設定すると、画像とPDF`PSDlayer` 取り込まれた画像が実行されます。

操作 `getGenerationInfo` 追加しました。

操作 `SystemMessage` プロパティ名を追加 `getProperty` ました。

一部のアセットタイプ文字列定数を、対応するアセット情報フィールドに一致するように変更しました。

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

成功、警告およびエラーを要約するために、バッチ操作の結果形式を変更しました。

バッチメタデータ操作 `batchSetAssetMetadata` 実装しました。

アプリ固有のデータのサポートを実装しました。

アップロードジョブの `createTemplate`、`extendLayers`、`extractText` のブールフラグのサポートを実装して、Photoshop処理のプロセス（ファイルのアップロードを追加する場合の変更と同様）を制御できるようになりました。

`setImageMaps` および `setZoomTargets` の操作を実装しました。

`ViewerPreset` 操作を実装しました。 認識されるタイプは次のとおりです。

* `VideoPlayer` （ビデオではこれらのビューアのみが公開されます）。
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

ビューアスキンは、`skinFg` と `skinBg` の 2 つのパラメーターをサポートしています。 バックエンドコードは、後方互換性を維持するために必要なすべての処理を行います。

操作 `getAssociatedAssets` 実装しました。

以前 `ReprocessAssets` アップロードしたプライマリソースファイルの再処理（PDF の再取り込みや画像の再最適化など）を可能にするジョブタイプが追加されました。

`PropertySetType` フィールドタイプの名前を `propertyType` に変更しました。 この名前の変更は、`createPropertySetType` パラメーターと応答 `getPropertySetType/getPropertySetTypes` 影響します。

画像ユーザーデータやその他の編集可能な画像フィールドの設定をサポートする `batchSetImageFields` 操作を実装しました。

47 様々なアセット情報タイプに fileSize フィールドを追加しました。

* `VignetteInfo`
* `CabinetInfo`
* `WindowCoveringInfo`
* `IccProfileInfo`
* `FontInfo`
* `XslInfo`
* `ViewerSwfInfo`
* `XmlInfo`
* `SvgInfo`
* `ZipInfo`
* `VideoInfo`
* `AcoInfo`
* `PdfInfo`
* `PsdInfo`
* `FlashInfo`
* `InDesignInfo`
* `PostScriptInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `RTFInfo`

操作 `getActivePublishContexts` 実装しました。 この操作は、指定された会社のアクティブな公開サーバーを含む公開コンテキスト名の配列を返します。 現在の公開コンテキスト名は次のとおりです。

* `ImageServing`
* `ImageRendering`
* `Video`

操作 `getSearchStrings` 実装しました。 指定されたアセットの検索文字列の配列を返します。

ジョブのロケールパラメーターと、API 操作のロケールを設定するメカニズムを追加しました。 ロケール文字列は `<language_code>[-<country_code>]` 形式にする必要があります。 言語コードは、ISO-639 で指定されている小文字の 2 文字のコードで、オプションの国コードは、ISO-3166 で指定されている大文字の 2 文字のコードです。

API 操作のロケールを設定するためのオプションのロケールパラメーターを `authHeader` SOAP ヘッダーに追加しました。 このパラメーターが存在しない場合は、HTTP ヘッダー `Accept-Language` が使用されます。 このヘッダーも存在しない場合、IPS サーバーのデフォルトのロケールが使用されます。

厳密に型指定されたメタデータフィールドの get/set サポートを追加しました。

gzip 応答制御のためのSOAPおよび HTTP ヘッダーのサポートを実装しました。

`gzipResponse` に `authHeader` フラグを追加しました。 存在しない場合、API は HTTP `Accept-Encoding` ヘッダーを確認します。

厳密に型指定されたメタデータフィールド条件の searchAssets のサポートを追加しました。

* すべてのフィールドタイプで、値は文字列比較演算子（`Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`）で渡すことができます
* ブール値フィールドの場合、`boolVal` は `Equals` の op で渡すことができます。
* Int フィールドの場合、`longVal` は数値比較演算子（`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`）で渡され、`minLong/maxLong` は数値範囲演算子（`Between, NotBetween`）で渡されます。
* Float フィールドの場合、`doubleVal` は数値比較演算子（`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`）で渡され、`minDouble/maxDouble` は数値範囲演算子（`Between, NotBetween`）で渡されます。
* 日付フィールドの場合、数値比較演算子（`dateVal`）を使用して `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals` を渡すか、数値範囲演算子（`Between, NotBetween`）を使用して minDate/maxDate を渡すことができます。

説明、`jobSubType`、`originalJobName` の各フィールドを `JobLog` タイプに追加しました。

* `originalJobName` は、`submitJob` に送信されるジョブ名です（一意性サフィックスまたは後続のジョブ名はありません）。
* `jobSubType` は、`ImageServingPublishJob` ジョブ（`full`、`increment, fullwithsearch,`、`fulloverride` のいずれか）でのみ使用されます。
* `description` は、すべてのジョブタイプで空の文字列ですが、最終的にはアップロードパスなどの概要ジョブ情報が含まれます。

さらに、次のフィールドは `getJobLogs` と `getJobLogDetails` の両方に含まれていません。 以前のバージョンでは、`getJobLogDetails` でのみ使用できました。

* `endDate` （ジョブが完了した場合）。
* `fileDuplicateCount` （以前は常に `0` と `getJobLogs` っていました）
* `fileUpdateCount` （以前は常に `0` と `getJobLogs` 合され、`fileSuccessCount` に含まれていましたが、現在は別々のフィールドに分割されています）。

`JobLogDetail` タイプに assetHandle フィールドを追加しました。

`submitJob` にオプションの説明パラメーターを追加しました。 このパラメーターは、`getScheduledJobs`、`getActiveJobs`、`getJobLogs` で取得するために渡されます。

「SKU システム」フィールドを非推奨（廃止予定）にしました。 フィールドが `SystemFieldCondition` に `searchAssets` として渡された場合、このフィールドは無視されます。

`excludeAssetTypeArray` に `searchAssets` フィルターを追加しました。

`MaskInfo` タイプを `Asset` に追加しました。

IPS で管理する新しいアセットタイプを追加しました。

<table id="table_DCCE936B797A448598C30E3B344525A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>アセットタイプ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Illustrator </span> </p> </td> 
   <td colname="col2"> <p>Adobe Illustrator ファイル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>EPS ファイルとPostScript ファイル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>.doc で終わるファイルのMicrosoft® Word ドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>.xls で終わるファイルのMicrosoft® Excel ドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>.ppt で終わるファイルのMicrosoft® PowerPoint ドキュメント </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>.rtf で終わるアップロードされたファイルの RTF ファイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`UploadDirectoryJob` および `UploadUrlsJob` に、Postscript、Illustrator、PDFの各ファイルの処理を個別に制御するオプションを追加しました。 既存のすべてのジョブは、3 つの処理パイプラインのそれぞれに必要なパラメーターを提供するので、現在どおりに正確に機能します。 元の `PostScriptOptions` ブロックは、IllustratorおよびEPS/PS ファイルの処理を設定するために使用されます。 オプションで、特定のファイルオプションブロックを指定して、処理を指定できます。 変更のリストには、次が含まれます。

<table id="table_D4E5ACCB2D144D05A5FA0129AA5F9344"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>フィールド </p> </th> 
   <th colname="col2" class="entry"> <p>パラメータ </p> </th> 
   <th colname="col3" class="entry"> <p>値 </p> </th> 
   <th colname="col4" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p> <span class="codeph"> [!DNL PostScriptOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL process] </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> None </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> ラスタライズ </span> （デフォルト） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>アセットを管理するだけです。アップロード時に派生画像を作成しません。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>EPSおよびPostScript ファイルを所定の解像度とカラースペースで画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>オプション。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>ファイルを画像にラスタライズするときに有効になります。 元のファイルがロゴのオーバーレイ用にこのように定義されている場合、透明な背景が作成されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> None </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rasterize </span> （デフォルト） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>アセットを管理するだけです。アップロード時に派生画像を作成しません。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>ファイルを所定の解像度とカラースペースでイメージにレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>ラスタライズの解像度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>レンダリングのターゲットカラースペース。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>オプション。 </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>ファイルを画像にラスタライズするときに有効になります。 元のファイルがロゴのオーバーレイを作成する方法で定義されている場合、透明な背景を作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> None </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rasterize </span> （デフォルト） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>アセットを管理するだけです。アップロード時に派生画像を作成しません。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>ファイルを所定の解像度とカラースペースでイメージにレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>ラスタライズの解像度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>レンダリングのターゲットカラースペース。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>レンダリング後に複数ページのPDFを eCatalog に組み合わせるかどうかを定義します（デフォルトは true）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>後で検索サーバーに提供するために、PDFの単語を DB に抽出するかどうかを定義します（デフォルトは false）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`getScheduledJobs` からクエリすることもできます。

`webservice.gzip.response` 設定プロパティを変更して、次のいずれかの値を取るようになりました。

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>値 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL never] </span> </p> </td> 
   <td colname="col2"> <p>応答を gzip 形式で圧縮しないでください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponse が true の場合にのみ gzip 応答を返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>Gzip :authHeader/gzipResponse が true の場合、または gzipResponse ヘッダーが存在せず、HTTP Accept-Encoding ヘッダーに gzip が含まれている場合。 （デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>ヘッダー値に関係なく、常に gzip 応答。 この値はデバッグ目的でのみ使用してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>
