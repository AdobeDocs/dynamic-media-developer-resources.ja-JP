---
description: データファイルのパス この画像に関連付けられている画像以外のデータファイルの相対パスと名前。
solution: Experience Manager
title: AuxPath
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# AuxPath{#auxpath}

データファイルのパス この画像に関連付けられている画像以外のデータファイルの相対パスと名前。

サーバは、この値をattribute::RootPathと組み合わせて、実際のファイルパスを作成します。 ファイルの絶対パスを指定することもできます。

キャビネットマテリアルのキャビネットスタイルファイル、または窓カバリングマテリアルの窓カバリングスタイルファイルを指定するために使用します。 その他の材料は、空のままにしておきます。

## プロパティ {#section-4268350054b7421da0ce0327f0731a52}

テキスト文字列の値。 指定する場合は、有効な相対パスまたは絶対ファイルパスを指定する必要があります。 キャビネットの材料と窓カバリング材料に必要です。 他のすべての材料の場合は空にする必要があります。

## 初期設定 {#section-287005c2d8e948fa958f69ba7b90b437}

なし

## 関連項目 {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) ,  [catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
