---
description: 実行がスケジュールされているジョブ。
solution: Experience Manager
title: ScheduledJob
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 4%

---


# ScheduledJob{#scheduledjob}

実行がスケジュールされているジョブ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 会社ハンドル |
| `*`jobHandle`*` | `xsd:string` | スケジュール済みのジョブハンドル。 |
| `*`name`*` | `xsd:string` | ジョブ名. |
| `*`originalName`*` | `xsd:string` | スケジュール済みジョブの元の名前。 |
| `*`type`*` | `xsd:string` | ジョブの種類。 |
| `*`submitUserEmail`*` | `xsd:string` | ジョブをスケジュールしたユーザーの電子メールアドレス。 |
| `*`locale`*` | `xsd:string` | ジョブログの詳細と電子メールローカライゼーションに使用するロケールです。 ロケールは`<language_code>[- <country_code>]`に指定します。言語コードはISO-639で指定された小文字の2文字のコードで、オプションの国コードはISO-3166で指定された大文字の2文字のコードです。 例えば、英語（米国）のロケール文字列は次のようになります。`en-US`. |
| `*`description`*` | `xsd:string` | `submitJob`で最初に指定されたジョブの説明。 |
| `*`execSchedule`*` | `xsd:string` | ジョブの実行がスケジュールされている場合。 |
| `*`nextFireTime`*` | `xsd:dateTime` | ジョブを実行する日付、時刻、およびタイムゾーン。 |
| `*`timeZone`*` | `xsd:dateTime` | スケジュールされたジョブのタイムゾーン。 |
| `*`triggerState`*` | `xsd:int` | ジョブトリガー状態の選択。 |
| `*`imageServingPublishJob`*` | `types:ImageServingPublishJob` | 画像サービング公開ジョブのジョブの詳細。 |
| `*`imageServingRenderJob`*` | `types:ImageServingRenderJob` | 画像レンダリングジョブのジョブの詳細。 |
| `*`videoPublishJob`*` | `types:VideoPublishJob` | ビデオ公開ジョブのジョブの詳細。 [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)を参照してください。 |
| `*`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | サーバーディレクトリ公開ジョブのジョブの詳細。 |
| `*`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | アップロードディレクトリジョブのジョブの詳細。 |
| `*`uploadUrlsJob`*` | `types:UploadUrlsJob` | アップロードURLジョブのジョブの詳細。 |
| `*`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| `*`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| `*`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| `*`exportJob`*` | `types:ExportJob` | 以前にアップロードされたファイルの承認されたエクスポートを許可します。 「[ジョブの書き出し](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)」を参照してください。 |

## 説明 {#section-34ec157f281f412f9f0f6e861e6ed0cd}

`submitJob`でジョブタイプの値を指定すると、その種類に基づくジョブが返されます。 次のジョブを返すことができます。

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

