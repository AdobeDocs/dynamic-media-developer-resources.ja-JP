---
description: 会社固有の設定。
solution: Experience Manager
title: CompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 1%

---

# [!DNL CompanySettings]{#companysettings}

会社固有の設定。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| overwriteMode | `xsd:string` | 現在のフォルダーにある、ベースの画像名と拡張子が同じ画像を上書きするかどうかを指定します。 |
| retainPublishState | `xsd:boolean` | IPS にアップロードされた置き換え画像で、既存の「公開準備完了」設定を維持するか、アップロードで指定されたとおりに公開するかを指定します。 |
| defaultSourceProfile | `types:Asset` | CMYK 画像ファイルの追加時に「デフォルトのカラー動作を使用」の一部として自動的に適用されるデフォルトのソースカラープロファイル（Coated FOGRA27 （ISO 126472:2004））を指定します。 |
| defaultDisplayProfile | `types:Asset` | CMYK 画像ファイルの追加時に「デフォルトのカラー動作を使用」の一部として自動的に適用されるデフォルトの内部カラープロファイル（U.S. Web Coated （SWOP） v2）を指定します。 |
| iptcExifMappingXslt | `types:Asset` | IPTCと EXIF 画像ヘッダーデータを IPS に抽出するには、会社の内部フィールド名をユーザー定義フィールド名に変換する必要があります。 アップロードした画像の XSL 変換テーブルを指定します（デフォルトは「IPTCまたは EXIF フィールドを抽出しない」）。 |
| xmpMappingXslt | `types:Asset` | XMP画像ヘッダーデータを IPS に抽出するには、会社の内部フィールド名をユーザー定義フィールド名に変換する必要があります。 アップロードされた画像の XSL 変換テーブルを指定します（デフォルトは「XMP フィールドを抽出しない」）。 |
| diskSpaceWarningMin | `xsd:int` | 警告が送信される前のイメージ ディレクトリの空きディスク領域の最小量です。 |
| emailTrashCleanupWarning | `xsd:boolean` | ごみ箱のアイテムが自動的に削除される前に E メールを送信するかどうかを決定します。 |
| javascriptUploadEnabled | `types:Asset` | JavaScript ファイルをアップロードするかどうかを指定します。 このオプションはセキュリティ上のリスクを伴う可能性があるので、慎重に使用してください。 |
