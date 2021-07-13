---
description: データファイルのパス。 この画像に関連付けられている非画像データファイルの相対パスと名前。
solution: Experience Manager
title: AuxPath
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 55f82596-72f0-48c4-9b3a-f10ea5f610f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# AuxPath{#auxpath}

データファイルのパス。 この画像に関連付けられている非画像データファイルの相対パスと名前。

サーバは、この値をattribute::RootPathと組み合わせて、実際のファイルパスを作成します。 また、絶対ファイルパスにすることもできます。

キャビネットマテリアルのキャビネットスタイルファイル、または窓カバーマテリアルの窓カバースタイルファイルを指定するために使用します。 その他の材料は空のままにします。

## プロパティ {#section-4268350054b7421da0ce0327f0731a52}

テキスト文字列の値。 指定する場合は、有効な相対パスまたは絶対パスを指定する必要があります。 キャビネットの材料と窓の覆い材料に必要です。 その他のすべてのマテリアルに対しては空にする必要があります。

## 初期設定 {#section-287005c2d8e948fa958f69ba7b90b437}

なし

## 関連項目 {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) 、 [catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590)、 [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
