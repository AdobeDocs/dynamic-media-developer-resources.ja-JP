---
title: サムネールの拡大/縮小
description: 画像レイヤー変換の手順 2 は、サムネールに対して次のように変更されます（req=tmb の場合）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# サムネールの拡大/縮小{#thumbnail-scaling}

画像レイヤー変換の手順 2 は、サムネールに対して次のように変更されます（req=tmb の場合）。

* `2.` 次の場合 `size=` が指定されている場合、（切り抜かれた）画像を `size=` サムネールのルールを使用して正しく設定します。 次の場合 `size=` が指定されていません。次に基づく尺度が指定されています： `res=`、または、 `res=` が指定されていない場合は、以下に示すサムネールルールを使用して、（切り抜いた）画像をキャンバスに合わせます。
