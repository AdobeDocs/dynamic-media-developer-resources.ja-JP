---
title: 非推奨の呼び出し
description: Image Production System API呼び出しと、Dynamic Mediaで使用されなくなった関連パラメーター。
solution: Experience Manager
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# 非推奨の呼び出し{#deprecated-calls}

Image Production System API呼び出しと、使用されなくなった関連パラメーター。

## 非推奨の呼び出し{#topic-654c0466e6434fe4a95953322255b08c}

Image Production System API呼び出しと、Dynamic Mediaで使用されなくなった関連パラメーター。

* `addMediaPortalEvent` - Operationsから廃止。この呼び出しにより、Media PortalイベントをIPSに追加できます。
* `getMediaPortalEvent` - Operationsから廃止。この呼び出しにより、指定した条件に一致するMedia Portalイベントを取得できます。
* `getCdnCacheInvalidationStatus` - Operationsから廃止。`cdnCacheInvalidation` APIはキャッシュをほぼすぐに無効にする（～5秒）ので、このAPIは非推奨となりました。 したがって、無効状態のポーリングは不要になります。

