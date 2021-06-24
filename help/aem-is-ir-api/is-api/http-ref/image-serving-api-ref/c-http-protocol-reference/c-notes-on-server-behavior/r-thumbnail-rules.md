---
description: これらのサムネールのルールに注意してください。
solution: Experience Manager
title: サムネールのルール
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# サムネールのルール{#thumbnail-rules}

これらのサムネールのルールに注意してください。

1. `catalog::ThumbType=Crop`の場合、（切り抜かれた）画像は、ターゲットの四角全体を覆いながら、可能な限り小さいサイズに拡大/縮小されます。 `catalog::ThumbType=Fit`の場合、（切り抜かれた）画像は可能な限り大きいサイズに拡大縮小され、画像全体がターゲット領域に収まります。 `catalog::ThumbType=Texture`の場合、（切り抜かれた）画像は`catalog::ThumbRes`と`catalog::Resolution`の比率に合わせて拡大縮小されます。
1. 拡大/縮小された画像を`attribute::ThumbHorizAlign`と`attribute::ThumbVertAlign`に基づいて、ターゲットの正方向に揃えます。
1. 結果をターゲットの直角に切り抜きます。
