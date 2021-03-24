---
description: 描画モード. レイヤーを合成するときに使用するブレンドの種類を指定します。 Photoshopでよく使用される描画モードをシミュレートします。 詳細はPhotoshopの文書を参照。
solution: Experience Manager
title: blendMode
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 14%

---


# blendMode{#blendmode}

描画モード. レイヤーを合成するときに使用するブレンドの種類を指定します。 Photoshopでよく使用される描画モードをシミュレートします。 詳細はPhotoshopの文書を参照。

`blendMode=norm|dissolve|lighten|darken|mult|screen`

## プロパティ {#section-418aad5a417f49929d1953e226e5c8dd}

レイヤー属性 `layer=0`と`layer=comp`では無視されます。

## 初期設定 {#section-69829acc6532448d8612a4a54e86f00e}

`blendMode=norm`

## 例 {#section-d209dd9c270b469c87558a8910c50b61}

`…&size=200,200&bgColor=191,120,241&…`

`…&layer=1&src=myRootId/myImageId&opac=80&blendMode=dissolve&…`

## 関連項目 {#section-bc7ccdfcb310441c938c0bde3e00d7b3}

[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)
