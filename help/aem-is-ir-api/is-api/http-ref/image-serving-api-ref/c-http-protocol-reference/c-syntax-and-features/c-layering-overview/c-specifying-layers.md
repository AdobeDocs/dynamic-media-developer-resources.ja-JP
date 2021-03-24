---
description: URLまたはカタログ修飾子コマンドシーケンスでは、layer=コマンドを使用してレイヤー定義シーケンス開始を行い、他のlayer=コマンド、effect=コマンドまたはURLの末尾で終了します。
solution: Experience Manager
title: レイヤーの指定
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# レイヤーの指定{#specifying-layers}

URLまたはcatalog::Modifierコマンドシーケンスで、layer=コマンドを使用してレイヤー定義シーケンス開始を終了し、別のlayer=コマンド、effect=コマンドまたはURLの末尾で終了します。

画層定義シーケンス内のすべてのコマンドが画層に関連付けられます。

`layer=`コマンドはレイヤー番号を指定します。0以上の整数である必要があります。 同じレイヤ番号を持つレイヤ定義シーケンス内のすべてのコマンドが、同じレイヤに適用されます。 同じコマンドが複数回発生した場合は、最後のインスタンスが使用されます。
