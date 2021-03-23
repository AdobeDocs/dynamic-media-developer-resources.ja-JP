---
description: これらのサムネールの規則に注意してください。
seo-description: これらのサムネールの規則に注意してください。
seo-title: サムネールのルール
solution: Experience Manager
title: サムネールのルール
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# サムネールの規則{#thumbnail-rules}

これらのサムネールの規則に注意してください。

1. `catalog::ThumbType=Crop`の場合、（切り抜かれた）画像は、ターゲットのrect全体を覆いながら、可能な限り小さいサイズに拡大縮小されます。 `catalog::ThumbType=Fit`の場合、（切り抜かれた）画像は、ターゲットレクトに画像全体を合わせながら、可能な限り大きいサイズに拡大縮小されます。 `catalog::ThumbType=Texture`の場合、（トリミングされた）画像は`catalog::ThumbRes`と`catalog::Resolution`の比率に合わせて拡大縮小されます。
1. `attribute::ThumbHorizAlign`と`attribute::ThumbVertAlign`に基づいて、拡大・縮小した画像をターゲットrectに揃えます。
1. 結果をターゲットrectに切り抜きます。

