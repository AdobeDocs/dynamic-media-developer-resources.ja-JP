---
title: 非推奨の呼び出し
description: 画像実稼動システム API 呼び出しと、それに関連するパラメーター（で使用またはサポートされなくなったもの） [!DNL Dynamic Media].
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# 非推奨の呼び出し{#deprecated-calls}

画像実稼動システム API 呼び出しと、それに関連する、使用されなくなったパラメーター。

## 非推奨の呼び出し {#topic-654c0466e6434fe4a95953322255b08c}

画像実稼動システム API 呼び出しと、それに関連するパラメーター ( [!DNL Dynamic Media].

* `ExcludeMasterVideoFromAVS`  — 非推奨 [データタイプ](/help/aem-ips-api/types/c-data-types/c-data-types.md). このパラメーターは、プライマリビデオをアダプティブビデオセットから除外します。 <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent`  — 非推奨 [運用](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). このパラメーターを使用すると、Media Portal イベントを IPS に追加できます。
* `getMediaPortalEvent`  — 非推奨 [運用](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). このパラメーターを使用すると、指定した条件に一致する Media Portal イベントを取得できます。
* `getCdnCacheInvalidationStatus`  — 非推奨 [運用](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). このパラメーターは、現在は非推奨 ( `cdnCacheInvalidation` パラメーターは、キャッシュをほぼ直ちに無効化します（約 5 秒）。 したがって、無効化ステータスに対するポーリングは不要になりました。
