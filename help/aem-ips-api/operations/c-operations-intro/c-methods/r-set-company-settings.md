---
description: 会社ごとに様々な設定値を設定します。
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
TQID: 'https://experienceleague.adobe.com/df-NUZDApA-q0a-A3oxM6PUQUoVmGy8gqS4HU8lhfvc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 10%

---

# setCompanySettings{#setcompanysettings}

会社ごとに様々な設定値を設定します。

構文

## 承認済みユーザータイプ {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-a472da6c57c74a94a179dda081004888}

**入力（setCompanySettingsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドル。 |
| overwriteMode | `xsd:string` | いいえ | アセットの上書きモード： |
| retainPublishState | `xsd:boolean` | いいえ | アセットが再アップロードされたときに公開状態を保持するには、`true`に設定します。 |
| defaultSourceProfileHandle | `xsd:string` | いいえ | デフォルトのソースカラープロファイルとして使用するIccProfile アセット。 |
| defaultDisplayProfileHandle | `xsd:string` | いいえ | デフォルトの表示カラープロファイルとして使用するIccProfile アセット。 |
| iptcExifMappingXsltHandle | `xsd:string` | いいえ | IPTCおよびEXIF メタデータをIPS メタデータフィールドにマッピングするために使用されるXSL アセット。 |
| xmpMappingXsltHandle | `xsd:string` | いいえ | XMP メタデータをIPS メタデータフィールドにマッピングするために使用されるXSL アセット。 |
| diskSpaceWarningMin | `xsd:int` | いいえ | 警告メッセージを送信する前に使用可能な最小の空きディスク容量（KB単位）。 |
| emailTrashCleanupWarning | `xsd:boolean` | いいえ | アセットがごみ箱から空になるたびに会社管理者に通知を送信するには、`true`に設定します。 |

**Output （setCompanySettingsReturn）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

このコードサンプルは、会社の設定を設定します。

**リクエスト**

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**応答**

なし
