---
description: URLまたはカタログモディファイヤのコマンドシーケンスでは、レイヤ定義シーケンスはlayer=コマンドで始まり、別のlayer=コマンド、effect=コマンド、またはURLの終わりで終わります。
solution: Experience Manager
title: レイヤーの指定
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# レイヤーの指定{#specifying-layers}

URLまたはcatalog::Modifierコマンドシーケンスでは、レイヤ定義シーケンスはlayer=コマンドで始まり、別のlayer=コマンド、effect=コマンド、またはURLの終わりで終わります。

画層定義シーケンス内のすべてのコマンドは、画層に関連付けられます。

`layer=`コマンドは、0以上の整数のレイヤー番号を指定します。 同じ画層番号を持つ画層定義シーケンス内のすべてのコマンドが、同じ画層に適用されます。 同じコマンドが複数回発生した場合は、最後のインスタンスが優先されます。
