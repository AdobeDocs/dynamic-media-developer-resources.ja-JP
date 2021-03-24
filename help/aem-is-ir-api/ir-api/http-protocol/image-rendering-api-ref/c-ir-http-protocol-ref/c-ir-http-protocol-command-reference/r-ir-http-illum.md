---
description: 照明マップセレクタ このマテリアルをレンダリングする際に使用する照明マップを指定します。
solution: Experience Manager
title: イラム
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 4%

---


# イラム{#illum}

照明マップセレクタ このマテリアルをレンダリングする際に使用する照明マップを指定します。

`illum=-1|0|1|2`

指定した照明マップがターゲットビネットで使用できない場合は、代わりに使用可能な最も近いマップが使用されます。

`illum=-1` は、 `gloss=` 値に基づいて照明マップが自動的に選択されるように指定します。

## プロパティ {#section-aace8466566e4cf1a0c5a6c0167245c9}

マテリアル属性 ビネットで複数の照明マップが定義されていない場合は無視されます。

## 初期設定 {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## 関連項目 {#section-9132e60381c64aa3a8ed1319690db55e}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
