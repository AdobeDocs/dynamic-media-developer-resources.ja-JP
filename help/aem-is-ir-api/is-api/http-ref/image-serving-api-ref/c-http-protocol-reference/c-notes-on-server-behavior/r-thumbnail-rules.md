---
description: これらのサムネールのルールに注意してください。
solution: Experience Manager
title: サムネールルール
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# サムネールルール{#thumbnail-rules}

これらのサムネールのルールに注意してください。

1. `catalog::ThumbType=Crop` の場合、（切り抜かれた）画像は、ターゲットの直角全体を覆ったまま、可能な限り小さいサイズに拡大縮小されます。 `catalog::ThumbType=Fit` の場合、（切り抜き）画像は、画像全体をターゲットの長方形に合わせたまま、可能な最大サイズに拡大または縮小されます。 `catalog::ThumbType=Texture` の場合、（切り抜かれた）画像は `catalog::ThumbRes` と `catalog::Resolution` の比率に合わせて拡大縮小されます。
1. `attribute::ThumbHorizAlign` と `attribute::ThumbVertAlign` に基づいて、スケールされた画像をターゲットの長方形に合わせます。
1. 結果をターゲットレコードに切り抜きます。
