---
title: サムネールの拡大縮小
description: 画像レイヤー変換の手順 2 は、サムネール（つまり、req=tmb）に対して次のように変更されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# サムネールの拡大縮小{#thumbnail-scaling}

画像レイヤー変換の手順 2 は、サムネール（つまり、req=tmb）に対して次のように変更されます。

* `2.` `size=` を指定した場合は、サムネールルールを使用して（切り抜いた）画像を `size=` rect 内に収めます。 `size=` が指定されていない場合は、`res=` に基づいた拡大縮小、`res=` が指定されていない場合は、以下に示すサムネールルールを使用して、（切り抜かれた）画像を canvas rect に収めます。
