---
description: フォントメトリクスのファイルパス フォント指標ファイルのパスと名前（ファイルのサフィックスを含む）。
seo-description: フォントメトリクスのファイルパス フォント指標ファイルのパスと名前（ファイルのサフィックスを含む）。
seo-title: MetricsPath
solution: Experience Manager
title: MetricsPath
uuid: b59110bf-330f-4ca4-8b0a-219a61d383f7
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---


# MetricsPath{#metricspath}

フォントメトリクスのファイルパス フォント指標ファイルのパスと名前（ファイルのサフィックスを含む）。

Adobe Type1のフォントに使用します。 指定しなかった場合、サーバーは、プリンシパルフォントファイルが存在するのと同じフォルダー内にフォントメトリクスファイルを探します。 レンダリング時に必要なフォント指標ファイルが見つからない場合は、エラーが発生します。

## プロパティ {#section-955268c581574875b05253d9e14544f3}

テキスト文字列。 Adobe Type1ファイルのオプションです。 空または有効なImage Serverのファイルパス（絶対パスまたは`attribute::RootPath`を基準とする相対パス）を指定する必要があります。

## 初期設定 {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

なし

## 関連項目 {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
