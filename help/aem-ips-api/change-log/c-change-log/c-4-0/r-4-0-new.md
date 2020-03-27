---
description: IPS API v4.0の新しい変更と実装された変更について説明します。
seo-description: IPS API v4.0の新しい変更と実装された変更について説明します。
seo-title: 新しい追加と変更
solution: Experience Manager
title: 新しい追加と変更
topic: Scene7 Image Production System API
uuid: ca4bbe36-c1b7-471f-90a8-6b695d56ac7a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 新しい追加と変更{#new-additions-and-changes}

IPS API v4.0の新しい変更と実装された変更について説明します。

別々のWSDLとスキーマの名前空間を使用して、APIバージョンを並べて実装しました。

* 以前のAPIバージョン： `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0バージョン： `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

フィールドを `PostScriptOptions/alpha` 追加しました。

操作のプ `VideoRootUrl` ロパテ `SwfRootUrl` ィとを追加し `getProperty` ました。

呼び出し元のアプリケ `appName` ーションを追 `appVersion` 跡するためのオプ `authHeader` ションとパラメーターを追加しました。 にログを追加しまし `ipsApiService.log`た。

WSDL生成サーブレット `serviceUrl` にオプションのパラメーターを追加しました。 これは、プロキシのデバッグに特に便利です。 例：`http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

操作を実装 `getZipEntries` しました。

システムフィールドの条件に対して、検索範囲と入力された比較値を実装しました。

主にアセ `'Asset'` ット間のメタデータフィールドを許可するために、アセットタイプの文字列定数を追加しました。

のパラメ `trashState` ータを実装し `searchAssets`た。

操作を実装 `getAssetPublishHistory` しました。

Flexでの障害処理を有効にする `faultHttpStatusCode` ためのオプションのSOAPヘッダーを追加しました。 Flexの場合は、を使用しま `<faultHttpStatusCode>200</faultHttpStatusCode>`す。 障害応答のデフォルトのステータスコードはで `500 (Internal Server Error)`す。

ごみ箱からアセットを復元し、ごみ箱からアセットを空にする操作を追加しました。

CRUD操作を実装。

有効なフラグをタイプと操 `ImageMap` 作に追加し `saveImageMap` ました。

残りのファイルの最適化ジョブのサポートを追加しました。

一括公開 `setAssetsPublishState` 状態の更新を追加しました。

Added `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

新しい操 `saveMetadataField` 作および操作を優先して、非 `createMetadataField` 推奨の操 `updateMetadataField` 作です。

バッチ削 `deleteAssetsParam` 除操作を実装しました。

バッチ `moveAssetsParam` 移動操作を実装。

操作を実装 `deleteMetadataField` しました。

実装、 `get/setImageRenderingPublishSettings`操作を `get/set/create/updateVignettePublishFormat` 行います。

Implemented `getAssetCounts`.

メンバーをアセットに含め `setImageSetMembers` るためのサポ `RenderSet` ートをに追加 `ImageSet` しました。

操作を追加 `replaceImage` しました。

操作を追加 `copyImage` しました。

、およ `setUrlModifier` びの操作とフ `urlModifier/urlPostApplyModifier` ィール `LayerViewInfo`ドを追 `TemplateInfo`加しま `WatermarkInfo`した。

操作を追加 `createDerivedAsset` しました。 現在、は画 `ownerHandle` 像アセットを参照し、タイプはまたはのいずれかである必要が `AdjustedView` ありま `LayerView`す。

操作を追加 `createTemplate` しました。 現在は、このメソッドを呼び出して、テンプレートまたは透かしアセットを作成できます。

IPSの会社設定(Webサ `CompanySettings`ービスAPIに転送)。

操作にフ `excludeByproducts` ィルターフラグを追 `searchAssets` 加しました。 このフラグをtrueに設定すると、画像とPDFのリ `PSDlayer` ッピングされた画像が実行されます。

操作を追加 `getGenerationInfo` しました。

操作にプ `SystemMessage` ロパティ名を追加 `getProperty` しました。

一部のアセットタイプ文字列定数を、対応するアセット情報フィールドに一致するように変更しました。

* WordDoc:単語
* ExcelDoc:Excel
* PowerPointDoc:PowerPoint
* RTFDoc:Rtf

成功、警告およびエラーを要約するために、バッチ操作の結果の形式を変更しました。

バッチメタデ `batchSetAssetMetadata` ータ操作を実装しました。

アプリ固有のデータのサポートを実装しました。

Photoshop処理の処理を制御するための、、 `createTemplate`およびア `extendLayers``extractText` ップロードジョブのブールフラグのサポートを実装しました（ファイルの追加アップロードの変更と同様）。

実装およ `setImageMaps` び操 `setZoomTargets` 作です。

操作を実装 `ViewerPreset` しました。 次のタイプが認識されます。

* `VideoPlayer` （ビデオはこれらのビューアのみを公開します）。
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

ビューアのスキンでは、次の2つのパラメータがサポートされています。 `skinFg` と `skinBg`バックエンドコードは、下位互換性を維持するために必要なすべての処理を実行します。

操作を実装 `getAssociatedAssets` しました。

PDFの取り `ReprocessAssets` 込みや画像の再最適化など、以前にアップロードしたマスターファイルの再処理を可能にするジョブの種類を追加しました。

フィールドタ `PropertySetType` イプの名前をに変更しま `propertyType`した。 これは、パラメーターと `createPropertySetType` 応答に影響を与 `getPropertySetType/getPropertySetTypes` えます。

画像ユー `batchSetImageFields` ザデータおよびその他の編集可能な画像フィールドの設定をサポートする操作を実装しました。

47各種のアセット情報タイプにfileSizeフィールドを追加しました。

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

操作を実装 `getActivePublishContexts` しました。 この操作は、指定した会社のアクティブなパブリッシュサーバを持つパブリッシュコンテキスト名の配列を返します。 現在のパブリッシュコンテキスト名は次のとおりです。

* `ImageServing`
* `ImageRendering`
* `Video`

操作を実装 `getSearchStrings` しました。 指定されたアセットの検索文字列の配列を返します。

ジョブのロケールパラメーターと、API操作のロケールを設定するメカニズムを追加しました。 ロケール文字列は、次の形式で指定する必要がありま `<language_code>[-<country_code>]`す。 言語コードはISO-639で指定された小文字の2文字のコードで、オプションの国コードはISO-3166で指定された大文字の2文字のコードです。

API操作のロケールを設定するために、 `authHeader` SOAPヘッダーにオプションのロケールパラメーターを追加しました。 このパラメーターが存在しない場合は、HTTPヘッダーが `Accept-Language` 使用されます。 このヘッダも存在しない場合は、IPSサーバの既定のロケールが使用されます。

厳密に型指定されたメタデータフィールドの取得/設定のサポートを追加しました。

gzip応答制御用のSOAPおよびHTTPヘッダーのサポートを実装しました。

にフラグ `gzipResponse` を追加しまし `authHeader`た。 存在しない場合、APIはHTTPヘッダもチェックし `Accept-Encoding` ます。

厳密に型指定されたメタデータフィールドの条件に対するsearchAssetsのサポートを追加しました。

* すべてのフィールドタイプで、文字列比較演算子( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)を使用して値を渡すことができます
* ブール型フィールドの場 `boolVal` 合は、opと共に渡すことがで `Equals` きます。
* Intフィールドの場 `longVal` 合は、数値比較演算子( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)で渡すこ `minLong/maxLong` とも、数値範囲演算( `Between, NotBetween`)で渡すこともできます。
* 浮動小数点型フィールド `doubleVal` の場合、数値比較演算子( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)で渡すことも、 `minDouble/maxDouble` 数値範囲演算子( `Between, NotBetween`)で渡すこともできます。
* 日付フィールドの場合は、数値 `dateVal` 比較演算子( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)で渡すか、数値範囲演算( `Between, NotBetween`)でminDate/maxDateを渡すことができます。

タイプに説明、フ `jobSubType`ィールド `originalJobName` を追加し `JobLog` ました。

* `originalJobName` は、(一意の接尾辞や後続のジ `submitJob` ョブ名なしで)に送信されるジョブ名です。
* `jobSubType` は現在、ジョブ(またはの `ImageServingPublishJob` いずれか)でのみ使用さ `full`れて `increment, fullwithsearch,` いま `fulloverride`す。
* `description` は現在、すべてのジョブタイプに対して空の文字列ですが、最終的には、アップロードパスなどの概要ジョブ情報が含まれます。

また、次のフィールドはとの両方に含まれてい `getJobLogs` ませ `getJobLogDetails`ん。 以前のバージョンでは、でのみ使用できまし `getJobLogDetails`た。

* `endDate` （ジョブが完了している場合）。
* `fileDuplicateCount` (以前は常に `0` 使用 `getJobLogs`)
* `fileUpdateCount` (以前は常に、に含ま `0` れて `getJobLogs``fileSuccessCount`いましたが、現在は、別々のフィールドに分割されています)。

タイプにassetHandleフィールドを追加 `JobLogDetail` しました。

にオプションの説明パラメータを追加しま `submitJob`した。 これは、、およびでの取得のために `getScheduledJobs`渡さ `getActiveJobs`れます `getJobLogs`。

「SKUシステム」フィールドを非推奨にしました。 このフィールドは、にとして渡された場合は無視さ `SystemFieldCondition` れます `searchAssets`。

にフィルタ `excludeAssetTypeArray` ーを追加しま `searchAssets`した。

にタイプ `MaskInfo` を追加しまし `Asset`た。

IPSによる管理用の新しいアセットタイプを追加しました。

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
   <td colname="col2"> <p>EPSファイルとPostScriptファイル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>.docで終わるファイルのMicrosoft Wordドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>.xlsで終わるファイルのMicrosoft Excelドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>.pptで終わるファイルのMicrosoft PowerPointドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>.rtfで終わるファイルのRTFファイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

Postscript、IllustratorおよびPDFファ `UploadDirectoryJob` イルの処 `UploadUrlsJob` 理を個別に制御するためのオプションが追加されました。 既存のジョブは、現在のとおりに機能するように、3つの処理パイプラインのそれぞれに必要なパラメータを提供します。 元のブロッ `PostScriptOptions` クは、IllustratorおよびEPS/PSファイルの処理の設定に使用されます。 オプションで、処理を指定する特定のファイルオプションブロックを指定できます。 変更のリストには、次のものが含まれます。

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> プロセス </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> なし </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> ラスタラ </span>イズ（初期設定） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>アセットの管理のみを行い、アップロード時に派生物を作成しないでください。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>EPSファイルとPostScriptファイルを、指定された解像度とカラースペースで画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>（オプション） </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;ブール&gt; </span> </p> </td> 
   <td colname="col4"> <p>ファイルを画像にラスタライズするときに有効になります。 ロゴを重ねる際に元のファイルがこのように定義されている場合は、透明な背景が作成されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> プロセス </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> なし </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> ラスタラ </span> イズ（初期設定） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>アセットの管理のみを行い、アップロード時に派生物を作成しないでください。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>指定した解像度とカラースペースでファイルを画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 解像度 </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;整数&gt; </span> </p> </td> 
   <td colname="col4"> <p>解像度のラスタライズ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> カラースペース </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>レンダリングのターゲットカラースペース。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>（オプション） </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>ファイルを画像にラスタライズする際に有効になります。 オーバーレイロゴを作成する際に、元のファイルがこの方法で定義されている場合、透明な背景を作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> プロセス </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> なし </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> ラスタラ </span> イズ（初期設定） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>アセットの管理のみを行い、アップロード時に派生物を作成しないでください。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>指定した解像度とカラースペースでファイルを画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 解像度 </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;整数&gt; </span> </p> </td> 
   <td colname="col4"> <p>解像度のラスタライズ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> カラースペース </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>レンダリングのターゲットカラースペース。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;ブール&gt; </span> </p> </td> 
   <td colname="col4"> <p>レンダリング後に複数のページのPDFをeCatalogに結合するかどうかを定義します（初期設定はtrue）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;ブール&gt; </span> </p> </td> 
   <td colname="col4"> <p>PDFの単語をDBに抽出して、後で検索サーバーに提供するかどうかを定義します（デフォルトはfalse）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

また、からクエリを実行することもできま `getScheduledJobs`す。

次のいずれかの `webservice.gzip.response` 値を取るように設定プロパティを変更しました。

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>値 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 決してない </span> </p> </td> 
   <td colname="col2"> <p>応答をgzipで送信しない。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SOAP </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponseがtrueの場合のみ、Gzip応答が返されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 受��入れる </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponseがtrueの場合、またはgzipResponseヘッダーが存在せず、HTTP Accept-Encodingヘッダーにgzipが含まれている場合は、Gzip。 (初期設定). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> いつも </span> </p> </td> 
   <td colname="col2"> <p>ヘッダー値に関係なく、常にgzip応答です。 この値は、デバッグ目的でのみ使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

