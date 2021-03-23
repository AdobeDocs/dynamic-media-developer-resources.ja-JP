---
description: 会社固有の様々な設定値を設定します。
seo-description: 会社固有の様々な設定値を設定します。
seo-title: setCompanySettings
solution: Experience Manager
title: setCompanySettings
uuid: 5908082f-6743-4444-ba73-757ad4664890
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 11%

---


# setCompanySettings{#setcompanysettings}

会社固有の様々な設定値を設定します。

構文

## 認証済みユーザータイプ{#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-a472da6c57c74a94a179dda081004888}

**入力(setCompanySettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社ハンドル |
| `*`overwriteMode`*` | `xsd:string` | いいえ | アセットの上書きモード。 |
| `*`retainPublishState`*` | `xsd:boolean` | いいえ | アセットが再アップロードされたときに公開状態を保持するには、`true`に設定します。 |
| `*`defaultSourceProfileHandle`*` | `xsd:string` | いいえ | 初期設定のソースカラープロファイルとして使用するIccProfileアセット。 |
| `*`defaultDisplayProfileHandle`*` | `xsd:string` | いいえ | 初期設定の表示カラープロファイルとして使用するIccProfileアセット。 |
| `*`iptcExifMappingXsltHandle`*` | `xsd:string` | いいえ | IPTCおよびEXIFメタデータをIPSメタデータフィールドにマッピングするために使用されるXSLアセット。 |
| `*`xmpMappingXsltHandle`*` | `xsd:string` | いいえ | XMPメタデータをIPSメタデータフィールドにマップするために使用されるXSLアセット。 |
| `*`diskSpaceWarningMin`*` | `xsd:int` | いいえ | 警告メッセージが送信される前に使用可能な最小空きディスク領域(KB)。 |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | いいえ | アセットがごみ箱から空になるたびに会社管理者に通知を送信するには、`true`に設定します。 |

**Output (setCompanySettingsReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

このコードのサンプルは、会社の設定を設定します。

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
