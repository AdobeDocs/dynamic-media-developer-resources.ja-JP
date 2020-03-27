---
description: 画像レイヤー変換の手順2は、サムネールに対して次のように変更されます（例：req=tmb）。
seo-description: 画像レイヤー変換の手順2は、サムネールに対して次のように変更されます（例：req=tmb）。
seo-title: サムネールの拡大縮小
solution: Experience Manager
title: サムネールの拡大縮小
topic: Scene7 Image Serving - Image Rendering API
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# サムネールの拡大縮小{#thumbnail-scaling}

画像レイヤー変換の手順2は、サムネールに対して次のように変更されます（例：req=tmb）。

* `2.` を指定 `size=` した場合、サムネールの規則を使用して（切り抜いた）画像を `size=` 長方形に合わせます。 を指定 `size=` しない場合、拡大・縮小、また `res=``res=` は指定しない場合は、以下に示すサムネールの規則を使用して（切り抜いた）画像をカンバスレクトに合わせます。

