---
description: Source データルートパス。 この画像カタログのソースデータのルートフォルダーの絶対パスまたは相対パス。
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
TQID: 'https://experienceleague.adobe.com/WFDqweSZS1tNJppprC8pJblN-7LBKRM-IHt2Vfj3oW0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 111
ht-degree: 2%

---

# RootPath{#rootpath}

Source データルートパス。 この画像カタログのソースデータのルートフォルダーの絶対パスまたは相対パス。

`RootPath`はテキスト文字列値です。 サーバールートパスについて詳しくは、[Source データの管理](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)を参照してください。

## プロパティ {#section-b41d7e0ea63143eb8034569706cad0c0}

テキスト文字列。 空、有効な相対フォルダーパス、またはImage Serverからアクセスできる有効な絶対パスである必要があります。

## 初期設定 {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

定義されていない場合、`default::RootPath`から継承されます。 定義されていても空の場合は、ソースファイルのルートパスには影響しません。

## 関連項目 {#section-6bf4ffc4987843a9a2dbe81b43076437}

[ カタログ：:Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md)、[ カタログ：:MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)、[ ルールセット：:PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)、[Source データの管理](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
