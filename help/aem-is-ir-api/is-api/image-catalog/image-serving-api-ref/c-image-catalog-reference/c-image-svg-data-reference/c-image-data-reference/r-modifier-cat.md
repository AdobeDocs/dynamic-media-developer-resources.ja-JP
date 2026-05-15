---
description: 接頭辞リクエスト修飾子文字列。 「&」文字で区切られた画像サービングコマンドはありません。
solution: Experience Manager
title: 修飾子
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
TQID: 'https://experienceleague.adobe.com/b1j5WmY-PNOt1zW9qglJob5W8csmI3TidhDwoHK3kCM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 7%

---

# 修飾子{#modifier}

接頭辞リクエスト修飾子文字列。 「&amp;」文字で区切られた画像サービングコマンドはありません。

画像を永続的に変更し、テンプレートの本文を保存するために使用します。

このフィールドのコマンドは、このレコードが参照されるリクエストまたはテンプレート内の同じコマンドと、`catalog::PostModifier`内のコマンドによって上書きされます

マクロは、同じカタログまたはデフォルトのカタログで定義されている限り、`catalog::Modifier`で許可されます。 カスタム変数も使用できます。

## プロパティ {#section-6674388f77d644469371a17e8809c45f}

テキスト文字列。 オプション。

## 初期設定 {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

なし

## 関連項目 {#section-7a67803d141b442180c418c1f3cff029}

[catalog::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
