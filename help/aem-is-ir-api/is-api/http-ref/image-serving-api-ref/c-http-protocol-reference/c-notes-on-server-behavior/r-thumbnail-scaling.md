---
description: 画像レイヤー変換の手順2は、サムネールに対して次のように変更します（req=tmbの場合）。
solution: Experience Manager
title: サムネールの拡大縮小
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# サムネールの拡大/縮小{#thumbnail-scaling}

画像レイヤー変換の手順2は、サムネールに対して次のように変更します（req=tmbの場合）。

* `2.` 指定 `size=` した場合、サムネールの規則を使用して、（切り抜いた）画像を `size=` rectに合わせます。`size=`を指定しない場合は`res=`に基づいて拡大縮小します。`res=`を指定しない場合は、以下に示すサムネール規則を使用して（切り抜かれた）画像をカンバスレクトに合わせます。

