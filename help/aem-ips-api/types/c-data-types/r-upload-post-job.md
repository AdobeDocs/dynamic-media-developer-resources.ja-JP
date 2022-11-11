---
description: getActiveJobs を使用してデスクトップのアップロードを追跡します。
solution: Experience Manager
title: UploadPostJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 60163016-fe96-4ac2-9208-da8192042d0f
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 7%

---

# [!DNL UploadPostJob]{#uploadpostjob}

getActiveJobs を使用してデスクトップのアップロードを追跡します。

関連トピック [HTTP POST を使用してアセットをアップロード中…](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>アップロードPOSTに対するすべてのジョブリクエストは、同じ IP アドレスから送信される必要があります。

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名前 </p> </th> 
   <th colname="col2" class="entry"> <p>種類 </p> </th> 
   <th colname="col3" class="entry"> <p>必須? </p> </th> 
   <th colname="col4" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutoColorCropOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>色に基づいて画像が自動的に切り抜かれるオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>アップロードされたファイルに適用する自動セット生成スクリプトの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>透明度に基づいて、画像の端から空白を削除します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>アップロード中に指定できるオプション。 セットは、アップロードでのカラーの管理方法に影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>はい</b> </p> </td> 
   <td colname="col4"> <p>マスクを作成するかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><b>はい</b> </p> </td> 
   <td colname="col4"> <p>メール設定の選択。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：InDesignOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>Image Server にInDesignファイルをアップロードするためのオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：IllustratorOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>Illustratorファイルを Image Server にアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>選択した画像の背景をマスクします。 これにより、他のレイヤーに、被写体の画像の外側に透明度を付けてオーバーレイできます。 （オプション） </p> <p>詳しくは、<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ManualCropOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>画像の手動切り抜きのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：MediaOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>ビデオからサムネール画像を設定できるオプション。 </p> <p>詳しくは、 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 上書き</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>はい</p> </td> 
   <td colname="col4"> <p>アップロード時にファイルを上書きするかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PDFOptions</span> </td> 
   <td colname="col3"> <p>いいえ</p> </td> 
   <td colname="col4"> <p>Image Server にPDFファイルをアップロードするためのオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>Photoshopファイルを Image Server にアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>ファイルがアップロードされる URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PostScriptOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>Post スクリプトファイルを Image Server にアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>既存の切り抜き定義の保存を制御します。 初期設定は true。</p> <p>manualCropOptions パラメーターと対応する値を指定した場合、preserveCrop の値に関係なく、新しい値（0、0、0、0 を除く）がアセットに適用されます。</p><p>もし <i>not</i> manualCropOptions パラメーターを指定した場合、preserveCrop の値は維持されます。 また、true の場合、既存の preserveCrop 値は保持されます。false の場合、preserveCrop 値は削除されます。</p><p>例：</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>はい</b> </p> </td> 
   <td colname="col4"> <p>上書き時に既存のアセットの公開状態を保持するかどうかを制御します。 設定されていない場合は、会社のデフォルト設定が使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>プロジェクトハンドルの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>はい</b> </p> </td> 
   <td colname="col4"> <p>ファイルの公開準備ができたとマークされているかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：UnCompressOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>アップロードした TAR/ZIP ファイルの内容を、以下のオプション設定で抽出して処理します。 </p> <p>詳しくは、 <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>最適化されたピラミッド TIF ファイルを作成する際に、アンシャープマスク設定を制御するオプションです。 これらの設定を使用すると、画像のシャープネスを改善できます。 </p> <p>詳しくは、 <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>アップロードジョブ内のすべての項目に対する追加のメタデータオプション。 </p> </td> 
  </tr> 
 </tbody> 
</table>
