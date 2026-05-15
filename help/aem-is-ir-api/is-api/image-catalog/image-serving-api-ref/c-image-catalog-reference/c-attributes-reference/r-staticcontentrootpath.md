---
description: 静的コンテンツデータのルートパス： この画像カタログの静的コンテンツデータのルートフォルダーの絶対パスまたは相対パスセグメント。
solution: Experience Manager
title: StaticContentRootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55ca44cd-4330-47e6-94cc-58c078d34bbd
TQID: 'https://experienceleague.adobe.com/u9O8XaMdnb02UPw1uIjhYjzpFvMk-tFfh3UqlcVnNcc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 2%

---

# StaticContentRootPath{#staticcontentrootpath}

静的コンテンツデータのルートパス： この画像カタログの静的コンテンツデータのルートフォルダーの絶対パスまたは相対パスセグメント。

サーバールートパスについて詳しくは、[Source データの管理](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)を参照してください。

## プロパティ {#section-f8e3986096294b36948d43aafdc3e795}

テキスト文字列。 空、有効な相対ファイルパスセグメント、または絶対パスである必要があります。 先頭と末尾のパス要素の区切り文字を含めないでください。

## 初期設定 {#section-0f741f90fd8d4758a43162c2b5c8a3a3}

定義されていない場合、`default::StaticContentsRootPath`から継承されます。 定義されていても空の場合は、ソースファイルのルートパスには影響しません。

## 関連項目 {#section-9af8846d20d242789df67877f84ed8a7}

[PS::staticContent.rootPaths](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-staticcontentrootpath.md#reference-a2b5368d078349828d282357681bb2a5)、[Source データの管理](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)
