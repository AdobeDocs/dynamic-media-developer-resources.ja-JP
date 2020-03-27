---
description: 会社固有の設定。
seo-description: 会社固有の設定。
seo-title: CompanySettings
solution: Experience Manager
title: CompanySettings
topic: Scene7 Image Production System API
uuid: a807d5c1-058d-4313-b4f8-6ee203284003
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CompanySettings{#companysettings}

会社固有の設定。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`overwriteMode`*` | `xsd:string` | 現在のフォルダ内の画像を同じ基本画像名と拡張子で上書きするかどうかを指定します。 |
| ` *`retainPublishState`*` | `xsd:boolean` | IPSにアップロードした置き換え画像に、既存の「公開準備完了」設定を保持するか、アップロードで指定したとおりに保持するかを指定します。 |
| ` *`defaultSourceProfile`*` | `types:Asset` | CMYK画像ファイルを追加する際に、「初期設定のカラー動作を使用」の一部として自動的に適用される初期設定のソースカラープロファイル(Coated FOGRA27(ISO 126472:2004))を指定します。 |
| ` *`defaultDisplayProfile`*` | `types:Asset` | CMYK画像ファイルを追加する際に「初期設定のカラー動作を使用」の一部として自動的に適用される初期設定の内部カラープロファイル(U.S. Web Coated (SWOP) v2)を指定します。 |
| ` *`iptcExifMappingXslt`*` | `types:Asset` | IPTCおよびEXIFイメージヘッダデータをIPSに抽出するには、内部フィールド名から会社のユーザ定義フィールド名に変換する必要があります。 アップロードされた画像のXSL変換テーブル（デフォルトは「IPTCまたはEXIFフィールドを抽出しない」）を決定します。 |
| ` *`xmpMappingXslt`*` | `types:Asset` | XMP画像ヘッダデータをIPSに抽出するには、内部のフィールド名から会社のユーザ定義のフィールド名に変換する必要があります。 アップロードした画像のXSL変換テーブル（デフォルトは「XMPフィールドを抽出しない」）を指定します。 |
| ` *`diskSpaceWarningMin`*` | `xsd:int` | 警告が送信される前の、イメージディレクトリの空きディスク領域の最小量。 |
| ` *`emailTrashCleanupWarning`*` | `xsd:boolean` | ごみ箱に入れた項目を自動的に削除する前に電子メールを送信するかどうかを指定します。 |
| ` *`javascriptUploadEnabled`*` | `types:Asset` | JavaScriptファイルをアップロードするかどうかを指定します。 これはセキュリティ上のリスクが高いので、このオプションは慎重に使用してください。 |

