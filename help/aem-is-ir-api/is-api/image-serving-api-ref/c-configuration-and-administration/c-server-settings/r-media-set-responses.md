---
description: この節の設定は、req=set修飾子で取得したメディアセットの応答に適用されます。
seo-description: この節の設定は、req=set修飾子で取得したメディアセットの応答に適用されます。
seo-title: メディアセットの回答
solution: Experience Manager
title: メディアセットの回答
topic: Scene7 Image Serving - Image Rendering API
uuid: 9fa6a38a-cd1f-499b-a2b6-e1a9a6c69ed0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# メディアセットの回答{#media-set-responses}

この節の設定は、req=set修飾子で取得したメディアセットの応答に適用されます。

## PS::fvctx.useCatalogRecordValidation — キャッシュポリシー {#section-9accb087d16548a988993bb30395a6f6}

このプロパティは、キャッシュから取得した設定応答を再生成する必要があるかどうかを判断する際のキャッシュポリシーを制御します。 プロパティが無効の場合、ファイルのタイムスタ [!DNL catalog.ini] ンプが検証に使用されます。 プロパティが有効な場合、参照されているすべての `catalog::LastModified` レコードの最新のタイムスタンプが検証に使用されます。

## PS::fvctx.nestingLimit — 入れ子の制限 {#section-280210341f1647fea02590e7069934d2}

任意の応答の最大入れ子の深 `req=set` さです。 この深さを超えると、エラーが返されます。

## PS::fvctx.brochureLimit — パンフレットの制限 {#section-fe36e47db49244cea7f07e9dd3639440}

すべての関連メタデータを含む、応答内のeカタロ `req=set` グパンフレットの最大数。 この制限を超えると、パンフレット項目に関連付けられたプライベートマップおよびユーザデータは表示されなくなります。
