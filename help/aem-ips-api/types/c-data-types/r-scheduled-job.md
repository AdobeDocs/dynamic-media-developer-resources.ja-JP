---
description: 実行がスケジュールされているジョブ。
seo-description: 実行がスケジュールされているジョブ。
seo-title: ScheduledJob
solution: Experience Manager
title: ScheduledJob
topic: Scene7 Image Production System API
uuid: cf0db523-2138-48c6-abbd-460a961e7de1
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 4%

---


# ScheduledJob{#scheduledjob}

実行がスケジュールされているジョブ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 会社ハンドル |
| ` *`jobHandle`*` | `xsd:string` | スケジュール済みのジョブハンドル。 |
| ` *`name`*` | `xsd:string` | ジョブ名. |
| ` *`originalName`*` | `xsd:string` | スケジュール済みジョブの元の名前。 |
| ` *`type`*` | `xsd:string` | ジョブの種類。 |
| ` *`submitUserEmail`*` | `xsd:string` | ジョブをスケジュールしたユーザーの電子メールアドレス。 |
| ` *`locale`*` | `xsd:string` | ジョブログの詳細と電子メールローカライゼーションに使用するロケールです。 ロケールはで指定 `<language_code>[- <country_code>]`します。言語コードはISO-639で指定された小文字、2文字のコードはISO-3166で指定された大文字、2文字のコードはオプションの国コードです。 例えば、英語（米国）のロケール文字列は次のようになります。 `en-US`. |
| ` *`description`*` | `xsd:string` | に最初に指定されたジョブの説明で `submitJob`す。 |
| ` *`execSchedule`*` | `xsd:string` | ジョブの実行がスケジュールされている場合。 |
| ` *`nextFireTime`*` | `xsd:dateTime` | ジョブを実行する日付、時刻、およびタイムゾーン。 |
| ` *`timeZone`*` | `xsd:dateTime` | スケジュールされたジョブのタイムゾーン。 |
| ` *`triggerState`*` | `xsd:int` | ジョブトリガー状態の選択。 |
| ` *`imageServingPublishJob`*` | `types:ImageServingPublishJob` | 画像サービング公開ジョブのジョブの詳細。 |
| ` *`imageServingRenderJob`*` | `types:ImageServingRenderJob` | 画像レンダリングジョブのジョブの詳細。 |
| ` *`videoPublishJob`*` | `types:VideoPublishJob` | ビデオ公開ジョブのジョブの詳細。 VideoPublishJobを参照して [ください](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)。 |
| ` *`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | サーバーディレクトリ公開ジョブのジョブの詳細。 |
| ` *`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | アップロードディレクトリジョブのジョブの詳細。 |
| ` *`uploadUrlsJob`*` | `types:UploadUrlsJob` | アップロードURLジョブのジョブの詳細。 |
| ` *`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| ` *`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| ` *`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| ` *`exportJob`*` | `types:ExportJob` | 以前にアップロードされたファイルの承認されたエクスポートを許可します。 詳しくは、 [ジョブの書き出し](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)を参照してください。 |

## 説明 {#section-34ec157f281f412f9f0f6e861e6ed0cd}

でジョブタイプの値を指定すると `submitJob`、そのタイプに基づくジョブが返されます。 次のジョブを返すことができます。

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

