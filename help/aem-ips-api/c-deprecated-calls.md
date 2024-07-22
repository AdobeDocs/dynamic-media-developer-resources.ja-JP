---
title: 非推奨の呼び出し
description: 画像実稼働システムの API 呼び出しと、 [!DNL Dynamic Media] で使用またはサポートされなくなった関連パラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# 非推奨の呼び出し{#deprecated-calls}

画像実稼働システムの API 呼び出しおよび関連するパラメーター（使用されなくなった）。

## 非推奨の呼び出し {#topic-654c0466e6434fe4a95953322255b08c}

画像実稼働システムの API 呼び出しと、[!DNL Dynamic Media] で使用されなくなった関連パラメーター。

* `ExcludeMasterVideoFromAVS` - [ データタイプ ](/help/aem-ips-api/types/c-data-types/c-data-types.md) から非推奨（廃止予定）。 このパラメーターにより、プライマリビデオがアダプティブビデオセットから除外されます。<!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - [ 操作 ](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md) から非推奨（廃止予定）になりました。 このパラメーターを使用すると、IPS にメディアポータルイベントを追加できます。
* `getMediaPortalEvent` - [ 操作 ](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md) から非推奨（廃止予定）になりました。 このパラメーターを使用すると、指定した条件に一致するメディアポータルイベントを取得できます。
* `getCdnCacheInvalidationStatus` - [ 操作 ](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md) から非推奨（廃止予定）になりました。 `cdnCacheInvalidation` パラメーターによってキャッシュがほぼ直ちに（約 5 秒）無効化されるので、このパラメーターは非推奨（廃止予定）になりました。 したがって、無効化ステータスのポーリングは不要になりました。
