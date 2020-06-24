---
description: サーバー上で実行するジョブ。 また、これはスケジュール済みジョブのインスタンスです。
seo-description: サーバー上で実行するジョブ。 また、これはスケジュール済みジョブのインスタンスです。
seo-title: ActiveJob
solution: Experience Manager
title: ActiveJob
topic: Scene7 Image Production System API
uuid: d7120a88-6f3e-4844-aafa-83d419470fad
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 1%

---


# ActiveJob{#activejob}

サーバー上で実行するジョブ。 また、これはスケジュール済みジョブのインスタンスです。

ジョブは3つの状態に存在します：

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 会社へのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブの処理。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブの一意の名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> originalName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">ジョブと共に送信された <span class="codeph"> ActiveJob</span> 型の元の名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> システムから返されるジョブタイプの選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> state</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> システムが返すアクティブなジョブ状態の選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブをスケジュールしたユーザーの電子メールアドレス。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">ジョブログの詳細と電子メールローカライゼーションのロケール。 <p>ロケールは <span class="codeph"> &lt;language_code&gt;[-&lt;country_code&gt;]</span>（言語コードはISO-639で指定された小文字の2文字のコードで、オプションの国コードはISO-3166で指定された大文字の2文字のコードです）と指定します。 例えば、英語（米国）のロケール文字列は次のようになります。 <span class="codeph"> en-US</span>。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> description</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">ジョブの説明は、最初はsubmitJob <span class="codeph"> で指定されています</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブを実行しているサーバーの名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> startDate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> アクティブなジョブの日付、時刻、およびタイムゾーン。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> totalSize</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> アクティブなジョブの合計サイズ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 進行状況</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> ジョブの進行状況（ジョブが完了するまでの間隔など） </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> ジョブの進行状況を説明するテキストメッセージです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 前回の進行状況の更新日、時刻およびタイムゾーン。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：TaskProgressArray</span> </td> 
   <td colname="col3"> 非同期タスクの進行状況の情報。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 画像サービング公開ジョブのジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingRenderJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：ImageServingRenderJob</span> </td> 
   <td colname="col3"> 画像レンダリング公開ジョブのジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：VideoPublishJob</span> </td> 
   <td colname="col3"> ビデオ公開ジョブのジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ImageServingPublishJob</span> </td> 
   <td colname="col3"> サーバーディレクトリ公開ジョブのジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：UploadUrlsJob</span> </td> 
   <td colname="col3"> アップロードURLジョブのジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：RipPdfsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadPostJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：UploadPostJob</span> </td> 
   <td colname="col3"> デスクトップアップロードのジョブ詳細追跡。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ExportJob</span> </td> 
   <td colname="col3">以前にアップロードされたファイルの承認されたエクスポートを許可します。 詳しくは、 <a href="https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-exportjob.html" format="http" scope="external"> ジョブの書き出し</a>を参照してください。 </td> 
  </tr> 
 </tbody> 
</table>

