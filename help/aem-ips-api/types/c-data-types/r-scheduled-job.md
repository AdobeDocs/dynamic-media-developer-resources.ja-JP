---
description: 実行がスケジュールされているジョブ。
solution: Experience Manager
title: ScheduledJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 4%

---

# ScheduledJob{#scheduledjob}

実行がスケジュールされているジョブ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 会社の取り扱い。 |
| `*`jobHandle`*` | `xsd:string` | スケジュール済みのジョブハンドル。 |
| `*`name`*` | `xsd:string` | ジョブ名. |
| `*`originalName`*` | `xsd:string` | スケジュール済みジョブの元の名前。 |
| `*`type`*` | `xsd:string` | ジョブタイプ。 |
| `*`submitUserEmail`*` | `xsd:string` | ジョブをスケジュールしたユーザーの電子メールアドレス。 |
| `*`locale`*` | `xsd:string` | ジョブログの詳細と電子メールのローカライゼーションに使用するロケールです。 ロケールは、 `<language_code>[- <country_code>]`（言語コードは ISO-639 で指定された小文字 2 文字のコードで、オプションの国コードは ISO-3166 で指定された大文字 2 文字のコードです）。 例えば、英語（米国）のロケール文字列は次のようになります。 `en-US`. |
| `*`説明`*` | `xsd:string` | 最初に指定されたジョブの説明 ( `submitJob`. |
| `*`execSchedule`*` | `xsd:string` | ジョブの実行がスケジュールされている場合。 |
| `*`nextFireTime`*` | `xsd:dateTime` | ジョブが実行された日付、時刻、およびタイムゾーン。 |
| `*`timeZone`*` | `xsd:dateTime` | スケジュール済みジョブのタイムゾーン。 |
| `*`triggerState`*` | `xsd:int` | ジョブのトリガー状態の選択。 |
| `*`imageServingPublishJob`*` | `types:ImageServingPublishJob` | 画像サービング公開ジョブのジョブの詳細。 |
| `*`imageServingRenderJob`*` | `types:ImageServingRenderJob` | 画像レンダリングジョブのジョブの詳細。 |
| `*`videoPublishJob`*` | `types:VideoPublishJob` | ビデオ公開ジョブのジョブの詳細。 詳しくは、 [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| `*`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | サーバーディレクトリ公開ジョブのジョブ詳細。 |
| `*`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | アップロードディレクトリジョブのジョブの詳細。 |
| `*`uploadUrlsJob`*` | `types:UploadUrlsJob` | アップロード URL ジョブのジョブ詳細。 |
| `*`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| `*`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| `*`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| `*`exportJob`*` | `types:ExportJob` | 以前にアップロードしたファイルの承認済み書き出しを許可します。 詳しくは、 [書き出しジョブ](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## 説明 {#section-34ec157f281f412f9f0f6e861e6ed0cd}

でジョブタイプの値を指定する場合 `submitJob`の場合、システムはそのタイプに基づいてジョブを返します。 次のジョブを返すことができます。

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
