---
description: この節の設定は、req=set修飾子で取得されたメディアセット応答に適用されます。
solution: Experience Manager
title: メディアセットの応答
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '155'
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
