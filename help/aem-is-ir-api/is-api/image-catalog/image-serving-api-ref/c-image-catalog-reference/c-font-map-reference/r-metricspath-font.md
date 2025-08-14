---
description: フォント指標ファイルのパス。 フォントメトリクスファイルのパスと名前（ファイルサフィックスを含む）。
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---

# MetricsPath{#metricspath}

フォント指標ファイルのパス。 フォントメトリクスファイルのパスと名前（ファイルサフィックスを含む）。

Adobe Type 1 フォントに使用します。 指定しない場合、サーバーは主フォントファイルと同じフォルダー内でフォント指標ファイルの検索を試みます。 レンダリング時に必要なフォント指標ファイルが見つからない場合、エラーが発生します。

## プロパティ {#section-955268c581574875b05253d9e14544f3}

テキスト文字列 Adobe Type 1 ファイルではオプションです。 空か、Image Server の有効なファイルパス（絶対パスまたは `attribute::RootPath` からの相対パス）である必要があります。

## 初期設定 {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

なし

## 関連項目 {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
