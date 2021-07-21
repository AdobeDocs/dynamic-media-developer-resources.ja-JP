---
description: IPS API v4.0の新しい変更と実装された変更について説明します。
solution: Experience Manager
title: 新しい追加と変更
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '1225'
ht-degree: 2%

---

# 新しい追加と変更{#new-additions-and-changes}

IPS API v4.0の新しい変更と実装された変更について説明します。

APIバージョンを並べて実装し、WSDLとスキーマの名前空間を個別に実装しました。

* 以前のAPIバージョン：`IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0バージョン：`IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

`PostScriptOptions/alpha`フィールドを追加しました。

`getProperty`操作の`VideoRootUrl`および`SwfRootUrl`プロパティを追加しました。

呼び出し元のアプリケーションを追跡するために、オプションの`appName`パラメーターと`appVersion`パラメーターを`authHeader`に追加しました。 `ipsApiService.log`にログを追加しました。

オプションの`serviceUrl`パラメーターがWSDL生成サーブレットに追加されました。 これは、デバッグプロキシに特に役立ちます。 例：`http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

`getZipEntries`操作を実装しました。

システムフィールド条件に検索範囲と型指定比較値を実装しました。

主にクロスアセットメタデータフィールドを許可するために、アセットタイプの文字列定数`'Asset'`を追加しました。

`searchAssets`に`trashState`パラメーターを実装しました。

`getAssetPublishHistory`操作を実装しました。

Flexでの障害処理を有効にするため、オプションの`faultHttpStatusCode` SOAPヘッダーを追加しました。 Flexの場合は、`<faultHttpStatusCode>200</faultHttpStatusCode>`を使用します。 障害応答のデフォルトのステータスコードは`500 (Internal Server Error)`です。

ごみ箱からアセットを復元し、ごみ箱からアセットを空にする操作を追加しました。

CRUD操作を実装しました。

`ImageMap`型と`saveImageMap`操作にenabledフラグを追加しました。

残りのファイルを最適化ジョブのサポートを追加しました。

一括公開状態更新のために`setAssetsPublishState`を追加しました。

`ImageServingPublishSettings`、`getImageServingPublishSettings`、`setImageServingPublishSettings`を追加しました。

新しい`createMetadataField`操作と`updateMetadataField`操作に代わって、`saveMetadataField`操作が廃止されました。

`deleteAssetsParam`バッチ削除操作を実装しました。

`moveAssetsParam`バッチ移動操作を実装しました。

`deleteMetadataField`操作を実装しました。

`get/setImageRenderingPublishSettings`、`get/set/create/updateVignettePublishFormat`操作を実装。

`getAssetCounts`を実装。

`setImageSetMembers`に、`ImageSet`アセットに`RenderSet`メンバーを含めるサポートを追加しました。

`replaceImage`操作を追加しました。

`copyImage`操作を追加しました。

`LayerViewInfo`、`TemplateInfo`および`WatermarkInfo`の`setUrlModifier`操作と`urlModifier/urlPostApplyModifier`フィールドを追加しました。

`createDerivedAsset`操作を追加しました。 現在、`ownerHandle`は画像アセットを参照し、タイプは`AdjustedView`または`LayerView`にする必要があります。

`createTemplate`操作を追加しました。 現在は、これを呼び出して、テンプレートアセットまたは透かしアセットを作成できます。

IPS会社の設定`CompanySettings`をWebサービスAPIに移植。

`excludeByproducts`フィルターフラグを`searchAssets`操作に追加しました。 このフラグをtrueに設定すると、画像とPDFの切り取られた画像が実行されます。`PSDlayer`

`getGenerationInfo`操作を追加しました。

`SystemMessage`プロパティ名を`getProperty`操作に追加しました。

一部のアセットタイプ文字列定数を変更し、対応するAsset Infoフィールドに一致するようにしました。

* WordDoc:Word
* ExcelDoc:Excel
* PowerPointDoc:PowerPoint
* RTFDoc:Rtf

成功、警告およびエラーを要約するために、バッチ操作の結果の形式を変更しました。

`batchSetAssetMetadata`バッチメタデータ操作を実装しました。

アプリ固有のデータのサポートを実装。

Photoshop処理のプロセスを制御するためのアップロードジョブの`createTemplate`、`extendLayers`および`extractText`のブール型フラグのサポートを実装しました（追加ファイルのアップロードの変更と同様）。

`setImageMaps`操作と`setZoomTargets`操作を実装。

`ViewerPreset`操作を実装しました。 次のタイプが認識されます。

* `VideoPlayer` （ビデオでは、これらのビューアのみを公開しています）。
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

ビューアスキンでは、次の2つのパラメータがサポートされています。`skinFg`と`skinBg`が表示されます。 バックエンドコードは、後方互換性を維持するために必要なすべての処理を実行します。

`getAssociatedAssets`操作を実装しました。

PDFの取り込みや画像の再最適化を含む、以前にアップロードしたプライマリソースファイルの再処理を許可する`ReprocessAssets`ジョブタイプが追加されました。

`PropertySetType`フィールドタイプの名前を`propertyType`に変更しました。 これは`createPropertySetType`パラメーターと`getPropertySetType/getPropertySetTypes`応答に影響します。

画像ユーザーデータやその他の編集可能な画像フィールドの設定をサポートするために、 `batchSetImageFields`操作を実装しました。

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

`getActivePublishContexts`操作を実装しました。 この操作は、指定した会社のアクティブなパブリッシュサーバーを持つパブリッシュコンテキスト名の配列を返します。 現在のパブリッシュコンテキスト名は次のとおりです。

* `ImageServing`
* `ImageRendering`
* `Video`

`getSearchStrings`操作を実装しました。 指定されたアセットの検索文字列の配列を返します。

ジョブのロケールパラメーターと、API操作のロケールを設定するメカニズムを追加しました。 ロケール文字列は`<language_code>[-<country_code>]`の形式にする必要があります。 言語コードは、ISO-639で指定された小文字の2文字のコードで、オプションの国コードは、ISO-3166で指定された大文字の2文字のコードです。

API操作のロケールを設定するために、オプションのロケールパラメーターを`authHeader` SOAPヘッダーに追加しました。 このパラメーターがない場合は、HTTPヘッダー`Accept-Language`が使用されます。 このヘッダーも存在しない場合は、IPSサーバのデフォルトロケールが使用されます。

厳密に型指定されたメタデータフィールドに対するget/setのサポートを追加しました。

gzip応答制御用にSOAPおよびHTTPヘッダーのサポートを実装しました。

`gzipResponse`フラグを`authHeader`に追加しました。 存在しない場合、APIはHTTP `Accept-Encoding`ヘッダーも確認します。

厳密に型指定されたメタデータフィールド条件に対するsearchAssetsのサポートを追加しました。

* すべてのフィールドタイプに対して、文字列比較演算子(`Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)を使用して値を渡すことができます。
* ブール値フィールドの場合、`boolVal`は`Equals`演算子と共に渡すことができます。
* Intフィールドの場合、`longVal`は数値比較演算子(`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)で渡すことも、`minLong/maxLong`は数値範囲演算(`Between, NotBetween`)で渡すこともできます。
* Floatフィールドの場合、`doubleVal`は数値比較演算子(`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)で渡すことも、`minDouble/maxDouble`は数値範囲演算(`Between, NotBetween`)で渡すこともできます。
* 日付フィールドには、`dateVal`を数値比較演算子(`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)で渡すか、minDate/maxDateを数値範囲演算(`Between, NotBetween`)で渡すことができます。

`JobLog`型に説明、`jobSubType`、`originalJobName`フィールドを追加しました。

* `originalJobName` に送信されるジョブ名で `submitJob` す（一意性のサフィックスや後続のジョブ名を除く）。
* `jobSubType` は、現在、ジョブ( `ImageServingPublishJob` またはのいずれか)でのみ使 `full`用さ `increment, fullwithsearch,` れます `fulloverride`。
* `description` は、現在、すべてのジョブタイプに対して空の文字列ですが、最終的には、アップロードパスなどの概要ジョブ情報が含まれます。

また、次のフィールドは`getJobLogs`と`getJobLogDetails`の両方に含まれません。 以前のバージョンでは、`getJobLogDetails`でのみ使用できました。

* `endDate` （ジョブが完了した場合）。
* `fileDuplicateCount` (以前は常にを使用してい `0` まし `getJobLogs`た)
* `fileUpdateCount` (以前は常にに付属し、 `0` に含ま `getJobLogs` れていまし `fileSuccessCount`た)。現在は、別々のフィールドに分割されます)。

`JobLogDetail`タイプにassetHandleフィールドを追加しました。

オプションの説明パラメーターを`submitJob`に追加しました。 `getScheduledJobs`、`getActiveJobs`、`getJobLogs`で取得するために渡されます。

「 SKUシステム」フィールドを非推奨（廃止予定） フィールドが`SystemFieldCondition`として`searchAssets`に渡される場合、このフィールドは無視されます。

`excludeAssetTypeArray`フィルターを`searchAssets`に追加しました。

`MaskInfo`型を`Asset`に追加しました。

IPSによる管理のための新しいアセットタイプを追加しました。

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
   <td colname="col2"> <p>.docで終わるファイル用のMicrosoft Wordドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc  </span> </p> </td> 
   <td colname="col2"> <p>.xlsで終わるファイルに関するMicrosoft Excelドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc  </span> </p> </td> 
   <td colname="col2"> <p>.pptで終わるファイル用のMicrosoft PowerPointドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc  </span> </p> </td> 
   <td colname="col2"> <p>.rtfで終わるファイルのRTFファイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`UploadDirectoryJob`と`UploadUrlsJob`に、Postscript、Illustrator、PDFファイルの処理を個別に制御するオプションを追加しました。 既存のジョブはすべて、現在のとおりに機能するように、3つの処理パイプラインのそれぞれに必要なパラメーターを提供します。 元の`PostScriptOptions`ブロックを使用して、IllustratorおよびEPS/PSファイルの処理を設定します。 オプションで、処理を指定するために特定のファイルオプションブロックを指定できます。 変更点のリストには、次のものが含まれます。

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
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> ラスタラ </span>イズ（デフォルト） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>アセットの管理のみを行い、アップロード時に派生物を作成しないでください。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>EPSファイルとPostScriptファイルを、所定の解像度とカラースペースで画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>（オプション） </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;ブール&gt; </span> </p> </td> 
   <td colname="col4"> <p>ファイルをイメージにラスタライズするときに有効になります。 元のファイルがこの方法でロゴのオーバーレイ用に定義されている場合、透明な背景が作成されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> プロセス </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> なし </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> ラスタラ </span> イズ（デフォルト） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>アセットの管理のみを行い、アップロード時に派生物を作成しないでください。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>所定の解像度とカラースペースでファイルを画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;整数&gt; </span> </p> </td> 
   <td colname="col4"> <p>解像度をラスタライズする。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> カラースペース </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>レンダリングのターゲットカラースペース </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha  </span> </p> <p>（オプション） </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>ファイルをイメージにラスタライズすると、影響を受けます。 元のファイルがこの方法で定義されている場合、透明な背景を作成して、ロゴをオーバーレイします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> プロセス </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> なし </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> ラスタラ </span> イズ（デフォルト） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>アセットの管理のみを行い、アップロード時に派生物を作成しないでください。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>所定の解像度とカラースペースでファイルを画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;整数&gt; </span> </p> </td> 
   <td colname="col4"> <p>解像度をラスタライズする。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> カラースペース </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>レンダリングのターゲットカラースペース </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;ブール&gt; </span> </p> </td> 
   <td colname="col4"> <p>レンダリング後に、複数ページのPDFをeCatalogに結合するかどうかを定義します（デフォルトはtrue）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;ブール&gt; </span> </p> </td> 
   <td colname="col4"> <p>後で検索サーバーに提供するために、PDFからの単語をDBに抽出するかどうかを定義します（デフォルトはfalse）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`getScheduledJobs`からクエリを実行することもできます。

`webservice.gzip.response`設定プロパティを次のいずれかの値に変更しました。

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
   <td colname="col2"> <p>応答をgzipにしないでください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SOAP </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponseがtrueの場合にのみGzipが応答します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 受��入れる </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponseがtrueの場合、またはgzipResponseヘッダーが存在せず、HTTP Accept-Encodingヘッダーにgzipが含まれている場合は、Gzipを使用します。 (初期設定). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> いつも </span> </p> </td> 
   <td colname="col2"> <p>ヘッダー値に関係なく、常にgzip応答。 この値は、デバッグ目的でのみ使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>
