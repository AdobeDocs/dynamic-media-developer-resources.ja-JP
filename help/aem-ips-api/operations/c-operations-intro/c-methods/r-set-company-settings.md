---
description: 会社固有の様々な設定値を設定します。
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 12%

---

# setCompanySettings{#setcompanysettings}

会社固有の様々な設定値を設定します。

構文

## 許可されたユーザーの種類 {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-a472da6c57c74a94a179dda081004888}

**入力(setCompanySettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社の担当。 |
| `*`overwriteMode`*` | `xsd:string` | いいえ | アセットの上書きモード。 |
| `*`retainPublishState`*` | `xsd:boolean` | いいえ | アセットが再アップロードされたときの公開状態を保持するには、 `true`に設定します。 |
| `*`defaultSourceProfileHandle`*` | `xsd:string` | いいえ | デフォルトのソースカラープロファイルとして使用するIccProfileアセット。 |
| `*`defaultDisplayProfileHandle`*` | `xsd:string` | いいえ | デフォルトの表示カラープロファイルとして使用するIccProfileアセット。 |
| `*`iptcExifMappingXsltHandle`*` | `xsd:string` | いいえ | IPTCおよびEXIFメタデータをIPSメタデータフィールドにマッピングするために使用されるXSLアセット。 |
| `*`xmpMappingXsltHandle`*` | `xsd:string` | いいえ | IPSメタデータフィールドへのXMPメタデータのマッピングに使用されるXSLアセット。 |
| `*`diskSpaceWarningMin`*` | `xsd:int` | いいえ | 警告メッセージが送信される前に使用可能な最小空きディスク領域(KB)。 |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | いいえ | アセットがごみ箱から空になるたびに会社の管理者に通知を送信するには、 `true`に設定します。 |

**出力(setCompanySettingsReturn)**

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
