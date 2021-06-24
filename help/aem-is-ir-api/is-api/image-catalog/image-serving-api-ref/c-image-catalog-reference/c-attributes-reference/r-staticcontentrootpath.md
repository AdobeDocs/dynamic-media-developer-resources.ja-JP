---
description: 静的コンテンツデータのルートパス。 この画像カタログの静的コンテンツデータのルートフォルダーの絶対パスまたは相対パスセグメント。
solution: Experience Manager
title: StaticContentRootPath
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 55ca44cd-4330-47e6-94cc-58c078d34bbd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# StaticContentRootPath{#staticcontentrootpath}

静的コンテンツデータのルートパス。 この画像カタログの静的コンテンツデータのルートフォルダーの絶対パスまたは相対パスセグメント。

サーバーのルートパスの詳細については、「[ソースデータの管理](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)」を参照してください。

## プロパティ {#section-f8e3986096294b36948d43aafdc3e795}

テキスト文字列。 空、有効な相対ファイルパスセグメント、または絶対パスを指定する必要があります。 先頭と末尾にパス要素の区切り文字を含めないでください。

## 初期設定 {#section-0f741f90fd8d4758a43162c2b5c8a3a3}

定義されていない場合は`default::StaticContentsRootPath`から継承されます。 定義されているが空の場合、はソースファイルのルートパスに影響しません。

## 関連項目 {#section-9af8846d20d242789df67877f84ed8a7}

[PS::staticContent.rootPaths](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-staticcontentrootpath.md#reference-a2b5368d078349828d282357681bb2a5) 、ソースデ  [ータの管理](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)
