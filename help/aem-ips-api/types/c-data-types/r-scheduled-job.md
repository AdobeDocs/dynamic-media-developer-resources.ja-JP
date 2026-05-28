---
description: 実行予定のジョブ。
solution: Experience Manager
title: ScheduledJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
TQID: 'https://experienceleague.adobe.com/OFG30nHlkuRT7HeNob0hkEfaygi8b2gNFEiu67LJBmU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 276
ht-degree: 3%

---

# [!DNL ScheduledJob]{#scheduledjob}

実行予定のジョブ。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| companyHandle | `xsd:string` | 会社のハンドル。 |
| jobHandle | `xsd:string` | スケジュールされたジョブハンドル： |
| name | `xsd:string` | ジョブ名： |
| originalName | `xsd:string` | スケジュールされたジョブの元の名前。 |
| タイプ | `xsd:string` | ジョブタイプ： |
| submitUserEmail | `xsd:string` | ジョブをスケジュールしたユーザーの電子メールアドレス。 |
| ロケール | `xsd:string` | ジョブのログの詳細と電子メールのローカライズに使用するロケール。 ロケールは`<language_code>[- <country_code>]`として指定されます。言語コードはISO-639で指定された小文字の2文字コードで、オプションの国コードはISO-3166で指定された大文字の2文字コードです。 例えば、英語（米国）のロケール文字列は`en-US`になります。 |
| description | `xsd:string` | 最初に`submitJob`で指定されたジョブの説明。 |
| execSchedule | `xsd:string` | ジョブが実行スケジュールされている場合。 |
| nextFireTime | `xsd:dateTime` | ジョブが実行された日付、時刻、タイムゾーン。 |
| timeZone | `xsd:dateTime` | スケジュールされたジョブのタイムゾーン。 |
| triggerState | `xsd:int` | ジョブトリガーの状態を選択します。 |
| imageServingPublishJob | `types:ImageServingPublishJob` | 画像サービング公開ジョブのジョブの詳細。 |
| imageServingRenderJob | `types:ImageServingRenderJob` | 画像レンダリングジョブのジョブ詳細。 |
| videoPublishJob | `types:VideoPublishJob` | ビデオ公開ジョブのジョブ詳細。 [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)を参照してください。 |
| serverDirectoryPublishJob | `types:ServerDirectoryPublishJob` | サーバーディレクトリ公開ジョブのジョブ詳細。 |
| uploadDirectoryJob | `types:UploadDirectoryJob` | アップロードディレクトリジョブのジョブ詳細。 |
| uploadUrlsJob | `types:UploadUrlsJob` | アップロード URL ジョブのジョブ詳細。 |
| optimizeImagesJob | `types:OptimizeImagesJob` | |
| ripPdfsJob | `types:RipPdfsJob` | |
| reprocessAssetsJob | `types:ReprocessAssetsJob` | |
| exportJob | `types:ExportJob` | 以前アップロードしたファイルの許可された書き出しを許可します。 [ ジョブのエクスポート ](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)を参照してください。 |

## 説明 {#section-34ec157f281f412f9f0f6e861e6ed0cd}

`submitJob`でジョブタイプの値を指定すると、そのタイプに基づいてジョブが返されます。 次のジョブを返すことができます。

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
