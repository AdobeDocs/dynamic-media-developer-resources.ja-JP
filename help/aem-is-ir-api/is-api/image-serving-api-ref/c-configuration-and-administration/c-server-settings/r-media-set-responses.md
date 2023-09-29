---
title: メディアセットの応答
description: このセクションの設定は、req=set 修飾子で取得されたメディアセット応答に適用されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# メディアセットの応答{#media-set-responses}

このセクションの設定は、 `req=set` 修飾子

## PS::fvctx.useCatalogRecordValidation — キャッシュポリシー {#section-9accb087d16548a988993bb30395a6f6}

このプロパティは、キャッシュから取得されたセット応答を再生成する必要があるかどうかを判断する際に、キャッシュポリシーを制御します。 プロパティが無効な場合、 [!DNL catalog.ini] ファイルが検証に使用されます。 プロパティが有効な場合、最新の `catalog::LastModified` すべての参照されたレコードのタイムスタンプが検証に使用されます。

## PS::fvctx.nestingLimit — ネスティング制限 {#section-280210341f1647fea02590e7069934d2}

任意の `req=set` 応答。 この深さを超えると、エラーが返されます。

## PS::fvctx.brochureLimit — パンフレットの制限 {#section-fe36e47db49244cea7f07e9dd3639440}

内の e カタログパンフレットの最大数 `req=set` 応答。関連するすべてのメタデータが含まれます。 この制限を超えると、パンフレット項目に関連付けられたプライベートマップおよびユーザデータは抑制されます。
