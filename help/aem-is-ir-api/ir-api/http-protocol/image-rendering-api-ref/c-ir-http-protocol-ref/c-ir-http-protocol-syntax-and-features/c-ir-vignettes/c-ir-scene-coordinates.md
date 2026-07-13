---
title: シーン座標
description: シーン座標空間は、テクスチャ可能なオブジェクトのサーフェス上のサイズと距離を指定するために使用されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: de7f088e-3825-4d2e-924e-001a44db62a0
TQID: 'https://experienceleague.adobe.com/eiZh-q74Q7fGwtuyj8dKSi8h-RMSjOSP7I6Wbq5FxTU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 0%

---

# シーン座標{#scene-coordinates}

シーン座標空間は、テクスチャ可能なオブジェクトのサーフェス上のサイズと距離を指定するために使用されます。

ほとんどのビネットは物理的なオブジェクトを表す実世界のシーンであるため、ほとんどのビネットはシーン座標空間の単位としてインチを使用して作成されます。 mmやcmなどの他の単位も使用できます。 画像レンダリングでは、単位変換はサポートされていません。

次のコマンドは、シーン座標空間の値を受け入れます。

* [grout=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
* [pos=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8)
* [size=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)

