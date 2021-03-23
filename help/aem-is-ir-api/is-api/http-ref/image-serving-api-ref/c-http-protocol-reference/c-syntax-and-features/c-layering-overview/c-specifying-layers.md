---
description: URLまたはカタログ修飾子コマンドシーケンスでは、layer=コマンドを使用してレイヤー定義シーケンス開始を行い、他のlayer=コマンド、effect=コマンドまたはURLの末尾で終了します。
seo-description: URLまたはカタログ修飾子コマンドシーケンスでは、layer=コマンドを使用してレイヤー定義シーケンス開始を行い、他のlayer=コマンド、effect=コマンドまたはURLの末尾で終了します。
seo-title: レイヤーの指定
solution: Experience Manager
title: レイヤーの指定
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# レイヤーの指定{#specifying-layers}

URLまたはcatalog::Modifierコマンドシーケンスで、layer=コマンドを使用してレイヤー定義シーケンス開始を終了し、別のlayer=コマンド、effect=コマンドまたはURLの末尾で終了します。

画層定義シーケンス内のすべてのコマンドが画層に関連付けられます。

`layer=`コマンドはレイヤー番号を指定します。0以上の整数である必要があります。 同じレイヤ番号を持つレイヤ定義シーケンス内のすべてのコマンドが、同じレイヤに適用されます。 同じコマンドが複数回発生した場合は、最後のインスタンスが使用されます。
