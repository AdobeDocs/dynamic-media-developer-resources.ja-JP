---
description: フォントメトリクスのファイルパス。 フォントメトリクスファイルのパスと名前（ファイルのサフィックスを含む）。
seo-description: フォントメトリクスのファイルパス。 フォントメトリクスファイルのパスと名前（ファイルのサフィックスを含む）。
seo-title: MetricsPath
solution: Experience Manager
title: MetricsPath
topic: Scene7 Image Serving - Image Rendering API
uuid: b59110bf-330f-4ca4-8b0a-219a61d383f7
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# MetricsPath{#metricspath}

フォントメトリクスのファイルパス。 フォントメトリクスファイルのパスと名前（ファイルのサフィックスを含む）。

Adobe Type 1フォントに使用されます。 指定しなかった場合、サーバーは、プリンシパルフォントファイルが存在するフォルダーと同じフォルダー内のフォントメトリクスファイルを検索しようとします。 レンダリング時に必要なフォントメトリクスファイルが見つからない場合は、エラーが発生します。

## プロパティ {#section-955268c581574875b05253d9e14544f3}

テキスト文字列。 Adobe Type 1ファイルのオプションです。 空または有効なImage Serverのファイルパス（絶対パスまたは相対パス）を指定する必要がありま `attribute::RootPath`す。

## 初期設定 {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

なし

## 関連項目 {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
