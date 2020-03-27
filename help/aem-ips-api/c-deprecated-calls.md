---
description: Image Production System API呼び出しと、使用されなくなった関連パラメーター。
seo-description: Image Production System API呼び出しと、使用されなくなった関連パラメーター。
seo-title: 非推奨の呼び出し
solution: Experience Manager
title: 非推奨の呼び出し
topic: Scene7 Image Production System API
uuid: 03925728-f011-45f0-84a6-808dff0fd529
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 非推奨の呼び出し{#deprecated-calls}

Image Production System API呼び出しと、使用されなくなった関連パラメーター。

## 非推奨の呼び出し {#topic-654c0466e6434fe4a95953322255b08c}

Image Production System API呼び出しと、使用されなくなった関連パラメーター。

* `addMediaPortalEvent` - Operationsから廃止されました。 この呼び出しにより、Media PortalイベントをIPSに追加できます。
* `getMediaPortalEvent` - Operationsから廃止されました。 この呼び出しにより、指定した条件に一致するMedia Portalイベントを取得できます。
* `getCdnCacheInvalidationStatus` - Operationsから廃止されました。 このAPIは、APIがキャッシュをほぼ直ちに無効にするので、非推奨となりました( `cdnCacheInvalidation` 約5秒)。 したがって、無効化ステータスのポーリングは不要になりました。

