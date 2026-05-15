---
title: サムネールの拡大・縮小
description: 画像レイヤーの変形の手順2は、サムネールの場合（req=tmbの場合）に次のように変更されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
TQID: 'https://experienceleague.adobe.com/He10BtjrEIOQW6SZcaUhcExDjP05BR-pc3BCj9TRawU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 79
ht-degree: 0%

---

# サムネールの拡大・縮小{#thumbnail-scaling}

画像レイヤーの変形の手順2は、サムネールの場合（req=tmbの場合）に次のように変更されます。

* `2.` `size=`が指定されている場合は、サムネールールを使用して、（切り抜かれた）画像を`size=`長方形に収めます。 `size=`が指定されていない場合は、`res=`に基づいて拡大・縮小するか、`res=`が指定されていない場合は、以下に示すサムネール規則を使用して、カンバスの長方形に（切り抜かれた）画像を収めます。
