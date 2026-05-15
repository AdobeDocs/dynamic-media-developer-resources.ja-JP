---
description: ユーザーデータ： サーバーは、req=userdataに応答して、このフィールドの内容をクライアントに返します。
solution: Experience Manager
title: UserData
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
TQID: 'https://experienceleague.adobe.com/9jhCw--mmCQ1-j1uNGFmfTEcnkNzxbKfXJtve5GugdA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 3%

---

# UserData{#userdata}

ユーザーデータ： サーバーは、req=userdataに応答して、このフィールドの内容をクライアントに返します。

## プロパティ {#section-06f2002b77d54a64be07f12fff54ad13}

テキスト文字列値。 [ プロパティデータ ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md)のフォーマットを使用することをお勧めします。 プロパティデータの書式設定を使用しない場合、テキスト文字列に「=」文字を含めることはできません。

ズーム、スピン、パンフレットビューアの各クライアントは、このフィールドがプロパティデータの書式設定を使用することを前提としています。 これらのクライアントは、ビューアの設定とカスタマイズにこのフィールドを使用します。 詳しくは、ビューアのドキュメントを参照してください。

このフィールドは、テキスト文字列のローカライズに参加します。 詳しくは、*HTTP プロトコルリファレンス*&#x200B;の[ テキスト文字列のローカライゼーション ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)を参照してください。

## 初期設定 {#section-7ee879762130467199745f2abc662f1e}

なし

## 関連項目 {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)、[ テキスト文字列のローカライゼーション ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
