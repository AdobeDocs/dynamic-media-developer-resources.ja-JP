---
description: サーバー上で実行するジョブ。 また、これはスケジュールされたジョブのインスタンスです。
seo-description: サーバー上で実行するジョブ。 また、これはスケジュールされたジョブのインスタンスです。
seo-title: ActiveJob
solution: Experience Manager
title: ActiveJob
topic: Scene7 Image Production System API
uuid: d7120a88-6f3e-4844-aafa-83d419470fad
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ActiveJob{#activejob}

サーバー上で実行するジョブ。 また、これはスケジュールされたジョブのインスタンスです。

ジョブが3つの状態に存在する：

* 実行がスケジュールされています。
* 現在実行中です。
* 実行が完了しました（ジョブログに情報が既に書き込まれています）。

ジョブの種類を返すジョブの種類の値を指定します。 次のジョブを返すことができます。

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublish`
* `JobUploadDirectoryJob`
* `uploadUrlsJob`

## パラメータ {#section-6590fe864a434000822b9ec384784512}

<table id="table_1C4DDAB4EB1341FDA92B6F14E0132F75"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 会社の取り扱い。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブの処理。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 名 <span class="varname"> 前</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブの一意の名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 元 <span class="varname"> の名</span> 前 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">ジョブと共に送信さ <span class="codeph"> れた</span> ActiveJobタイプの元の名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> システムから返されるジョブタイプの選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> state</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> システムから返されたアクティブなジョブ状態の選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブをスケジュールしたユーザーの電子メールアドレス。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">ジョブログの詳細と電子メールのローカリゼーションのロケールです。 <p>ロケールは <span class="codeph"> &lt;language_code&gt;[-&lt;country_code&gt;]</span>（言語コードはISO-639で指定された小文字の2文字のコードで、オプションの国コードはISO-3166で指定された大文字の2文字のコードです）と指定します。 例えば、英語（米国）のロケール文字列は次のようになります。 <span class="codeph"> en-US</span>。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 説 <span class="varname"> 明</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">最初にsubmitJobで指定されたジョ <span class="codeph"> ブの説明</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブを実行しているサーバーの名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> startDate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> アクティブなジョブの日付、時刻、およびタイムゾーン。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> totalSize</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> アクティブなジョブの合計サイズ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 進 <span class="varname"> 行</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> ジョブの進行状況（ジョブが完了するまでにどれだけ近いか）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> ジョブの進行状況を説明するテキストメッセージです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 前回の進行状況の更新の日付、時刻およびタイムゾーン。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> taskProgressArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：TaskProgressArray</span> </td> 
   <td colname="col3"> 非同期タスクの進行状況の情報。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 画像サービング公開ジョブのジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingRenderJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：ImageServingRenderJob</span> </td> 
   <td colname="col3"> 画像レンダリング公開ジョブのジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> videoPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：VideoPublishJob</span> </td> 
   <td colname="col3"> ビデオ公開ジョブのジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> serverDirectoryPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：ImageServingPublishJob</span> </td> 
   <td colname="col3"> サーバーディレクトリ公開ジョブのジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> uploadUrlsJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：UploadUrlsJob</span> </td> 
   <td colname="col3"> アップロードURLジョブのジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> PdfsJobの <span class="varname"> 取り込み</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：RipPdfsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> optimizeImagesJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> reprocessAssetsJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> uploadPostJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：UploadPostJob</span> </td> 
   <td colname="col3"> デスクトップアップロードのジョブ詳細追跡。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ExportJob</span> </td> 
   <td colname="col3">以前にアップロードされたファイルの承認されたエクスポートを許可します。 詳しくは、 <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exportjob.html" format="http" scope="external"> ジョブの書き出し</a>。 </td> 
  </tr> 
 </tbody> 
</table>

