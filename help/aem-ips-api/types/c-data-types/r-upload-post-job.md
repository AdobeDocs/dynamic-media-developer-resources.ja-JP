---
description: getActiveJobsを使用して、デスクトップのアップロードを追跡します。
seo-description: getActiveJobsを使用して、デスクトップのアップロードを追跡します。
seo-title: UploadPostJob
solution: Experience Manager
title: UploadPostJob
topic: Scene7 Image Production System API
uuid: 172f47c7-685a-4014-9c30-dacd78733655
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UploadPostJob{#uploadpostjob}

getActiveJobsを使用して、デスクトップのアップロードを追跡します。

詳しくは、HTTP POSTを [使用したアセットのアップロードを参照してください。](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>アップロードジョブに対するすべてのPOST要求は、同じIPアドレスから送信される必要があります。

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名前 </p> </th> 
   <th colname="col2" class="entry"> <p>種類 </p> </th> 
   <th colname="col03" class="entry"> <p>必須? </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> autoColorCropOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：AutoColorCropOptions</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>色に基づいて画像を自動的に切り抜くオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> autoSetCreationOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AutoSetCreateOptions</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>アップロードされたファイルに適用する自動セット生成スクリプトの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> autoTransparentCropOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：AutoTransparentCropOptions</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>透明度に基づいて、画像の端の余白を削除します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ColorManagementOptions</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>アップロード時に指定できるオプション。 このセットは、アップロードのカラーの管理方法に影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p><b>はい</b> </p> </td> 
   <td colname="col3"> <p>マスクを作成するかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 電子メ <span class="varname"> ール設定</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col03"> <p><b>はい</b> </p> </td> 
   <td colname="col3"> <p>電子メールの設定の選択。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：InDesignOptions</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>InDesignファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：IllustratorOptions</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>IllustratorファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> ノックアウト <span class="varname"> の背景</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：KnockoutBackgroundOptions</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>選択した画像の背景をマスクします。 これにより、他のレイヤーの被写体画像の外側に透明部分を重ね合わせることができます。 （オプション） </p> <p>KnockoutBackgroundOptionsを参照<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"></a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> manualCropOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ManualCropOptions</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>画像の手動切り抜きのオプション。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：MediaOptions</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>ビデオのサムネール画像を設定するオプション。 </p> <p>詳しくは、MediaOptionsを参 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> 照してくださ</a>い。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 上書 <span class="varname"> き</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p><b>はい</b> </p> </td> 
   <td colname="col3"> <p>アップロード時にファイルを上書きするかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PDFOptions</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>PDFファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：PhotoshopOptions</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>PhotoshopファイルをImage Serverにアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>ファイルがアップロードされるURL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postScriptOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PostScriptOptions</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>Image Serverに投稿スクリプトファイルをアップロードするためのオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 切り抜 <span class="varname"> きを保</span> 存 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>既存の作物定義の保存を制御します。 デフォルトはtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> preservePublishState <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p><b>はい</b> </p> </td> 
   <td colname="col3"> <p>既存のアセットを上書きする際に、そのアセットの公開状態を保持するかどうかを制御します。 設定しない場合は、会社のデフォルト設定が使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：HandleArray</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>プロジェクトハンドルの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p><b>はい</b> </p> </td> 
   <td colname="col3"> <p>ファイルが公開準備完了とマークされているかどうか。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> UnCompressOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：UnCompressOptions</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>アップロードしたTAR/ZIPファイルの内容を抽出し、次のオプション設定で処理します。 </p> <p>UnCompressOptionsを参 <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> 照してください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> unsharpMaskOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：UnsharpMaskOptions</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>最適化されたピラミッドTIFファイルを作成する際に、アンシャープマスクの設定を制御するオプション。 これらの設定を使用して、画像のシャープさを改善します。 </p> <p>UnsharpMaskOptionsを参 <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> 照してください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col03"> <p>いいえ </p> </td> 
   <td colname="col3"> <p>アップロードジョブ内のすべてに対する追加のメタデータオプション。 </p> </td> 
  </tr> 
 </tbody> 
</table>

