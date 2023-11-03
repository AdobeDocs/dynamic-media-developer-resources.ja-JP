---
description: URL またはカタログモディファイヤのコマンドシーケンスでは、レイヤ定義シーケンスは layer=コマンドで始まり、別の layer=コマンド、effect=コマンド、または URL の末尾で終わります。
solution: Experience Manager
title: レイヤーの指定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# レイヤーの指定{#specifying-layers}

URL または catalog::Modifier コマンドシーケンスでは、レイヤ定義シーケンスは layer=コマンドで始まり、別の layer=コマンド、effect=コマンド、または URL の終わりで終わります。

画層定義シーケンス内のすべてのコマンドは、画層に関連付けられます。

The `layer=` コマンドは、0 以上の整数で指定する必要がある画層番号を指定します。 同じ画層番号を持つ画層定義シーケンス内のすべてのコマンドが、同じ画層に適用されます。 同じコマンドが複数回発生した場合は、最後のインスタンスが優先されます。
