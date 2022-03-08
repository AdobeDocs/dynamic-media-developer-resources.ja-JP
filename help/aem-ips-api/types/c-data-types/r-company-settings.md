---
description: 会社固有の設定。
solution: Experience Manager
title: CompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 2%

---

# CompanySettings{#companysettings}

会社固有の設定。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| overwriteMode | `xsd:string` | 現在のフォルダ内の画像を元の同じ画像名と拡張子で上書きするかどうかを指定します。 |
| retainPublishState | `xsd:boolean` | IPS にアップロードされた置き換え画像で、既存の「公開準備完了」設定を保持するか、アップロードで指定された設定を保持するかを指定します。 |
| defaultSourceProfile | `types:Asset` | CMYK 画像ファイルを追加する際に、「初期設定のカラー動作を使用」の一部として自動的に適用される初期設定のソースカラープロファイル (Coated FOGRA27(ISO 126472:2004)) を指定します。 |
| defaultDisplayProfile | `types:Asset` | CMYK 画像ファイルを追加する際に、「初期設定のカラー動作を使用」の一部として自動的に適用される初期設定の内部カラープロファイル (U.S. Web Coated (SWOP) v2) を指定します。 |
| iptcExifMappingXslt | `types:Asset` | IPTC および EXIF の画像ヘッダーデータを IPS に抽出する場合、内部フィールド名から会社のユーザー定義フィールド名に変換する必要があります。 アップロードした画像の XSL 変換テーブル（デフォルトは「IPTC または EXIF フィールドを抽出しない」）を決定します。 |
| xmpMappingXslt | `types:Asset` | XMPの画像ヘッダーデータを IPS に抽出する場合、社内フィールド名から会社のユーザー定義フィールド名に変換する必要があります。 アップロードした画像の XSL 翻訳テーブル ( デフォルトは「XMPフィールドを抽出しない」) を決定します。 |
| diskSpaceWarningMin | `xsd:int` | 警告が送信される前のイメージディレクトリの空きディスク領域の最小量。 |
| emailTrashCleanupWarning | `xsd:boolean` | ごみ箱に入っている項目を自動的に削除する前に E メールを送信するかどうかを指定します。 |
| javascriptUploadEnabled | `types:Asset` | JavaScript ファイルをアップロードするかどうかを決定します。 これは潜在的なセキュリティリスクなので、このオプションを使用する際は注意が必要です。 |
