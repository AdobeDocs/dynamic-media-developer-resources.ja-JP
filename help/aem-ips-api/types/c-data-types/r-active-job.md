---
title: ActiveJob
description: サーバーで実行されるジョブ。 また、スケジュール済みジョブのインスタンスです。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3d878207-99e4-4c75-ab12-b38a37c82fb7
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 1%

---

# [!DNL ActiveJob]{#activejob}

サーバーで実行されるジョブ。 また、スケジュール済みジョブのインスタンスです。

ジョブは次の 3 つの状態で存在します。

* 実行がスケジュールされています。
* 現在実行中です。
* 実行が完了しました（および既にジョブログに情報を書き込んでいます）。

ジョブタイプを返すには、ジョブタイプの値を指定します。 次のジョブを返すことができます。

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
   <td colname="col3"> 会社に対する取り扱い。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブを処理します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名前</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブの一意の名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> originalName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">元の <span class="codeph"> ActiveJob</span> ジョブで送信されたタイプ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> システムから返されるジョブタイプの選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> state</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> システムから返されるアクティブなジョブ状態の選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブをスケジュールしたユーザーの電子メールアドレス。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">ジョブログの詳細と電子メールのローカライゼーションのロケールです。 <p>ロケールをとして指定します。 <span class="codeph"> &lt;language_code&gt;[-&lt;country_code&gt;]</span>（言語コードは ISO-639 で指定された小文字 2 文字のコードで、オプションの国コードは ISO-3166 で指定された大文字 2 文字のコードです）。 例えば、英語（米国）のロケール文字列は次のようになります。 <span class="codeph"> en-US</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 説明</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">元々で指定されていたジョブの説明 <span class="codeph"> submitJob</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブを実行するサーバーの名前。 </td> 
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
   <td colname="col3"> ジョブの進行状況（ジョブが完了するまでの距離）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> ジョブの進行状況を示すテキストメッセージです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 前回の進行状況更新の日付、時刻、タイムゾーン。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:TaskProgressArray</span> </td> 
   <td colname="col3"> 非同期タスクの進捗状況情報。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageServingPublishJob</span> </td> 
   <td colname="col3"> 画像サービング公開ジョブのジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingRenderJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageServingRenderJob</span> </td> 
   <td colname="col3"> 画像レンダリング公開ジョブのジョブ詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：VideoPublishJob</span> </td> 
   <td colname="col3"> ビデオ公開ジョブのジョブの詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageServingPublishJob</span> </td> 
   <td colname="col3"> サーバーディレクトリ公開ジョブのジョブ詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：UploadUrlsJob</span> </td> 
   <td colname="col3"> アップロード URL ジョブのジョブ詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：RipPdfsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadPostJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：UploadPostJob</span> </td> 
   <td colname="col3"> ジョブの詳細、デスクトップのアップロードを追跡します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ExportJob</span> </td> 
   <td colname="col3">以前にアップロードしたファイルの承認済み書き出しを許可します。 詳しくは、 <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-exportjob.html" format="http" scope="external"> 書き出しジョブ</a>. </td> 
  </tr> 
 </tbody> 
</table>
