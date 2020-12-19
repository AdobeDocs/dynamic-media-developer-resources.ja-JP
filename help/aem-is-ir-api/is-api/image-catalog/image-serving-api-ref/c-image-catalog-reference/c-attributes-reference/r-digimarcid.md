---
description: Digimarcユーザ情報 Digimarc埋め込みのユーザ情報を指定します。
seo-description: Digimarcユーザ情報 Digimarc埋め込みのユーザ情報を指定します。
seo-title: DigimarcId
solution: Experience Manager
title: DigimarcId
topic: Scene7 Image Serving - Image Rendering API
uuid: 23f1952f-71b7-4b2a-917d-8161ea855ac9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 3%

---


# DigimarcId{#digimarcid}

Digimarcユーザ情報 Digimarc埋め込みのユーザ情報を指定します。

## プロパティ {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

カンマ区切りの5または6個の整数。 3番目と4番目の数字は使用されなくなりました。

`creator-id, creator-pin, durability [ , chroma ]`

`creator-id`と`creator-pin`は、サービスの購入時にDigimarcから提供されます。 未使用の値は空のままにする必要があります。

`durability` Digimarc透かし埋め込みの強度を指定します。1、2、3または4の場合があり、1は最も弱いことを示し、4は最も強い耐久性を示します。

透かしを画像のクロミナンスデータにエンコードする場合は`chroma`を1に設定し、輝度にエンコードする場合は0（初期設定）に設定します。 グレースケール画像を出力する場合、この設定は無視されます。

## 初期設定 {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

定義されていない場合や空の場合は`default::DigimarcId`から継承されます。

## 例 {#section-8469ae1c27b4461da3d53fbabc32d3c5}

耐久性が4に設定されたテストDigimarc creator idを指定します。

`DigimarcId= 404407,32,,,4`

## 関連項目 {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
