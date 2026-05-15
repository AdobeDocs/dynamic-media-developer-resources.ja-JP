---
description: URLまたはカタログ修飾子コマンド シーケンスでは、レイヤー定義シーケンスはlayer= コマンドで始まり、別のlayer= コマンド、effect= コマンド、またはURLの最後で終了します。
solution: Experience Manager
title: レイヤーの指定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
TQID: 'https://experienceleague.adobe.com/jNFpOYrBFWWc53JvzwENSjpM-SkIpenxxWPUgGX-p0Q'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 0%

---

# レイヤーの指定{#specifying-layers}

URLまたはcatalog::Modifier コマンドシーケンスでは、レイヤー定義シーケンスはlayer= コマンドで始まり、別のlayer= コマンド、effect= コマンド、またはURLの最後で終了します。

レイヤー定義シーケンス内のすべてのコマンドは、レイヤーに関連付けられます。

`layer=` コマンドは、レイヤー番号を指定します。レイヤー番号は0以上の整数である必要があります。 同じレイヤー番号を持つレイヤー定義シーケンスのすべてのコマンドが、同じレイヤーに適用されます。 同じコマンドが複数回実行された場合は、最後のインスタンスが優先されます。
