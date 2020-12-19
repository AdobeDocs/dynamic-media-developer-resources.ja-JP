---
description: 再サンプリングモード resMode=の初期設定。 レンダリングイメージを最終的なサイズにスケールする際に使用するリサンプリングと補間のアトリビュートを指定します。
seo-description: 再サンプリングモード resMode=の初期設定。 レンダリングイメージを最終的なサイズにスケールする際に使用するリサンプリングと補間のアトリビュートを指定します。
seo-title: ResMode
solution: Experience Manager
title: ResMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 91d83274-b3e1-4233-bd01-21936726e1db
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 5%

---


# ResMode{#resmode}

再サンプリングモード resMode=の初期設定。 レンダリングイメージを最終的なサイズにスケールする際に使用するリサンプリングと補間のアトリビュートを指定します。

## プロパティ {#section-1183a155f33c4eca80f1dc6fb6bda1b5}

列挙。 `'bilin'`の場合は2、`'bicub'`の場合は3、`'sharp2'`の場合は4に設定します（詳しくは` [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)`を参照）。

## 初期設定 {#section-ed432a0acc3e4bce926a07e9cfd2c865}

定義されていない場合や空の場合は`default::ResMode`から継承されます。

## 関連項目 {#section-34b71c295b4349dfb4379823a2de83c2}

[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
