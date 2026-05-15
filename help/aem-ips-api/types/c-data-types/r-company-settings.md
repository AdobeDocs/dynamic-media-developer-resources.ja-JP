---
description: 会社固有の設定設定。
solution: Experience Manager
title: CompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
TQID: 'https://experienceleague.adobe.com/iGc-AwCFbpkATjLjvSBtx4vsP0-OUDSkH2dFHZ-j2rg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 244
ht-degree: 1%

---

# [!DNL CompanySettings]{#companysettings}

会社固有の設定設定。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| overwriteMode | `xsd:string` | 現在のフォルダー内の画像を、同じ基本画像名と拡張子で上書きするかどうかを指定します。 |
| retainPublishState | `xsd:boolean` | IPSにアップロードされた置き換え画像が、既存の「公開準備完了」設定を保持する必要があるか、またはアップロードで指定されたとおりに保持する必要があるかどうかを指定します。 |
| defaultSourceProfile | `types:Asset` | CMYK画像ファイルを追加する際に、「デフォルトのカラー動作を使用」の一部として自動的に適用されるデフォルトのソースカラープロファイル（コーティングされたFOGRA27 （ISO 126472:2004））を指定します。 |
| defaultDisplayProfile | `types:Asset` | CMYK画像ファイルを追加する際に、「デフォルトのカラー動作を使用」の一部として自動的に適用されるデフォルトの内部カラープロファイル（U.S. Web Coated （SWOP） v2）を指定します。 |
| iptcExifMappingXslt | `types:Asset` | IPTCおよびEXIF画像ヘッダーデータをIPSに抽出するには、社内フィールド名から自社で定義したフィールド名に変換する必要があります。 アップロードされた画像のXSL翻訳テーブルを指定します（デフォルトは「IPTCまたはEXIF フィールドを抽出しない」）。 |
| xmpMappingXslt | `types:Asset` | XMPの画像ヘッダーデータをIPSに取り込むには、社内フィールド名を社内フィールド名から自社フィールド名に変換する必要があります。 アップロードされた画像のXSL翻訳テーブルを指定します（デフォルトは「XMP フィールドを抽出しない」）。 |
| diskSpaceWarningMin | `xsd:int` | 警告が送信される前のイメージ ディレクトリの空きディスク領域の最小量。 |
| emailTrashCleanupWarning | `xsd:boolean` | ゴミ箱アイテムが自動的に削除される前にメールを送信するかどうかを決定します。 |
| javascriptUploadEnabled | `types:Asset` | JavaScript ファイルをアップロードするかどうかを指定します。 このオプションはセキュリティ上の潜在的なリスクがあるため、慎重に使用してください。 |
