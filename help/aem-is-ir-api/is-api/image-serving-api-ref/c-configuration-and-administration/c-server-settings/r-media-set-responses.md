---
description: この節の設定は、 req=set修飾子で取得されたメディアセット応答に適用されます。
solution: Experience Manager
title: メディアセットの応答
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# メディアセットの応答{#media-set-responses}

この節の設定は、 req=set修飾子で取得されたメディアセット応答に適用されます。

## PS::fvctx.useCatalogRecordValidation — キャッシュポリシー {#section-9accb087d16548a988993bb30395a6f6}

このプロパティは、キャッシュから取得した応答を再生成する必要があるかどうかを決定する際に、キャッシュポリシーを制御します。 プロパティが無効になっている場合、[!DNL catalog.ini]ファイルのタイムスタンプが検証に使用されます。 プロパティが有効な場合、参照されているすべてのレコードの最新の`catalog::LastModified`タイムスタンプが検証に使用されます。

## PS::fvctx.nestingLimit — ネストの制限 {#section-280210341f1647fea02590e7069934d2}

`req=set`応答のネストの最大深さ。 この深さを超えると、エラーが返されます。

## PS::fvctx.brochureLimit — パンフレットの制限 {#section-fe36e47db49244cea7f07e9dd3639440}

`req=set`応答内のeカタログパンフレットの最大数。関連するメタデータがすべて含まれます。 この制限を超えると、パンフレットアイテムに関連付けられたプライベートマップおよびユーザデータは表示されなくなります。
