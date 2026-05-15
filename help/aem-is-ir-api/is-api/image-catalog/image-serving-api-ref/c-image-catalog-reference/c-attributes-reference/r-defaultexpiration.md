---
description: デフォルトの画像応答のクライアントキャッシュ TTL。 デフォルトの画像応答（defaultImage=または属性DefaultImageで指定されたデフォルト画像を返す応答）の有効期限を指定します。
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
TQID: 'https://experienceleague.adobe.com/v-wtXCBtpHpf9mTjoQ58GZ9eXq-yR2tpGT0Kd-DTyNI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 1%

---

# DefaultExpiration{#defaultexpiration}

デフォルトの画像応答のクライアントキャッシュ TTL。 デフォルトの画像応答（defaultImage=またはattribute::DefaultImageで指定されたデフォルト画像を返す応答）の有効期限を指定します。

既定の画像がカタログ レコードに関連付けられていない場合、または既定の画像カタログ レコードが特定の`catalog::Expiration`値を提供しない場合にのみ適用されます。

## プロパティ {#section-e564512476604fd7b964f9f2903d6d33}

実数、0以上。 返信データが生成されてから有効期限が切れるまでの時間数。 0に設定すると、返信画像が即座に期限切れになり、デフォルトの画像応答のクライアントキャッシュが効果的に無効になります。 `never expire`としてマークするには、`-1`に設定します。

## 初期設定 {#section-131cd32c2e214391857dba5af321f8cd}

定義されていない場合や空の場合は、`default::DefaultExpiration`から継承されます。

TTL （Time-To-Live）は、キャッシュの有効期限が切れるまでの時間です。 デフォルトのTTLは1時間です。

## 関連項目 {#section-d8642c22e3d947129367dd76366963d6}

[ カタログ：：有効期限](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a)、[属性：:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
