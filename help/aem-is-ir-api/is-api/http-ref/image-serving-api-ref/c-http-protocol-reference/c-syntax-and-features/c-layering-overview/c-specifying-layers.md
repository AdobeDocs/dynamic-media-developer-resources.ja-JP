---
description: URLまたはカタログ修飾子のコマンドシーケンスでは、レイヤー定義シーケンスはlayer=コマンドで始まり、別のlayer=コマンド、effect=コマンドまたはURLの終わりで終わります。
seo-description: URLまたはカタログ修飾子のコマンドシーケンスでは、レイヤー定義シーケンスはlayer=コマンドで始まり、別のlayer=コマンド、effect=コマンドまたはURLの終わりで終わります。
seo-title: レイヤーの指定
solution: Experience Manager
title: レイヤーの指定
topic: Scene7 Image Serving - Image Rendering API
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# レイヤーの指定{#specifying-layers}

URLまたはcatalog::Modifierコマンドシーケンスでは、レイヤー定義シーケンスはlayer=コマンドで始まり、別のlayer=コマンド、effect=コマンドまたはURLの終わりで終わります。

画層定義シーケンス内のすべてのコマンドが画層に関連付けられます。

このコ `layer=` マンドでは、0以上の整数のレイヤー番号を指定します。 同じレイヤ番号を持つレイヤ定義シーケンス内のすべてのコマンドが、同じレイヤに適用されます。 同じコマンドが複数回発生した場合は、最後のインスタンスが使用されます。
