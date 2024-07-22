---
description: Digimarc ユーザ情報 Digimarc 埋め込みのユーザー情報を指定します。
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# DigimarcId{#digimarcid}

Digimarc ユーザ情報 Digimarc 埋め込みのユーザー情報を指定します。

## プロパティ {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

5 ～ 6 個のコンマ区切りの整数。 3 番目と 4 番目の数値は使用されなくなりました。

`creator-id, creator-pin, durability [ , chroma ]`

`creator-id` と `creator-pin` は、サービスの購入時に Digimarc によって提供されます。 未使用の値は空のままにする必要があります。

`durability` 埋め込み強度を指定します。 1、2、3、4 のいずれかです。1 は最も弱い耐久性を示し、4 は最も強い耐久性を示します。

`chroma` を 1 に設定すると、透かしを画像のクロミナンスデータにエンコードし、0 （デフォルト）を設定すると、ルミナンスにエンコードします。 グレースケール画像を出力する場合、この設定は無視されます。

## 初期設定 {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

定義されていない場合または空の場合は `default::DigimarcId` から継承します。

## 例 {#section-8469ae1c27b4461da3d53fbabc32d3c5}

耐久度を 4 に設定したテスト Digimarc Creator ID を指定します。

`DigimarcId= 404407,32,,,4`

## 関連項目 {#section-75d4d2afd1df4127b31b1a82f30079d8}

[カタログ：:DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
