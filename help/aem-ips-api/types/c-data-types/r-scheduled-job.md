---
description: 実行スケジュールが設定されたジョブ。
solution: Experience Manager
title: ScheduledJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 3%

---

# [!DNL ScheduledJob]{#scheduledjob}

実行スケジュールが設定されたジョブ。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| companyHandle | `xsd:string` | 会社ハンドル。 |
| jobHandle | `xsd:string` | スケジュールされたジョブハンドル。 |
| name | `xsd:string` | ジョブ名。 |
| originalName | `xsd:string` | スケジュールされたジョブの元の名前。 |
| タイプ | `xsd:string` | ジョブタイプ。 |
| submitUserEmail | `xsd:string` | ジョブをスケジュールしたユーザーのメールアドレス。 |
| ロケール | `xsd:string` | ジョブ ログの詳細および電子メール ローカリゼーションに使用されるロケールです。 ロケールは `<language_code>[- <country_code>]` として指定します。言語コードは ISO-639 で指定された小文字 2 文字のコードで、オプションの国コードは ISO-3166 で指定された大文字 2 文字のコードです。 例えば、英語（米国）のロケール文字列は `en-US` になります。 |
| description | `xsd:string` | `submitJob` で最初に指定されたジョブの説明。 |
| execSchedule | `xsd:string` | ジョブの実行がスケジュールされている場合。 |
| nextFireTime | `xsd:dateTime` | ジョブが実行される日付、時刻、およびタイムゾーンです。 |
| timeZone | `xsd:dateTime` | スケジュールされたジョブのタイムゾーン。 |
| triggerState | `xsd:int` | ジョブトリガーの状態の選択。 |
| imageServingPublishJob | `types:ImageServingPublishJob` | 画像サービング公開ジョブの詳細。 |
| imageServingRenderJob | `types:ImageServingRenderJob` | 画像レンダリングジョブのジョブ詳細。 |
| videoPublishJob | `types:VideoPublishJob` | ビデオ公開ジョブのジョブの詳細。 [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html?lang=ja) を参照してください。 |
| serverDirectoryPublishJob | `types:ServerDirectoryPublishJob` | サーバーディレクトリ公開ジョブのジョブの詳細。 |
| uploadDirectoryJob | `types:UploadDirectoryJob` | ディレクトリのアップロードジョブのジョブの詳細。 |
| uploadUrlsJob | `types:UploadUrlsJob` | アップロード URL ジョブのジョブの詳細。 |
| optimizeImagesJob | `types:OptimizeImagesJob` | |
| ripPdfsJob | `types:RipPdfsJob` | |
| reprocessAssetsJob | `types:ReprocessAssetsJob` | |
| exportJob | `types:ExportJob` | 以前にアップロードしたファイルの承認済みエクスポートを許可します。 [ エクスポートジョブ ](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html?lang=ja) を参照してください。 |

## 説明 {#section-34ec157f281f412f9f0f6e861e6ed0cd}

`submitJob` でジョブタイプの値を指定すると、そのタイプに基づいてジョブが返されます。 次のジョブを返すことができます。

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
