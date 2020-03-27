---
description: これらのサムネールの規則に注意してください。
seo-description: これらのサムネールの規則に注意してください。
seo-title: サムネールの規則
solution: Experience Manager
title: サムネールの規則
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# サムネールの規則{#thumbnail-rules}

これらのサムネールの規則に注意してください。

1. この場 `catalog::ThumbType=Crop`合、（切り抜かれた）画像は、ターゲットレクト全体を覆いながら、可能な限り小さいサイズに縮小されます。 この場 `catalog::ThumbType=Fit`合、（切り抜かれた）画像は、可能な限り大きいサイズに縮小され、画像全体がターゲットの長方形に合わせられます。 の場 `catalog::ThumbType=Texture`合、（切り抜かれた）画像はの比率に合わせて拡大・縮小 `catalog::ThumbRes` されま `catalog::Resolution`す。
1. とを基にして、拡大/縮小された画像をターゲットの長方形に揃 `attribute::ThumbHorizAlign` えま `attribute::ThumbVertAlign`す。
1. 結果をターゲットrectに切り抜きます。

