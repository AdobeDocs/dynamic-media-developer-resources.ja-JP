---
title: ResMode
description: 再サンプリングモード。 resMode=のデフォルト。 レンダリングされた画像を最終サイズに拡大/縮小するために使用するリサンプリングおよび補間属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c57932a0-529c-4f31-b60e-a38de6fe277f
TQID: 'https://experienceleague.adobe.com/FZ76OaQf5qTWEDjwaLQ38GcgXsSnemM8xST9CmH9HPs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 4%

---

# ResMode{#resmode}

再サンプリングモード。 `resMode=`の既定値。 レンダリングされた画像を最終サイズに拡大/縮小するために使用するリサンプリングおよび補間属性を指定します。

## プロパティ {#section-1183a155f33c4eca80f1dc6fb6bda1b5}

列挙： `'bilin'`では2に、`'bicub'`では3に、`'sharp2'`補間モードでは4に設定します（詳細は[resMode=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md)を参照）。

## 初期設定 {#section-ed432a0acc3e4bce926a07e9cfd2c865}

定義されていない場合や空の場合は、`default::ResMode`から継承されます。

## 関連項目 {#section-34b71c295b4349dfb4379823a2de83c2}

[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
