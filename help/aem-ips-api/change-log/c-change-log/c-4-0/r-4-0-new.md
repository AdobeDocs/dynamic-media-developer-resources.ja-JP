---
description: IPS API v4.0の新しい変更と実装された変更について説明します。
seo-description: IPS API v4.0の新しい変更と実装された変更について説明します。
seo-title: 新しい追加と変更
solution: Experience Manager
title: 新しい追加と変更
topic: Scene7 Image Production System API
uuid: ca4bbe36-c1b7-471f-90a8-6b695d56ac7a
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '1234'
ht-degree: 2%

---


# 新しい追加と変更{#new-additions-and-changes}

IPS API v4.0の新しい変更と実装された変更について説明します。

WSDLとスキーマの名前空間が別々に用意された、並べておけるAPIバージョンを実装。

* 以前のAPIバージョン：`IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0バージョン：`IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

`PostScriptOptions/alpha`フィールドを追加しました。

`getProperty`操作に`VideoRootUrl`および`SwfRootUrl`プロパティを追加しました。

呼び出し元のアプリケーションを追跡するために、オプションの`appName`パラメーターと`appVersion`パラメーターを`authHeader`に追加しました。 `ipsApiService.log`にログを追加しました。

オプションの`serviceUrl`パラメーターがWSDL生成サーブレットに追加されました。 これは、デバッグプロキシに特に便利です。 例：`http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

`getZipEntries`操作を実装しました。

システムフィールド条件に対して検索範囲と入力された比較値を実装。

主にアセット間のメタデータフィールドを許可するために、`'Asset'`アセットタイプの文字列定数を追加しました。

`searchAssets`に`trashState`パラメーターを実装しました。

`getAssetPublishHistory`操作を実装しました。

オプションの`faultHttpStatusCode` SOAPヘッダを追加し、Flexでの障害処理を有効にしました。 Flexの場合は、`<faultHttpStatusCode>200</faultHttpStatusCode>`を使用します。 フォルト応答のデフォルトのステータスコードは`500 (Internal Server Error)`です。

ごみ箱からアセットを復元し、ごみ箱からアセットを空にする操作を追加しました。

CRUD操作を実装しました。

有効なフラグを`ImageMap`型と`saveImageMap`操作に追加しました。

残りのファイルを最適化ジョブのサポートを追加しました。

一括発行状態の更新のために`setAssetsPublishState`を追加しました。

`ImageServingPublishSettings`、`getImageServingPublishSettings`、`setImageServingPublishSettings`を追加しました。

`saveMetadataField`操作が廃止され、新しい`createMetadataField`操作と`updateMetadataField`操作が使用されるようになりました。

`deleteAssetsParam`バッチ削除操作を実装しました。

`moveAssetsParam`バッチ移動操作を実装しました。

`deleteMetadataField`操作を実装しました。

`get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat`操作を実装。

`getAssetCounts`を実装。

`setImageSetMembers`に、`ImageSet`アセットに`RenderSet`メンバーを含めるサポートを追加しました。

`replaceImage`操作を追加しました。

`copyImage`操作を追加しました。

`LayerViewInfo`、`TemplateInfo`、`WatermarkInfo`に`setUrlModifier`演算と`urlModifier/urlPostApplyModifier`フィールドを追加しました。

`createDerivedAsset`操作を追加しました。 現在、`ownerHandle`は画像アセットを参照する必要があり、タイプは`AdjustedView`または`LayerView`です。

`createTemplate`操作を追加しました。 現在、このメソッドを呼び出して、テンプレートアセットまたは透かしアセットを作成できます。

IPS会社設定`CompanySettings`、WebサービスAPIに移植されます。

`excludeByproducts`フィルターフラグを`searchAssets`操作に追加しました。 このフラグをtrueに設定すると、`PSDlayer`画像とPDFのリップ画像が実行されます。

`getGenerationInfo`操作を追加しました。

`SystemMessage`プロパティ名を`getProperty`操作に追加しました。

アセットタイプ文字列定数の一部を、対応するアセット情報フィールドに一致するように変更しました。

* WordDoc:Word
* ExcelDoc:Excel
* PowerPointDoc:PowerPoint
* RTFDoc:Rtf

成功、警告およびエラーを要約するために、バッチ操作の結果の形式を変更しました。

`batchSetAssetMetadata`バッチメタデータ操作を実装しました。

アプリ固有のデータのサポートを実装しました。

`createTemplate`、`extendLayers`、`extractText`のブール型フラグのサポートを実装し、Photoshop処理の処理を制御します（追加ファイルのアップロードの変更と同様）。

`setImageMaps`操作と`setZoomTargets`操作を実装しました。

`ViewerPreset`操作を実装しました。 認識される型は次のとおりです。

* `VideoPlayer` （ビデオはこれらのビューアのみを公開します）。
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

ビューアのスキンでは、次の2つのパラメータがサポートされています。`skinFg`と`skinBg`。 バックエンドコードは、下位互換性を維持するために必要なすべての処理を行います。

`getAssociatedAssets`操作を実装しました。

PDFのリッピングや画像の再最適化など、以前にアップロードしたプライマリソースファイルの再処理を許可する`ReprocessAssets`ジョブタイプが追加されました。

`PropertySetType`フィールドタイプの名前を`propertyType`に変更しました。 これは`createPropertySetType`パラメーターと`getPropertySetType/getPropertySetTypes`応答に影響します。

`batchSetImageFields`操作を導入し、画像ユーザーデータおよびその他の編集可能な画像フィールドの設定をサポートしました。

47様々なアセット情報タイプにfileSizeフィールドを追加しました。

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

`getActivePublishContexts`操作を実装しました。 この操作は、指定された会社のアクティブなパブリッシュサーバを持つパブリッシュコンテキスト名の配列を返します。 現在のパブリッシュコンテキスト名は次のとおりです。

* `ImageServing`
* `ImageRendering`
* `Video`

`getSearchStrings`操作を実装しました。 渡されたアセットの検索文字列の配列を返します。

ジョブのロケールパラメーターと、API操作のロケールを設定するメカニズムを追加しました。 ロケール文字列は`<language_code>[-<country_code>]`の形式にする必要があります。 言語コードは、ISO-639で指定された小文字の2文字のコードで、オプションの国コードは、ISO-3166で指定された大文字の2文字のコードです。

API操作のロケールを設定するために、`authHeader` SOAPヘッダーにオプションのロケールパラメーターを追加しました。 このパラメーターが存在しない場合は、HTTPヘッダー`Accept-Language`が使用されます。 このヘッダも存在しない場合は、IPSサーバの既定のロケールが使用されます。

厳密に型指定されたメタデータフィールドの取得/設定のサポートを追加しました。

gzip応答制御用にSOAPおよびHTTPヘッダーのサポートを実装。

`gzipResponse`フラグを`authHeader`に追加しました。 存在しない場合は、APIはHTTP `Accept-Encoding`ヘッダもチェックします。

searchAssetsで、厳密に型指定されたメタデータフィールドの条件のサポートが追加されました。

* すべてのフィールドタイプに対して、文字列比較演算子(`Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)を使用して値を渡すことができます。
* ブール型フィールドの場合は、`boolVal`を`Equals`操作と共に渡すことができます。
* Intフィールドの場合、`longVal`は数値比較演算子(`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)で渡すことも、`minLong/maxLong`は数値範囲演算(`Between, NotBetween`)で渡すこともできます。
* 浮動小数点数フィールドの場合、`doubleVal`は数値比較演算子(`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)で渡すか、`minDouble/maxDouble`は数値範囲演算(`Between, NotBetween`)で渡すことができます。
* 日付フィールドでは、`dateVal`を数値比較演算子(`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)で渡すか、minDate/maxDateを数値範囲演算(`Between, NotBetween`)で渡すことができます。

`JobLog`型に説明、`jobSubType`、`originalJobName`フィールドを追加しました。

* `originalJobName` は、に送信されるジョブ名 `submitJob` です（一意のサフィックスやフォローオンジョブ名は含まれません）。
* `jobSubType` は、現在、 `ImageServingPublishJob` ジョブ（またはのいずれかである）でのみ使用され `full`ています `increment, fullwithsearch,`  `fulloverride`。
* `description` は、現在、すべてのジョブタイプに対して空の文字列ですが、最終的には、アップロードパスなどの概要ジョブ情報が含まれます。

さらに、次のフィールドは`getJobLogs`と`getJobLogDetails`の両方に含まれていません。 以前のバージョンでは、`getJobLogDetails`でのみ利用可能でした。

* `endDate` （ジョブが完了している場合）。
* `fileDuplicateCount` (以前は常に次 `0` と一緒でした `getJobLogs`)
* `fileUpdateCount` (以前は、常ににに含ま `0` れ `getJobLogs` ていました `fileSuccessCount`。現在は、別々のフィールドに分割されています)。

assetHandleフィールドを`JobLogDetail`タイプに追加しました。

オプションで`submitJob`に説明パラメーターを追加しました。 これは`getScheduledJobs`、`getActiveJobs`、`getJobLogs`での取得のために渡されます。

「SKUシステム」フィールドが非推奨となりました。 フィールドを`SystemFieldCondition`として`searchAssets`に渡すと、無視されます。

`excludeAssetTypeArray`フィルターを`searchAssets`に追加しました。

`MaskInfo`型を`Asset`に追加しました。

IPSによる管理用に、新しいアセットタイプを追加しました。

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
   <td colname="col1"> <p> <span class="codeph"> WordDoc  </span> </p> </td> 
   <td colname="col2"> <p>.docで終わるファイルのMicrosoft Wordドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc  </span> </p> </td> 
   <td colname="col2"> <p>.xlsで終わるファイルのMicrosoft Excelドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc  </span> </p> </td> 
   <td colname="col2"> <p>.pptで終わるファイルのMicrosoft PowerPointドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc  </span> </p> </td> 
   <td colname="col2"> <p>.rtfで終わるファイルをアップロードする場合のRTFファイル </p> </td> 
  </tr> 
 </tbody> 
</table>

`UploadDirectoryJob`と`UploadUrlsJob`に、Postscript、Illustrator、PDFファイルの処理を個別に制御するオプションを追加しました。 既存のジョブは、3つの処理パイプラインのそれぞれに必要なパラメータを提供し、現在のジョブと同じように機能します。 元の`PostScriptOptions`ブロックは、IllustratorファイルとEPS/PSファイルの処理を設定するために使用されます。 オプションで、処理を指定するために特定のファイルオプションブロックを指定できます。 変更のリストには、次のものが含まれます。

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> プロセス </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> なし </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> ラスタライズ </span>（初期設定） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>アセットのみを管理し、アップロード時に派生物は作成しません。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>EPSファイルとPostScriptファイルを所定の解像度とカラースペースで画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>（オプション） </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;ブール&gt; </span> </p> </td> 
   <td colname="col4"> <p>ファイルを画像にラスタライズするときに有効になります。 元のファイルがこのように定義されている場合、ロゴのオーバーレイに対して透明な背景が作成されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> プロセス </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> なし </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> ラスタライズ </span> （初期設定） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>アセットのみを管理し、アップロード時に派生物は作成しません。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>指定された解像度とカラースペースでファイルを画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;整数&gt; </span> </p> </td> 
   <td colname="col4"> <p>解像度のラスタライズ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> カラースペース </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>レンダリング用のターゲットカラースペース。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha  </span> </p> <p>（オプション） </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>ファイルを画像にラスタライズするときに影響を受けます。 オーバーレイロゴを作成する際に元のファイルがこのように定義されている場合、透明な背景を作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> プロセス </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> なし </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> ラスタライズ </span> （初期設定） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>アセットのみを管理し、アップロード時に派生物は作成しません。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>指定された解像度とカラースペースでファイルを画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;整数&gt; </span> </p> </td> 
   <td colname="col4"> <p>解像度のラスタライズ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> カラースペース </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>レンダリング用のターゲットカラースペース。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;ブール&gt; </span> </p> </td> 
   <td colname="col4"> <p>レンダリング後に複数ページのPDFをeCatalogに結合するかどうかを定義します（初期設定はtrue）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;ブール&gt; </span> </p> </td> 
   <td colname="col4"> <p>後で検索サーバーに供給するために、PDFの単語をDBに抽出するかどうかを定義します（デフォルトはfalse）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`getScheduledJobs`からクエリすることもできます。

`webservice.gzip.response`設定プロパティが次のいずれかの値になるように変更されました。

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
   <td colname="col2"> <p>gzip応答を送信しない。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SOAP </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponseがtrueの場合のみ、Gzip応答が返されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 受��入れる </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponseがtrueの場合、またはgzipResponseヘッダが存在せず、HTTP Accept-Encodingヘッダにgzipが含まれている場合は、gzip。 (初期設定). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> いつも </span> </p> </td> 
   <td colname="col2"> <p>ヘッダーの値に関係なく、常にgzip応答です。 この値は、デバッグ目的でのみ使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

