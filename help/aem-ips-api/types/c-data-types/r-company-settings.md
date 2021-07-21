---
description: 会社固有の設定。
solution: Experience Manager
title: CompanySettings
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 2%

---

# CompanySettings{#companysettings}

会社固有の設定。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`overwriteMode`*` | `xsd:string` | 現在のフォルダー内の画像をベース名と拡張子が同じ画像で上書きするかどうかを指定します。 |
| `*`retainPublishState`*` | `xsd:boolean` | IPSにアップロードされた置き換え画像が、既存の「公開準備完了」設定を保持するか、アップロードで指定されたとおりに保持するかを指定します。 |
| `*`defaultSourceProfile`*` | `types:Asset` | CMYK画像ファイルを追加する際に、「デフォルトのカラー動作を使用」の一部として自動的に適用されるデフォルトのソースカラープロファイル(Coated FOGRA27(ISO 126472:2004))を指定します。 |
| `*`defaultDisplayProfile`*` | `types:Asset` | CMYK画像ファイルを追加する際に、「デフォルトのカラー動作を使用」の一部として自動的に適用される、デフォルトの内部カラープロファイル(U.S. Web Coated (SWOP) v2)を指定します。 |
| `*`iptcExifMappingXslt`*` | `types:Asset` | IPTCおよびEXIF画像ヘッダーデータをIPSに抽出するには、社内のフィールド名から会社のユーザー定義のフィールド名に変換する必要があります。 アップロードされた画像のXSL変換テーブル（デフォルトは「IPTCまたはEXIFフィールドを抽出しない」）を決定します。 |
| `*`xmpMappingXslt`*` | `types:Asset` | XMP画像ヘッダーデータをIPSに抽出する場合、社内のフィールド名から会社のユーザー定義のフィールド名に変換する必要があります。 アップロードされた画像のXSL変換テーブル(デフォルトは「XMPフィールドを抽出しない」)を決定します。 |
| `*`diskSpaceWarningMin`*` | `xsd:int` | 警告が送信される前の、イメージディレクトリの空きディスク領域の最小量。 |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | ごみ箱に入れた項目を自動的に削除する前にEメールを送信するかどうかを指定します。 |
| `*`javascriptUploadEnabled`*` | `types:Asset` | JavaScriptファイルをアップロードするかどうかを決定します。 これはセキュリティ上のリスクが発生する可能性があるので、このオプションを使用する際は注意が必要です。 |
