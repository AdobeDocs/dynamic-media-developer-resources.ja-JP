---
title: ResMode
description: 再サンプリングモード。 resMode=のデフォルト。 レンダリング イメージを最終サイズにスケーリングするために使用する再サンプリングおよび補間属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c57932a0-529c-4f31-b60e-a38de6fe277f
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# ResMode{#resmode}

再サンプリングモード。 `resMode=` のデフォルト。 レンダリング イメージを最終サイズにスケーリングするために使用する再サンプリングおよび補間属性を指定します。

## プロパティ {#section-1183a155f33c4eca80f1dc6fb6bda1b5}

列挙値。 補間モードが `'bilin'` の場合は 2、`'bicub'` の場合は 3、`'sharp2'` の場合は 4 に設定します（詳しくは [resMode=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md) を参照）。

## 初期設定 {#section-ed432a0acc3e4bce926a07e9cfd2c865}

定義されていない場合または空の場合は `default::ResMode` から継承します。

## 関連項目 {#section-34b71c295b4349dfb4379823a2de83c2}

[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
