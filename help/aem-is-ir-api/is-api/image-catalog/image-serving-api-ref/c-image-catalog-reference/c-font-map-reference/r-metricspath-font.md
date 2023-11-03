---
description: フォント指標のファイルパス。 ファイルサフィックスを含むフォント指標ファイルのパスと名前。
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 3%

---

# MetricsPath{#metricspath}

フォント指標のファイルパス。 ファイルサフィックスを含むフォント指標ファイルのパスと名前。

Adobe Type1 フォントに使用します。 指定しなかった場合、サーバーは、プリンシパルフォントファイルが存在するフォルダー内のフォントメトリクスファイルを探します。 レンダリング時に必要なフォント指標ファイルが見つからない場合は、エラーが発生します。

## プロパティ {#section-955268c581574875b05253d9e14544f3}

テキスト文字列。 Adobe Type1 ファイルの場合はオプションです。 空または有効な Image Server ファイルパス（絶対パスまたは相対パス）を指定する必要があります `attribute::RootPath`.

## 初期設定 {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

なし

## 関連項目 {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
