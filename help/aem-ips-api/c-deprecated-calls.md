---
title: 非推奨の呼び出し
description: 画像実稼動システム API 呼び出しと、Dynamic Mediaで使用またはサポートされなくなった関連パラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# 非推奨の呼び出し{#deprecated-calls}

画像実稼動システム API 呼び出しと、それに関連する、使用されなくなったパラメーター。

## 非推奨の呼び出し {#topic-654c0466e6434fe4a95953322255b08c}

画像実稼動システム API 呼び出しと、Dynamic Mediaで使用されなくなった関連パラメーター。

* `ExcludeMasterVideoFromAVS`  — 非推奨 [データタイプ](/help/aem-ips-api/types/c-data-types/c-data-types.md). このパラメーターは、プライマリビデオをアダプティブビデオセットから除外します。
   >[!IMPORTANT]
   >
   >Adobeは、2022 年 9 月 1 日にこのパラメーターのサポートを終了します。 関連トピック [ExcludeMasterVideoFromAVS](/help/aem-ips-api/types/c-data-types/r-exclude-master-video-from-avs.md).
* `addMediaPortalEvent`  — 非推奨 [運用](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). このパラメーターを使用すると、Media Portal イベントを IPS に追加できます。
* `getMediaPortalEvent`  — 非推奨 [運用](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). このパラメーターを使用すると、指定した条件に一致する Media Portal イベントを取得できます。
* `getCdnCacheInvalidationStatus`  — 非推奨 [運用](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). このパラメーターは、現在は非推奨 ( `cdnCacheInvalidation` パラメーターは、キャッシュをほぼ直ちに無効化します（約 5 秒）。 したがって、無効化ステータスに対するポーリングは不要になりました。
