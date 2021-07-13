---
description: フォント指標のファイルパス。 ファイルサフィックスを含むフォントメトリックファイルのパスと名前。
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---

# MetricsPath{#metricspath}

フォント指標のファイルパス。 ファイルサフィックスを含むフォントメトリックファイルのパスと名前。

Adobe Type1フォントに使用します。 指定しなかった場合、サーバーはプリンシパルフォントファイルが存在するフォルダーと同じフォルダー内でフォントメトリックファイルを探します。 必要なフォントメトリックファイルがレンダリング時に見つからない場合、エラーが発生します。

## プロパティ {#section-955268c581574875b05253d9e14544f3}

テキスト文字列。 Adobe Type1ファイルの場合はオプション。 空または有効なImage Serverファイルパス（絶対パスまたは`attribute::RootPath`に対する相対パス）を指定する必要があります。

## 初期設定 {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

なし

## 関連項目 {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
