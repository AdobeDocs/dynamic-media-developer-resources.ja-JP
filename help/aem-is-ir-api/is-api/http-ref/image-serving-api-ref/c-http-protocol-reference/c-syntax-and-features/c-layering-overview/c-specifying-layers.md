---
description: URL またはカタログ修飾子のコマンド シーケンスでは、画層定義シーケンスは layer= コマンドで開始し、別の layer= コマンド、effect= コマンド、または URL の末尾で終了します。
solution: Experience Manager
title: レイヤーの指定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# レイヤーの指定{#specifying-layers}

URL または catalog::Modifier コマンド シーケンスでは、画層定義シーケンスは layer= コマンドで開始し、別の layer= コマンド、effect= コマンド、または URL の末尾で終了します。

画層定義シーケンス内のすべてのコマンドは、画層に関連付けられます。

`layer=` コマンドは、レイヤ番号を指定します。レイヤ番号は 0 以上の整数にする必要があります。 同じレイヤ番号を持つレイヤ定義シーケンスのすべてのコマンドは、同じレイヤに適用されます。 同じコマンドが複数回発生した場合は、最後のインスタンスが優先されます。
