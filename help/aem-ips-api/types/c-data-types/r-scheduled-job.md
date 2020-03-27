---
description: 実行がスケジュールされているジョブ。
seo-description: 実行がスケジュールされているジョブ。
seo-title: ScheduledJob
solution: Experience Manager
title: ScheduledJob
topic: Scene7 Image Production System API
uuid: cf0db523-2138-48c6-abbd-460a961e7de1
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ScheduledJob{#scheduledjob}

実行がスケジュールされているジョブ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 会社の担当。 |
| ` *`jobHandle`*` | `xsd:string` | スケジュールされたジョブの処理。 |
| ` *`name`*` | `xsd:string` | ジョブ名. |
| ` *`originalName`*` | `xsd:string` | スケジュールされたジョブの元の名前。 |
| ` *`type`*` | `xsd:string` | ジョブのタイプ。 |
| ` *`submitUserEmail`*` | `xsd:string` | ジョブをスケジュールしたユーザーの電子メールアドレス。 |
| ` *`locale`*` | `xsd:string` | ジョブログの詳細および電子メールのローカリゼーションに使用するロケールです。 ロケールは、 `<language_code>[- <country_code>]`ISO-639で指定された小文字の2文字のコードを言語コードとして指定し、オプションの国コードは、ISO-3166で指定された大文字の2文字のコードを使用します。 例えば、英語（米国）のロケール文字列は次のようになります。 `en-US`. |
| ` *`説明`*` | `xsd:string` | で最初に指定されたジョブの説明 `submitJob`。 |
| ` *`execSchedule`*` | `xsd:string` | ジョブの実行がスケジュールされた日時。 |
| ` *`nextFireTime`*` | `xsd:dateTime` | ジョブが実行される日付、時刻、およびタイムゾーン。 |
| ` *`timeZone`*` | `xsd:dateTime` | スケジュールされたジョブのタイムゾーン。 |
| ` *`triggerState`*` | `xsd:int` | ジョブトリガー状態の選択。 |
| ` *`imageServingPublishJob`*` | `types:ImageServingPublishJob` | 画像サービング公開ジョブのジョブの詳細。 |
| ` *`imageServingRenderJob`*` | `types:ImageServingRenderJob` | 画像レンダリングジョブのジョブの詳細。 |
| ` *`videoPublishJob`*` | `types:VideoPublishJob` | ビデオ公開ジョブのジョブの詳細。 VideoPublishJobを参照し [てください](https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_scheduled_job.html)。 |
| ` *`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | サーバーディレクトリ公開ジョブのジョブの詳細。 |
| ` *`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | アップロードディレクトリジョブのジョブの詳細。 |
| ` *`uploadUrlsJob`*` | `types:UploadUrlsJob` | アップロードURLジョブのジョブの詳細。 |
| ` *`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| ` *`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| ` *`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| ` *`exportJob`*` | `types:ExportJob` | 以前にアップロードされたファイルの承認されたエクスポートを許可します。 詳しくは、 [ジョブの書き出し](https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_scheduled_job.html)。 |

## 説明 {#section-34ec157f281f412f9f0f6e861e6ed0cd}

でジョブタイプの値を指定すると、そ `submitJob`のタイプに基づいてジョブが返されます。 次のジョブを返すことができます。

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

