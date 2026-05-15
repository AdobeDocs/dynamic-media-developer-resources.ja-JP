---
description: これらのサムネールールに注意してください。
solution: Experience Manager
title: サムネールール
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
TQID: 'https://experienceleague.adobe.com/2HjWzEcMFnTFzwDWz-Ld7wZ6FsFcq3gwaUFcSWgxPko'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 0%

---

# サムネールール{#thumbnail-rules}

これらのサムネールールに注意してください。

1. `catalog::ThumbType=Crop`の場合、（切り抜かれた）画像は、ターゲットの直列全体をカバーしながら、可能な限り小さなサイズに拡大・縮小されます。 `catalog::ThumbType=Fit`の場合、画像全体をターゲットの直方体に合わせながら、（切り抜かれた）画像を可能な限り大きなサイズに拡大・縮小します。 `catalog::ThumbType=Texture`の場合、（切り抜かれた）画像は`catalog::ThumbRes`から`catalog::Resolution`の比率に拡大・縮小されます。
1. `attribute::ThumbHorizAlign`と`attribute::ThumbVertAlign`に基づいて、拡大・縮小された画像をターゲットの直腸に合わせます。
1. 結果を切り抜いて、ターゲットの直流に切り抜きます。
