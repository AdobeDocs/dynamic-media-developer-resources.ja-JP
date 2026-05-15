---
description: カタログレコード識別子
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
TQID: 'https://experienceleague.adobe.com/M3stRhM1PHUVUFXTKj-KERQVMOGVolpxUuyNUrRzado'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 7%

---

# ID {#id}

画像データ ファイル内のレコードが[!DNL Platform Server]によって検索されるインデックス キー値。

通常、SKUに複数の画像がある場合は、SKU番号などの短い一意の画像識別子（ある種の画像サフィックスを含む場合もあります）。 また、画像サービングを使用してweb サイトを簡単にレトロフィッティングできるように、ファイルパスのように見える、より複雑な文字列を指定することもできます。

## プロパティ {#id-properties}

テキスト文字列。 必須。 画像データテーブルのプライマリインデックスキー。 各カタログ：:Id値は、テーブル内で一意である必要があります。

## 初期設定 {#id-default}

なし

## 関連項目 {#id-seealso}

[属性：:RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
