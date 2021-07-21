---
description: 実行がスケジュールされているジョブ。
solution: Experience Manager
title: ScheduledJob
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 4%

---

# ScheduledJob{#scheduledjob}

実行がスケジュールされているジョブ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 会社の担当。 |
| `*`jobHandle`*` | `xsd:string` | スケジュール済みジョブの処理。 |
| `*`name`*` | `xsd:string` | ジョブ名. |
| `*`originalName`*` | `xsd:string` | スケジュール済みジョブの元の名前。 |
| `*`type`*` | `xsd:string` | ジョブタイプ。 |
| `*`submitUserEmail`*` | `xsd:string` | ジョブをスケジュールしたユーザーの電子メールアドレス。 |
| `*`locale`*` | `xsd:string` | ジョブログの詳細と電子メールのローカライゼーションに使用するロケールです。 ロケールは`<language_code>[- <country_code>]`と指定し、言語コードはISO-639で指定された小文字、2文字のコードで、オプションの国コードはISO-3166で指定された大文字、2文字のコードです。 例えば、英語（米国）のロケール文字列は次のようになります。`en-US`. |
| `*`説明`*` | `xsd:string` | `submitJob`で最初に指定されたジョブの説明。 |
| `*`execSchedule`*` | `xsd:string` | ジョブの実行がスケジュールされている場合。 |
| `*`nextFireTime`*` | `xsd:dateTime` | ジョブが実行される日付、時刻およびタイムゾーン。 |
| `*`timeZone`*` | `xsd:dateTime` | スケジュール済みジョブのタイムゾーン。 |
| `*`triggerState`*` | `xsd:int` | ジョブのトリガー状態の選択。 |
| `*`imageServingPublishJob`*` | `types:ImageServingPublishJob` | 画像サービング公開ジョブのジョブの詳細。 |
| `*`imageServingRenderJob`*` | `types:ImageServingRenderJob` | 画像レンダリングジョブのジョブの詳細。 |
| `*`videoPublishJob`*` | `types:VideoPublishJob` | ビデオ公開ジョブのジョブの詳細。 [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)を参照してください。 |
| `*`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | サーバーディレクトリ公開ジョブのジョブの詳細。 |
| `*`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | アップロードディレクトリジョブのジョブの詳細。 |
| `*`uploadUrlsJob`*` | `types:UploadUrlsJob` | アップロードURLジョブのジョブの詳細。 |
| `*`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| `*`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| `*`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| `*`exportJob`*` | `types:ExportJob` | 以前にアップロードしたファイルの承認済み書き出しを許可する。 [Export Job](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)を参照してください。 |

## 説明 {#section-34ec157f281f412f9f0f6e861e6ed0cd}

`submitJob`にジョブタイプ値を指定すると、そのタイプに基づいてジョブが返されます。 次のジョブを返すことができます。

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
