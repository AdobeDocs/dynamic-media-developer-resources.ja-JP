---
title: 新規追加と変更
description: IPS API v4.0 の新しい変更と実装された変更について説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 2%

---

# 新規追加と変更{#new-additions-and-changes}

IPS API v4.0 の新しい変更と実装された変更について説明します。

異なる WSDL とスキーマ名前空間を使用して、API バージョンを並べて実装しました。

* 以前の API バージョン： `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0 バージョン： `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

追加済み `PostScriptOptions/alpha` フィールドに入力します。

追加済み `VideoRootUrl` および `SwfRootUrl` プロパティ `getProperty` 操作。

オプションの追加 `appName` および `appVersion` パラメーター `authHeader` 呼び出し元のアプリケーションを追跡する。 にログを追加しました `ipsApiService.log`.

オプションの `serviceUrl` パラメーターを WSDL 生成サーブレットに渡します。 このパラメーターは、デバッグプロキシに役立ちます。 例：`http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

実装済み `getZipEntries` 操作。

システムフィールド条件の検索範囲および入力された比較値を実装しました。

追加済み `'Asset'` 主にアセット間メタデータフィールドを許可するための、アセットタイプの文字列定数。

実装済み `trashState` パラメーター `searchAssets`.

実装済み `getAssetPublishHistory` 操作。

オプションの追加 `faultHttpStatusCode` Flexで障害処理を有効にする SOAP ヘッダー。 Flexの場合は、 `<faultHttpStatusCode>200</faultHttpStatusCode>`. 障害応答のデフォルトのステータスコードは次のとおりです。 `500 (Internal Server Error)`.

ごみ箱からアセットを復元する操作と、ごみ箱からアセットを空にする操作を追加しました。

CRUD 操作を実装しました。

有効フラグを `ImageMap` 入力と `saveImageMap` 操作。

残りのファイルの最適化ジョブのサポートが追加されました。

追加済み `setAssetsPublishState` 一括公開状態の更新の場合。

追加済み `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

非推奨 `saveMetadataField` 新たな手術に有利な `createMetadataField` および `updateMetadataField` 操作。

実装済み `deleteAssetsParam` バッチ削除操作。

実装済み `moveAssetsParam` バッチ移動操作。

実装済み `deleteMetadataField` 操作。

実装済み `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` 操作。

実装済み `getAssetCounts`.

サポートを `setImageSetMembers` 含む `RenderSet` メンバー `ImageSet` アセット。

追加済み `replaceImage` 操作。

追加済み `copyImage` 操作。

追加済み `setUrlModifier` 操作と `urlModifier/urlPostApplyModifier` フィールド `LayerViewInfo`, `TemplateInfo`、および `WatermarkInfo`.

追加済み `createDerivedAsset` 操作。 現在、 `ownerHandle` は画像アセットを参照し、タイプは `AdjustedView` または `LayerView`.

追加済み `createTemplate` 操作。 を呼び出して、テンプレートまたは透かしアセットを作成します。

IPS 会社設定 `CompanySettings`を Web サービス API に移行しました。

追加済み `excludeByproducts` フラグをフィルター `searchAssets` 操作。 このフラグを true に設定すると、実行が実行されます `PSDlayer` 画像とPDFのリッピング画像。

追加済み `getGenerationInfo` 操作。

追加済み `SystemMessage` プロパティ名 `getProperty` 操作。

一部のアセットタイプ文字列定数を、対応する「 Asset Info 」フィールドに合わせて変更しました。

* WordDoc:Word
* ExcelDoc:Excel
* PowerPointDoc:PowerPoint
* RTFDoc:Rtf

成功、警告およびエラーを要約するために、バッチ操作の結果の形式を変更しました。

実装済み `batchSetAssetMetadata` バッチメタデータ操作。

アプリ固有のデータをサポートするようになりました。

のブール型フラグのサポートを実装しました。 `createTemplate`, `extendLayers`、および `extractText` Photoshop処理のプロセスを制御するためのアップロードジョブ（追加ファイルのアップロードの変更と同様）。

実装済み `setImageMaps` および `setZoomTargets` 操作。

実装済み `ViewerPreset` 操作。 次のタイプが認識されます。

* `VideoPlayer` （ビデオでは、これらのビューアのみが公開されています）。
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

ビューアスキンでは、次の 2 つのパラメータがサポートされています。 `skinFg` および `skinBg`. バックエンドコードは、後方互換性を維持するために必要なすべての処理を実行します。

実装済み `getAssociatedAssets` 操作。

追加済み `ReprocessAssets` ジョブタイプ：リッピングPDFの再処理や画像の再最適化を含む、以前にアップロードしたプライマリソースファイルの再処理を許可する場合。

名前を変更 `PropertySetType` フィールドタイプ： `propertyType`. 名前の変更は `createPropertySetType` パラメーターと `getPropertySetType/getPropertySetTypes` 応答。

実装済み `batchSetImageFields` 画像ユーザーデータおよびその他の編集可能な画像フィールドの設定をサポートする操作。

47 様々なアセット情報タイプに、 fileSize フィールドを追加しました。

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

実装済み `getActivePublishContexts` 操作。 この操作は、指定した会社のアクティブな公開サーバーを持つ公開コンテキスト名の配列を返します。 現在の公開コンテキスト名は次のとおりです。

* `ImageServing`
* `ImageRendering`
* `Video`

実装済み `getSearchStrings` 操作。 指定されたアセットの検索文字列の配列を返します。

ジョブのロケールパラメーターと、API 操作のロケールを設定するメカニズムを追加しました。 ロケール文字列は `<language_code>[-<country_code>]`. 言語コードは、ISO-639 で指定された小文字の 2 文字のコードで、オプションの国コードは、ISO-3166 で指定された大文字の 2 文字のコードです。

オプションのロケールパラメーターを `authHeader` API 操作のロケールを設定する SOAP ヘッダー。 このパラメーターがない場合、HTTP ヘッダー `Accept-Language` が使用されます。 このヘッダーも存在しない場合は、IPS サーバのデフォルトのロケールが使用されます。

厳密に型指定されたメタデータフィールドに対する get/set のサポートを追加しました。

gzip 応答制御に SOAP および HTTP ヘッダーのサポートを実装しました。

追加済み `gzipResponse` フラグ設定 `authHeader`. 存在しない場合、API は HTTP を確認します `Accept-Encoding` ヘッダー。

厳密に型指定されたメタデータフィールド条件に対する searchAssets のサポートを追加しました。

* すべてのフィールドタイプに対して、値は文字列比較演算子 ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* ブール値フィールドの場合、 `boolVal` は、 `Equals` op.
* Int フィールドの場合、 `longVal` は数値比較演算子 ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) または `minLong/maxLong` は数値範囲演算 ( `Between, NotBetween`) をクリックします。
* フロートフィールドの場合、 `doubleVal` は数値比較演算子 ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) または `minDouble/maxDouble` は数値範囲演算 ( `Between, NotBetween`) をクリックします。
* 日付フィールドの場合、 `dateVal` と数値比較演算子 ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) を渡すか、数値範囲演算 ( `Between, NotBetween`) をクリックします。

説明を追加しました。 `jobSubType`、および `originalJobName` フィールド `JobLog` タイプ。

* `originalJobName` は、次に送信されたジョブ名です： `submitJob` （一意性のサフィックスや後続のジョブ名を含まない）。
* `jobSubType` が次の場合にのみ使用されます： `ImageServingPublishJob` ジョブ ( ここで、 `full`, `increment, fullwithsearch,` または `fulloverride`) をクリックします。
* `description` はすべてのジョブタイプに対して空の文字列ですが、最終的には、アップロードパスなどの概要ジョブ情報が含まれます。

また、次のフィールドは、 `getJobLogs` および `getJobLogDetails`. 以前のバージョンでは、でのみ使用できました。 `getJobLogDetails`.

* `endDate` （ジョブが完了した場合）。
* `fileDuplicateCount` ( 以前は `0` と `getJobLogs`)
* `fileUpdateCount` ( 以前は `0` と `getJobLogs` およびに含まれる `fileSuccessCount`;現在は、別々のフィールドに分割されます )。

assetHandle フィールドを `JobLogDetail` タイプ。

オプションの説明パラメーターをに追加しました。 `submitJob`. このパラメーターは、で取得するために渡されます。 `getScheduledJobs`, `getActiveJobs`、および `getJobLogs`.

「 SKU システム」フィールドが非推奨となりました。 フィールドが `SystemFieldCondition` から `searchAssets`.

追加済み `excludeAssetTypeArray` フィルター `searchAssets`.

追加済み `MaskInfo` 入力 `Asset`.

IPS による管理用の新しいアセットタイプを追加しました。

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
   <td colname="col2"> <p>Adobe Illustratorファイル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>EPSファイルと PostScript ファイル </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® .doc で終わるファイルの Word ドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® .xls で終わるファイルに関する Excel ドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>.ppt で終わるファイルのMicrosoft® PowerPoint ドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>.rtf で終わるファイルの RTF ファイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

次の追加オプションが追加されました： `UploadDirectoryJob` および `UploadUrlsJob` PostScript ファイル、Illustratorファイル、PDFファイルの処理を個別に制御する。 既存のすべてのジョブは、3 つの処理パイプラインのそれぞれに必要なパラメーターを提供し、現在のとおりに機能するようにします。 オリジナル `PostScriptOptions` ブロックは、IllustratorファイルとEPS/PS ファイルの処理を設定するために使用されます。 必要に応じて、処理を指定するために、特定のファイルオプションブロックを指定できます。 変更のリストには、以下が含まれます。

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
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> なし </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> ラスタライズ </span>（デフォルト） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>アセットの管理のみを行い、アップロード時に派生アセットを作成しないでください。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>EPSと PostScript ファイルを、所定の解像度とカラースペースで画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>（オプション） </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;ブール&gt; </span> </p> </td> 
   <td colname="col4"> <p>ファイルを画像にラスタライズするときに有効になります。 元のファイルがこの方法でロゴのオーバーレイに定義されている場合、透明な背景が作成されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> プロセス </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> なし </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> ラスタライズ </span> （デフォルト） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>アセットの管理のみを行い、アップロード時に派生アセットを作成しないでください。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>ファイルを所定の解像度とカラースペースで画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;整数&gt; </span> </p> </td> 
   <td colname="col4"> <p>解像度をラスタライズする。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>レンダリング用のターゲットカラースペース。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> アルファ </span> </p> <p>（オプション） </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>ファイルを画像にラスタライズするときに有効になります。 元のファイルがこの方法で定義されている場合、オーバーレイロゴを作成する際に透明な背景を作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> プロセス </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> なし </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> ラスタライズ </span> （デフォルト） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>アセットの管理のみを行い、アップロード時に派生アセットを作成しないでください。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>ファイルを所定の解像度とカラースペースで画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;整数&gt; </span> </p> </td> 
   <td colname="col4"> <p>解像度をラスタライズする。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>レンダリング用のターゲットカラースペース。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;ブール&gt; </span> </p> </td> 
   <td colname="col4"> <p>レンダリング後に、複数のページPDFを eCatalog に組み合わせるかどうかを定義します（デフォルトは true）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;ブール&gt; </span> </p> </td> 
   <td colname="col4"> <p>後で検索サーバーに提供するために、PDFからの単語を DB に抽出するかどうかを定義します（デフォルトは false）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

また、 `getScheduledJobs`.

変更された `webservice.gzip.response` 設定プロパティで次のいずれかの値を取得します。

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
   <td colname="col2"> <p>応答を gzip で圧縮しないでください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponse が true の場合のみ、Gzip 応答。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponse が true の場合は Gzip。それ以外の場合、gzipResponse ヘッダーが存在せず、HTTP Accept-Encoding ヘッダーに gzip が含まれている場合は Gzip。 (初期設定). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>ヘッダー値に関係なく、常に gzip 応答です。 この値は、デバッグ目的でのみ使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>
