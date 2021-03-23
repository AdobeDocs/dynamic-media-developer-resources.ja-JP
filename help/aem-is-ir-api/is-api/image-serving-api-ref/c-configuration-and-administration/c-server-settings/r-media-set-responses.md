---
description: この節の設定は、req=set修飾子で取得されたメディアセット応答に適用されます。
seo-description: この節の設定は、req=set修飾子で取得されたメディアセット応答に適用されます。
seo-title: メディアセットの応答
solution: Experience Manager
title: メディアセットの応答
uuid: 9fa6a38a-cd1f-499b-a2b6-e1a9a6c69ed0
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# メディアセット応答{#media-set-responses}

この節の設定は、req=set修飾子で取得されたメディアセット応答に適用されます。

## PS::fvctx.useCatalogRecordValidation — キャッシュポリシー{#section-9accb087d16548a988993bb30395a6f6}

このプロパティは、キャッシュから取得された応答を再生成する必要があるかどうかを判断する際のキャッシュポリシーを制御します。 プロパティが無効の場合、[!DNL catalog.ini]ファイルのタイムスタンプが検証に使用されます。 プロパティが有効な場合、参照されるすべてのレコードの最新の`catalog::LastModified`タイムスタンプが検証に使用されます。

## PS::fvctx.nestingLimit — ネストの制限{#section-280210341f1647fea02590e7069934d2}

`req=set`応答の最大入れ子深さです。 この深さを超えると、エラーが返されます。

## PS::fvctx.brochureLimit — パンフレットの制限{#section-fe36e47db49244cea7f07e9dd3639440}

`req=set`応答内のeカタログパンフレットの最大数です。この中にすべての関連メタデータが含まれています。 この制限を超えると、パンフレット項目に関連付けられたプライベートマップおよびユーザデータは表示されなくなります。
