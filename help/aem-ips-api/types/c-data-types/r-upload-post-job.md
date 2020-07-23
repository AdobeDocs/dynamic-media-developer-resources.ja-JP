---
description: getActiveJobsを使用してデスクトップアップロードを追跡します。
seo-description: getActiveJobsを使用してデスクトップアップロードを追跡します。
seo-title: UploadPostJob
solution: Experience Manager
title: UploadPostJob
topic: Scene7 Image Production System API
uuid: 172f47c7-685a-4014-9c30-dacd78733655
translation-type: tm+mt
source-git-commit: fa8be83171215f39cd2593a3bfe75ffe5fb7abcd
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 6%

---


# UploadPostJob{#uploadpostjob}

getActiveJobsを使用してデスクトップアップロードを追跡します。

詳しくは、HTTP POSTを使用したアセットのアップロードを参照して [ください。](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>アップロードジョブに対するすべてのPOST要求は、同じIPアドレスから送信される必要があります。

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
   <td colname="col2"> <span class="codeph"> 種類：AutoColorCropOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>色に基づいて画像を自動的に切り抜くためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>アップロードされたファイルに適用する自動セット生成スクリプトの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>透明度に基づいて、画像の端から空白を削除します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>アップロード中に指定できるオプション。 このセットは、アップロード時のカラーの管理方法に影響します。 </p> </td> 
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
   <td colname="col4"> <p>電子メールの設定の選択。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：InDesignOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>InDesignファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：IllustratorOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>IllustratorファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>選択した画像の背景をマスクします。 これにより、他のレイヤーの中で、被写体の画像の外側に透明部分を持つレイヤーを重ね合わせることができます。 （オプション） </p> <p>KnockoutBackgroundOptionsを参照してください<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"></a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ManualCropOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>画像の手動切り抜きに関するオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：MediaOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>ビデオのサムネール画像を設定するためのオプション。 </p> <p>MediaOptionsを参照して <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> ください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 上書き</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>はい</p> </td> 
   <td colname="col4"> <p>アップロード時にファイルを上書きするかどうかを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PDFOptions</span> </td> 
   <td colname="col3"> <p>いいえ</p> </td> 
   <td colname="col4"> <p>PDFファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>PhotoshopファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>ファイルのアップロード先URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PostScriptOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>Image Serverに投稿スクリプトファイルをアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>既存の切り抜き定義の保存を制御します。 初期設定は true。</p> <p>manualCropOptionsパラメーターと対応する値を指定した場合は、preserveCrop値に関係なく、新しい値（0,0,0,0を除く）がアセットに適用されます。</p><p>manualCropOptionsパラメータ <i>を指定しない場合</i> 、preserveCropの値は維持されます。 また、trueの場合は、既存のpreserveCrop値が保持されます。 falseの場合、preserveCrop値は削除されます。</p><p>例：</p><p><p>&lt;preserveCrop&gt;false&lt;/preserveCrop&gt;<br />&lt;manualCropOptions&gt;<br />&lt;left&gt;&lt;right&gt;<br />&lt;right&gt;310&lt;/right&gt;<br />&lt;top&gt;160&lt;/top&gt;&lt;bottom&gt;120&lt;/bottom&gt;<br /><br />&lt;/manualCrop Options&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>はい</b> </p> </td> 
   <td colname="col4"> <p>既存のアセットを上書きする際に、そのアセットの公開状態を保持するかどうかを制御します。 設定されていない場合は、会社のデフォルト設定が使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：HandleArray</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>プロジェクトハンドルの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>はい</b> </p> </td> 
   <td colname="col4"> <p>ファイルが公開準備完了とマークされているかどうかを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：UnCompressOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>アップロードしたTAR/ZIPファイルの内容を抽出し、次のオプション設定で処理します。 </p> <p>UnCompressOptionsを参照して <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> ください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>最適化されたピラミッドTIFファイルを作成する際に、アンシャープマスクの設定を制御するためのオプション。 これらの設定を使用して、画像のシャープさを向上させます。 </p> <p>UnsharpMaskOptionsを参照して <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> ください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>アップロードジョブ内のすべての項目に対する追加のメタデータオプションです。 </p> </td> 
  </tr> 
 </tbody> 
</table>

