---
description: 画像レイヤー変換の手順2は、サムネールに対して次のように変更します（req=tmbの場合）。
seo-description: 画像レイヤー変換の手順2は、サムネールに対して次のように変更します（req=tmbの場合）。
seo-title: サムネールの拡大縮小
solution: Experience Manager
title: サムネールの拡大縮小
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# サムネールの拡大/縮小{#thumbnail-scaling}

画像レイヤー変換の手順2は、サムネールに対して次のように変更します（req=tmbの場合）。

* `2.` 指定 `size=` した場合、サムネールの規則を使用して、（切り抜いた）画像を `size=` rectに合わせます。`size=`を指定しない場合は`res=`に基づいて拡大縮小します。`res=`を指定しない場合は、以下に示すサムネール規則を使用して（切り抜かれた）画像をカンバスレクトに合わせます。

