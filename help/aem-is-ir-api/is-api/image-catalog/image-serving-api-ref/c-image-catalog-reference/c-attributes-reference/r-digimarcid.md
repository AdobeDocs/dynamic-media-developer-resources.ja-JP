---
description: Digimarc ユーザー情報。 Digimarc埋め込み用のユーザー情報を指定します。
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
TQID: 'https://experienceleague.adobe.com/2kkvN1RLEhbDEmN4cA6lE5nGe9d-T3qcdxgGqF7L3Ig'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 2%

---

# DigimarcId{#digimarcid}

Digimarc ユーザー情報。 Digimarc埋め込み用のユーザー情報を指定します。

## プロパティ {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

5または6つのコンマ区切りの整数。 3番目と4番目の数字は使用されなくなりました。

`creator-id, creator-pin, durability [ , chroma ]`

`creator-id`と`creator-pin`は、サービスの購入時にDigimarcによって提供されます。 未使用の値は空のままにする必要があります。

`durability`は、Digimarc透かしの埋め込み強度を指定します。 1、2、3、4のいずれかであり、1は最も弱く、4は最も強い耐久性を示す。

画像のクロミナンスデータに透かしをエンコードするには`chroma`を1に、輝度にエンコードするには0 （デフォルト）に設定します。 グレースケール画像を出力する場合、この設定は無視されます。

## 初期設定 {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

定義されていない場合や空の場合は、`default::DigimarcId`から継承されます。

## 例 {#section-8469ae1c27b4461da3d53fbabc32d3c5}

耐久性が4に設定されたテスト Digimarc作成者IDを指定します。

`DigimarcId= 404407,32,,,4`

## 関連項目 {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
