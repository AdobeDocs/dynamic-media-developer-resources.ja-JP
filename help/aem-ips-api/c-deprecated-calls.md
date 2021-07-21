---
title: 非推奨の呼び出し
description: 画像実稼動システムのAPI呼び出しと、Dynamic Mediaで使用されなくなった関連パラメーター。
solution: Experience Manager
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# 非推奨の呼び出し{#deprecated-calls}

画像実稼動システムのAPI呼び出しと、使用されなくなった関連パラメーター。

## 非推奨の呼び出し {#topic-654c0466e6434fe4a95953322255b08c}

画像実稼動システムのAPI呼び出しと、Dynamic Mediaで使用されなくなった関連パラメーター。

* `addMediaPortalEvent` - Operationsで非推奨（廃止予定）となりました。この呼び出しを使用して、Media PortalイベントをIPSに追加できます。
* `getMediaPortalEvent` - Operationsで非推奨（廃止予定）となりました。この呼び出しにより、指定した条件に一致するメディアポータルイベントを取得できます。
* `getCdnCacheInvalidationStatus` - Operationsで非推奨（廃止予定）となりました。`cdnCacheInvalidation` APIはキャッシュをほぼ即座に無効化する（約5秒）ので、このAPIは非推奨（廃止予定）となりました。 そのため、無効化ステータスのポーリングは不要になりました。
