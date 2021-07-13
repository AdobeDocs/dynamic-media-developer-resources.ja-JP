---
description: Digimarcユーザ情報 Digimarc埋め込みのユーザ情報を指定します。
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# DigimarcId{#digimarcid}

Digimarcユーザ情報 Digimarc埋め込みのユーザ情報を指定します。

## プロパティ {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

コンマ区切りの整数を5または6個指定します。 3番目と4番目の数値は使用されなくなりました。

`creator-id, creator-pin, durability [ , chroma ]`

`creator-id`と`creator-pin`は、サービスの購入時にDigimarcから提供されます。 未使用の値は空のままにする必要があります。

`durability` Digimarc透かし埋め込みの強さを指定します。1、2、3、4の場合があり、1は最も弱いことを示し、4は最も強い耐久性を示します。

透かしを画像の彩度データにエンコードする場合は`chroma`を1に設定し、輝度にエンコードする場合は0（デフォルト）に設定します。 グレースケール画像を出力する際、この設定は無視されます。

## 初期設定 {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

`default::DigimarcId`から継承されます（定義されていない場合または空の場合）。

## 例 {#section-8469ae1c27b4461da3d53fbabc32d3c5}

耐久性が4に設定されたテストDigimarc creator idを指定します。

`DigimarcId= 404407,32,,,4`

## 関連項目 {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
