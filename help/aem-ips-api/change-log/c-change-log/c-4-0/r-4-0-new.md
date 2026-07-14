---
title: 新しい追加と変更
description: IPS API v4.0の新しい変更と実装された変更について説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
TQID: 'https://experienceleague.adobe.com/QuVnFsc1R-WcjFpnyENi6n9US7Y7V-cETwitnVsmMss'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 1207
ht-degree: 0%

---

# 新しい追加と変更{#new-additions-and-changes}

IPS API v4.0の新しい変更と実装された変更について説明します。

個別のWSDLとスキーマ名前空間を持つ並列API バージョンを実装しました。

* 以前のAPI バージョン：`IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`。
* SPS 4.0 バージョン：`IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`。

`PostScriptOptions/alpha` フィールドを追加しました。

`getProperty`操作に`VideoRootUrl`と`SwfRootUrl`のプロパティを追加しました。

呼び出し元のアプリケーションを追跡するために、オプションの`appName`および`appVersion`個のパラメーターを`authHeader`に追加しました。 ログを`ipsApiService.log`に追加しました。

オプションの`serviceUrl` パラメーターをWSDL生成サーブレットに追加しました。 このパラメーターは、デバッグプロキシに便利です。 例：`http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

`getZipEntries`操作を実装しました。

システムフィールド条件の検索範囲と入力済み比較値を実装しました。

アセットタイプ文字列定数`'Asset'`を追加しました。主に、クロスアセットのメタデータフィールドを許可します。

`searchAssets`の`trashState` パラメーターを実装しました。

`getAssetPublishHistory`操作を実装しました。

Flexでエラー処理を有効にするために、オプションの`faultHttpStatusCode` SOAP ヘッダーを追加しました。 Flexの場合は、`<faultHttpStatusCode>200</faultHttpStatusCode>`を使用します。 フォールト応答の既定の状態コードは`500 (Internal Server Error)`です。

ゴミ箱からアセットを復元する操作と、ゴミ箱から空のアセットを復元する操作を追加しました。

CRUD操作を実装しました。

有効なフラグを`ImageMap`種類と`saveImageMap`操作に追加しました。

残りファイルを最適化ジョブのサポートを追加しました。

一括公開状態の更新用に`setAssetsPublishState`を追加しました。

`ImageServingPublishSettings`、`getImageServingPublishSettings`、`setImageServingPublishSettings`を追加しました。

新しい`createMetadataField`および`updateMetadataField`操作を優先して、`saveMetadataField`操作を廃止しました。

`deleteAssetsParam` バッチ削除操作を実装しました。

`moveAssetsParam` バッチ移動操作を実装しました。

`deleteMetadataField`操作を実装しました。

`get/setImageRenderingPublishSettings`、`get/set/create/updateVignettePublishFormat`操作を実装しました。

`getAssetCounts`を実装しました。

`ImageSet`個のアセットに`RenderSet`人のメンバーを含めるためのサポートを`setImageSetMembers`に追加しました。

`replaceImage`操作を追加しました。

`copyImage`操作を追加しました。

`LayerViewInfo`、`TemplateInfo`、`WatermarkInfo`に`setUrlModifier`操作と`urlModifier/urlPostApplyModifier` フィールドを追加しました。

`createDerivedAsset`操作を追加しました。 現在、`ownerHandle`は画像アセットを参照する必要があり、タイプは`AdjustedView`または`LayerView`である可能性があります。

`createTemplate`操作を追加しました。 テンプレートまたは透かしアセットを作成するための呼び出し。

IPS会社の設定`CompanySettings`、Web サービス APIに報告されました。

`excludeByproducts` フィルターフラグを`searchAssets`操作に追加しました。 このフラグをtrueに設定すると、`PSDlayer`枚の画像とPDFで画像がリッピングされます。

`getGenerationInfo`操作を追加しました。

`SystemMessage` プロパティ名を`getProperty`操作に追加しました。

一部のアセットタイプ文字列定数を、対応するアセット情報フィールドと一致するように変更しました。

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

成功、警告、エラーを要約するために、バッチ操作の結果形式を変更しました。

`batchSetAssetMetadata` バッチメタデータ操作を実装しました。

アプリ固有のデータのサポートを実装しました。

Photoshop処理のプロセスを制御するアップロードジョブの`createTemplate`、`extendLayers`および`extractText`のブール値フラグのサポートを実装しました（ファイルのアップロードを追加する場合の変更点と同様）。

`setImageMaps`および`setZoomTargets`操作を実装しました。

`ViewerPreset`操作を実装しました。 認識される型は次のとおりです。

* `VideoPlayer` （ビデオはこれらのビューアのみを公開します）
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

ビューアのスキンは、次の2つのパラメーターをサポートしています：`skinFg`と`skinBg`。 バックエンドコードは、下位互換性を維持するために必要なすべての処理を行います。

`getAssociatedAssets`操作を実装しました。

PDFのリッピングや画像の再最適化など、以前アップロードしたプライマリソースファイルの再処理を可能にする`ReprocessAssets`件のジョブタイプを追加しました。

フィールドの種類`PropertySetType`を`propertyType`に変更しました。 この名前の変更は、`createPropertySetType` パラメーターと`getPropertySetType/getPropertySetTypes`応答に影響します。

画像ユーザーデータおよびその他の編集可能な画像フィールドの設定をサポートする`batchSetImageFields`操作を実装しました。

47さまざまなアセット情報タイプにfileSize フィールドを追加しました。

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

`getActivePublishContexts`操作を実装しました。 この操作は、指定された会社のアクティブな公開サーバーを含む公開コンテキスト名の配列を返します。 現在のパブリッシュコンテキスト名は次のとおりです。

* `ImageServing`
* `ImageRendering`
* `Video`

`getSearchStrings`操作を実装しました。 指定されたアセットの検索文字列の配列を返します。

ジョブのロケールパラメーターと、API操作のロケールを設定するメカニズムを追加しました。 ロケール文字列は`<language_code>[-<country_code>]`形式にする必要があります。 言語コードは、ISO-639で指定された小文字の2文字コードで、オプションの国コードは、ISO-3166で指定された大文字の2文字コードです。

`authHeader` SOAP ヘッダーにオプションのロケールパラメーターを追加して、API操作のロケールを設定しました。 このパラメーターが存在しない場合は、HTTP ヘッダー`Accept-Language`が使用されます。 このヘッダーも存在しない場合は、IPS サーバーのデフォルトのロケールが使用されます。

強力に入力されたメタデータフィールドの取得/設定のサポートを追加しました。

Gzip応答制御のためのSOAPおよびHTTP ヘッダーのサポートを実装しました。

`gzipResponse` フラグを`authHeader`に追加しました。 存在しない場合、APIはHTTP `Accept-Encoding` ヘッダーをチェックします。

強力に入力されたメタデータフィールド条件に対するsearchAssetsのサポートを追加しました。

* すべてのフィールドタイプに対して、文字列比較演算子（`Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`）で値を渡すことができます
* ブール型フィールドの場合、`boolVal`は`Equals` opで渡すことができます。
* Int フィールドの場合、`longVal`を数値比較演算子（`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`）で渡したり、`minLong/maxLong`を数値範囲演算（`Between, NotBetween`）で渡したりできます。
* 浮動小数点フィールドの場合、`doubleVal`を数値比較演算子（`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`）で渡したり、`minDouble/maxDouble`を数値範囲演算（`Between, NotBetween`）で渡したりできます。
* 日付フィールドの場合は、数値比較演算子（`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`）で`dateVal`を渡すか、数値範囲演算（`Between, NotBetween`）でminDate/maxDateを渡すことができます。

説明、`jobSubType`、および`originalJobName` フィールドを`JobLog` タイプに追加しました。

* `originalJobName`は、`submitJob`に送信されたジョブ名です（一意の接尾辞や後続のジョブ名は含まれません）。
* `jobSubType`は`ImageServingPublishJob`個のジョブでのみ使用されます（このジョブは`full`、`increment, fullwithsearch,`または`fulloverride`のいずれかです）。
* `description`は、すべてのジョブタイプに対して空の文字列ですが、最終的にはアップロードパスなどの概要ジョブ情報が含まれます。

また、次のフィールドは`getJobLogs`と`getJobLogDetails`の両方に含まれていません。 以前のバージョンでは、`getJobLogDetails`でのみ使用できました。

* `endDate` （ジョブが完了した場合）。
* `fileDuplicateCount` （以前は常に`0`、以前は`getJobLogs`）
* `fileUpdateCount` （以前は`getJobLogs`の`0`で、`fileSuccessCount`に含まれていました。現在は別々のフィールドに分割されています）。

assetHandle フィールドを`JobLogDetail` タイプに追加しました。

オプションの説明パラメーターを`submitJob`に追加しました。 このパラメーターは、`getScheduledJobs`、`getActiveJobs`、`getJobLogs`で取得するために渡されます。

SKU システムフィールドを非推奨（廃止予定）にしました。 フィールドは、`SystemFieldCondition`として`searchAssets`に渡された場合は無視されます。

`excludeAssetTypeArray` フィルターを`searchAssets`に追加しました。

`MaskInfo` タイプを`Asset`に追加しました。

IPSによる管理に新しいアセットタイプを追加しました。

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
   <td colname="col2"> <p>EPSおよびPostScript ファイル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>.docで終わるファイルのMicrosoft® Word ドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>.xlsで終わるファイルのMicrosoft® Excel ドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>.pptで終わるファイルのMicrosoft® PowerPoint ドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>.rtfで終わるファイルのRTF ファイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

Postscript、Illustrator、PDF ファイルの処理を個別に制御するために、`UploadDirectoryJob`および`UploadUrlsJob`に追加オプションを追加しました。 既存のすべてのジョブは、3つの処理パイプラインのそれぞれに必要なパラメーターを提供するため、現在と同じように機能します。 元の`PostScriptOptions` ブロックは、IllustratorおよびEPS/PS ファイルの処理を設定するために使用されます。 オプションで、特定のファイルオプションブロックを指定して処理を指定できます。 変更内容のリストには、次のものが含まれます。

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
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>アセットのみを管理し、アップロード時に派生を作成しないでください。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>EPSとPostScript ファイルを、指定した解像度とカラースペースで画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> アルファ </span> </p> <p>オプション。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>ファイルを画像にラスタライズする際に効果を発揮します。 元のファイルがロゴのオーバーレイ用にこのように定義されている場合は、透明な背景が作成されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> プロセス </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> None </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> ラスタライズ </span> （既定値） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>アセットのみを管理し、アップロード時に派生を作成しないでください。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>指定した解像度とカラースペースでファイルを画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;整数&gt; </span> </p> </td> 
   <td colname="col4"> <p>解像度のラスタライズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>レンダリング用のターゲットカラースペース </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> アルファ </span> </p> <p>オプション。 </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>ファイルを画像にラスタライズする際に効果を発揮します。 元のファイルがオーバーレイのロゴを作成するためにこの方法で定義されている場合は、透明な背景を作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> プロセス </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> None </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> ラスタライズ </span> （既定値） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>アセットのみを管理し、アップロード時に派生を作成しないでください。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>指定した解像度とカラースペースでファイルを画像にレンダリングします。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;整数&gt; </span> </p> </td> 
   <td colname="col4"> <p>解像度のラスタライズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>レンダリング用のターゲットカラースペース </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>レンダリング後に複数ページのPDFをeCatalogに組み合わせるかどうかを定義します（デフォルトはtrue）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>PDFの単語をDBに抽出して、後で検索サーバーに提供するかどうかを定義します（デフォルトはfalse）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`getScheduledJobs`からクエリすることもできます。

次のいずれかの値を取るように`webservice.gzip.response`設定プロパティを変更しました：

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
   <td colname="col2"> <p>応答をgzip形式にしないでください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>Gzip応答は、authHeader/gzipResponseがtrueの場合のみ有効です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponseがtrueの場合、またはgzipResponse ヘッダーが存在せず、HTTP Accept-Encoding ヘッダーにgzipが含まれている場合はGzip。 （Default）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>ヘッダー値に関係なく、常にgzip応答を使用します。 この値は、デバッグの目的でのみ使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

