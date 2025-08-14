---
description: ジョブをシステムに送信します。
solution: Experience Manager
title: submitJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b1dc7a0e-da9a-4086-822b-5274bd62eadf
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 7%

---

# submitJob{#submitjob}

ジョブをシステムに送信します。

構文

## 許可されているユーザータイプ {#section-eb7024277bec43c79e03f396205be16f}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-31a07dbccf964850883e817384499459}

**入力（submitJobParam）**

<table id="table_9CB1F668E036422E8CE4E0BBA42EC44C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名前 </p> </th> 
   <th colname="col2" class="entry"> <p>種類 </p> </th> 
   <th colname="col3" class="entry"> <p>必須 </p> </th> 
   <th colname="col4" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p>会社ハンドル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブを送信したユーザーへのハンドル。 </p> <p> <p>メモ：userHandle<span class="codeph"> で指定したユーザーにメールが送信 </span> れます。 userHandle<span class="codeph"></span> 指定されていない場合、ジョブを送信したユーザーがメールを受け取ります。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p>ジョブ名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブ ログの詳細および E メール ローカリゼーションに使用されるロケールです。 </p> <p>ロケールは <span class="codeph"> &lt;language_code&gt;</span> および <span class="codeph"> [&lt;country_code&gt;]</span> として指定します。言語コードは ISO-639 で指定される小文字の 2 文字コードで、オプションの国コードは ISO-3166 で指定される大文字の 2 文字コードです。 例えば、英語（米国）のロケール文字列は en-US になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブを実行する日時。 </p> <p>メモ：リクエストのタイムゾーンを指定します。 タイムゾーンは、ターゲット IPS サーバーのタイムゾーンに合わせて調整されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブを実行するタイミングを決定します。 </p> <p> ジョブを繰り返し実行する <span class="codeph"> cron</span> 文字列を指定できます。 </p> <p>スケジュールは、常にサーバーのローカルタイムゾーンを基準とした相対スケジュールになります。 カスタムスケジュール形式については、IPS ドキュメントを参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> の説明 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ExportJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>以前にアップロードしたファイルを書き出します。 </p> <p><a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a> を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ImageServingPublishJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>画像サービング公開ジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>画像レンダリング公開ジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：VideoPublishJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ビデオ公開ジョブの詳細。 </p> <p>VideoPublishJob<a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"></a> 参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> の種類：ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>サーバーディレクトリ公開ジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：UploadDirectoryJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ディレクトリのアップロードジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：UploadUrlsJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>アップロード URL ジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：OptimizeImagesJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> の種類：RipPdfsJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ReprocessAssetsJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> automatedSetGenerationJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> の種類：AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>Automated Set スクリプトを使用して、アセットリストをセットに処理します。 </p> <p>AutomatedSetGenerationJob<a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"></a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力（submitJobReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| jobHandle | `xsd:string` | はい | ジョブハンドル。 |

## 例 {#section-40ac77d14adf4588ba2575be6879b2d2}

このコードサンプルでは、公開ジョブを提供する画像を IPS に送信し、ジョブハンドルを返します。 リクエストで 1 つのタイプのジョブのみを選択します。 `userHandle` が省略されたため、ジョブを送信したユーザーにメール通知が送信されます。 このサンプルジョブは、`execTime` と `execSchedule` が省略されたので、すぐに実行されます。

**リクエスト**

```java
<submitJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobName>My Test Job</jobName>
   <imageServingPublishJob>
      <publishType>Full</publishType>
      <emailSetting>Error</emailSetting>
   </imageServingPublishJob>
</submitJobParam>
```

**応答**

```java
<submitJobReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobHandle>47|My Test Job|</jobHandle>
</submitJobReturn>
```

## 説明 {#section-0f3078e503a249aeb6f3d662a51f036a}

指定できる値は、`execTime` と `execSchedule` のいずれか 1 つだけです。 どちらも渡されない場合、ジョブは直ちに実行されます。 次のうちいずれか 1 つのみを使用できます。

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`
