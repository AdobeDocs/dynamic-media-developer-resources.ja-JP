---
title: 非推奨の呼び出し
description: Image Production System API呼び出しと、 [!DNL Dynamic Media]で使用またはサポートされなくなった関連パラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
autotag-review: '2026-05-13T21:03:57.183Z'
TQID: 'https://experienceleague.adobe.com/JLoyXksHQ-LAXXxfY71Dv-FOE0trpt-RzcKcV-Pv96I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 0%

---

# 非推奨の呼び出し{#deprecated-calls}

Image Production System API呼び出しと、使用されなくなった関連パラメーター。

## 非推奨の呼び出し {#topic-654c0466e6434fe4a95953322255b08c}

[!DNL Dynamic Media]で使用されなくなったImage Production System API呼び出しと関連パラメーター。

* `ExcludeMasterVideoFromAVS` - [ データタイプ ](/help/aem-ips-api/types/c-data-types/c-data-types.md)から非推奨（廃止予定）。 このパラメーターは、アダプティブビデオセットからプライマリビデオを除外しました。<!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - [操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md)から非推奨になりました。 このパラメーターを使用すると、Media Portal イベントをIPSに追加できます。
* `getMediaPortalEvent` - [操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md)から非推奨になりました。 このパラメーターを使用すると、指定した条件に一致するメディアポータルのイベントを取得できます。
* `getCdnCacheInvalidationStatus` - [操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md)から非推奨になりました。 このパラメーターは、ほぼ即時（約5秒）に`cdnCacheInvalidation` パラメーターでキャッシュが無効になるため、現在は非推奨です。 そのため、無効化ステータスのポーリングは不要になりました。

