---
description: フォント指標ファイルのパス。 フォントメトリックファイルのパスと名前（ファイルのサフィックスを含む）。
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
TQID: 'https://experienceleague.adobe.com/XPXcnrT94IfPupctNoxqN7-qYCuxdeoqXQeBkM1Un4k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 3%

---

# MetricsPath{#metricspath}

フォント指標ファイルのパス。 フォントメトリックファイルのパスと名前（ファイルのサフィックスを含む）。

Adobe Type 1 フォントに使用されます。 指定しない場合、サーバーは、プリンシパルフォントファイルが配置されているフォルダー内にフォント指標ファイルを検索しようとします。 レンダリング時に必要なフォント指標ファイルが見つからない場合にエラーが発生します。

## プロパティ {#section-955268c581574875b05253d9e14544f3}

テキスト文字列。 Adobe Type 1 ファイルの場合はオプションです。 空または有効なImage Server ファイルパスを指定する必要があります。絶対パスまたは`attribute::RootPath`からの相対パスを指定してください。

## 初期設定 {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

なし

## 関連項目 {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[属性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
