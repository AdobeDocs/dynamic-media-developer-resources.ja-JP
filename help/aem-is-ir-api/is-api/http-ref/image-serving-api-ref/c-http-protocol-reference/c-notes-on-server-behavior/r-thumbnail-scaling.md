---
description: 画像レイヤー変換の手順2は、サムネールの場合（req=tmbの場合）に次のように変更されます。
solution: Experience Manager
title: サムネールの拡大/縮小
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# サムネールの拡大/縮小{#thumbnail-scaling}

画像レイヤー変換の手順2は、サムネールの場合（req=tmbの場合）に次のように変更されます。

* `2.` 指定し `size=` た場合、サムネールのルールを使用して、（切り抜いた）画像を `size=` 正しい位置に合わせます。`size=`を指定しない場合は、`res=`に基づいて拡大・縮小します。`res=`を指定しない場合は、以下に示すサムネールの規則を使用して、（切り抜いた）画像をカンバスに合わせます。
