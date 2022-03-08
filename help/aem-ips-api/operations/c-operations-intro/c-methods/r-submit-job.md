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
ht-degree: 8%

---

# submitJob{#submitjob}

ジョブをシステムに送信します。

構文

## 認証済みユーザータイプ {#section-eb7024277bec43c79e03f396205be16f}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-31a07dbccf964850883e817384499459}

**入力 (submitJobParam)**

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
   <td colname="col4"> <p>会社の取り扱い。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブを送信したユーザーに対するハンドル。 </p> <p> <p>注意：システムは、 <span class="codeph"> userHandle</span>. If <span class="codeph"> userHandle</span> が指定されていない場合、ジョブを送信した人が電子メールを受信します。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p>ジョブ名. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブログの詳細と電子メールのローカライゼーションに使用されるロケールです。 </p> <p>ロケールは、 <span class="codeph"> &lt;language_code&gt;</span> および <span class="codeph"> [&lt;country_code&gt;]</span>（言語コードは ISO-639 で指定された小文字、2 文字のコードで、オプションの国コードは ISO-3166 で指定された大文字、2 文字のコードです）。 例えば、英語（米国）のロケール文字列は次のようになります。en-US. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブを実行する日時。 </p> <p>注意：リクエストのタイムゾーンを指定します。 タイムゾーンは、ターゲット IPS サーバーのタイムゾーンに合わせて調整されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブを実行するタイミングを決定します。 </p> <p> 次の値を指定できます。 <span class="codeph"> cron</span> ジョブを繰り返し実行する文字列。 </p> <p>スケジュールは、常にサーバーのローカルタイムゾーンに基づいて設定されます。 カスタムスケジュール形式については、IPS のドキュメントを参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 説明</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ExportJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>以前にアップロードしたファイルを書き出します。 </p> <p>詳しくは、 <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageServingPublishJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>画像サービング公開ジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>画像レンダリング公開ジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：VideoPublishJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ビデオ公開ジョブの詳細。 </p> <p>詳しくは、 <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>サーバーディレクトリ公開ジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：UploadDirectoryJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>アップロードディレクトリジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：UploadUrlsJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>アップロード URL ジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:OptimizeImagesJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：RipPdfsJob</span> </td> 
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
   <td colname="col2"> <span class="codeph"> types:AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>自動セットスクリプトを使用して、アセットリストをセットに処理します。 </p> <p>詳しくは、 <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力 (submitJobReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| jobHandle | `xsd:string` | はい | ジョブハンドル。 |

## 例 {#section-40ac77d14adf4588ba2575be6879b2d2}

このコードサンプルは、画像サービング公開ジョブを IPS に送信し、ジョブハンドルを返します。 リクエストでは 1 つのタイプのジョブのみを選択します。 理由： `userHandle` を省略すると、ジョブを送信したユーザーに電子メール通知が送信されます。 このサンプルジョブは、 `execTime` および `execSchedule` が省略された。

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

最大 1 つの `execTime` および `execSchedule`. どちらも渡されない場合、ジョブは直ちに実行されます。 次のいずれかを使用できます。

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`
