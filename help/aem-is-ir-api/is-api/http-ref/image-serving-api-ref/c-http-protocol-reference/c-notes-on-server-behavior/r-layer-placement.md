---
title: レイヤーの配置
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
TQID: https://experienceleague.adobe.com/SMf4V0AmxYIi0o0FZhMkRx9pprIxjJjEcCWT2agF1Bo
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 0f5947b3f28ba40cd479df463c843f7e99155d5e
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 0%

---

# レイヤーの配置{#layer-placement}

レイヤーは、レイヤーの原点（origin=）と背景レイヤーの原点をpos=で指定されたオフセットに揃えることで配置されます。

レイヤーの原点が画像レイヤーに明示的に指定されていない場合、次のように計算されます。

1. 画像のアンカーを決定します。 `anchor=`を使用するか、指定されていない場合は`catalog::Anchor`を使用します。
1. 画像アンカーが定義されている場合は、レイヤーを変形し、`extend=`を適用してorigin=値に変換します。
1. 画像アンカーが定義されていない場合は、レイヤーの原点がレイヤーの長方形の中心に配置されます（`extend=`適用後）。

![&#x200B; レイヤー配置画像](assets/layerplacement.png)
