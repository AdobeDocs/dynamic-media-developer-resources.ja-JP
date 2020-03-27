---
description: ジョブをシステムに送信します。
seo-description: ジョブをシステムに送信します。
seo-title: submitJob
solution: Experience Manager
title: submitJob
topic: Scene7 Image Production System API
uuid: d3a83b59-bcd7-4ae9-b1ee-e515fc3c9261
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# submitJob{#submitjob}

ジョブをシステムに送信します。

構文

## 認証されたユーザータイプ {#section-eb7024277bec43c79e03f396205be16f}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-31a07dbccf964850883e817384499459}

**入力(submitJobParam)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p>会社の担当。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブを送信したユーザーの処理。 </p> <p> <p>注意：システムは、userHandleで指定されたユーザーに電子メールを送 <span class="codeph"> 信します</span>。 userHandleが指 <span class="codeph"> 定されない場合</span> 、ジョブを送信した人が電子メールを受信します。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p>ジョブ名. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブログの詳細と電子メールのローカリゼーションに使用するロケールです。 </p> <p>ロケールは <span class="codeph"> &lt;language_code&gt;</span><span class="codeph"></span>および[&lt;country_code&gt;]と指定します。言語コードはISO-639で指定された小文字の2文字のコードで、オプションの国コードはISO-3166で指定された大文字の2文字のコードです。 例えば、英語（米国）のロケール文字列は次のようになります。en-US. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブを実行する日時。 </p> <p>注意： リクエストのタイムゾーンを指定します。 タイムゾーンは、対象のIPSサーバのタイムゾーンに合わせて調整されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブを実行するタイミングを指定します。 </p> <p> 定期的にジョブ <span class="codeph"> を実行する</span> cron文字列を指定できます。 </p> <p>スケジュールは、常にサーバーのローカルタイムゾーンに対する相対的な設定です。 カスタムスケジュールの形式については、IPSのドキュメントを参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 説 <span class="varname"> 明</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ジョブの説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ExportJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>以前にアップロードしたファイルを書き出します。 </p> <p>ExportJobを参照し <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> てください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：ImageServingPublishJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>画像サービング公開ジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> imageRenderingPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>画像レンダリング公開ジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> videoPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：VideoPublishJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>ビデオ公開ジョブの詳細。 </p> <p>VideoPublishJobを参照し <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> てください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> serverDirectoryPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>サーバーディレクトリ公開ジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> uploadDirectoryJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：UploadDirectoryJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>アップロードディレクトリジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> uploadUrlsJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：UploadUrlsJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>アップロードURLジョブの詳細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> optimizeImagesJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：OptimizeImagesJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> PdfsJobの <span class="varname"> 取り込み</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：RipPdfsJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> reprocessAssetsJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ReprocessAssetsJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> automatedSetGenerationJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>自動セットスクリプトを使用して、アセットリストをセットに処理します。 </p> <p>AutomatedSetGenerationJobを参照し <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> てください</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(submitJobReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`jobHandle`*` | `xsd:string` | はい | ジョブハンドル。 |

## 例 {#section-40ac77d14adf4588ba2575be6879b2d2}

このコード例では、画像サービング公開ジョブをIPSに送信し、ジョブハンドルを返します。 リクエスト内のジョブのタイプを1つだけ選択します。 が省略さ `userHandle` れたので、ジョブを送信したユーザーに電子メール通知が送信されます。 このサンプルジョブは、省略されたので、す `execTime` ぐに実 `execSchedule` 行されます。

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

とのうち1つ以上を指定でき `execTime` ます `execSchedule`。 どちらも渡されない場合、ジョブは直ちに実行されます。 次のいずれか1つのみを使用できます。

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`

