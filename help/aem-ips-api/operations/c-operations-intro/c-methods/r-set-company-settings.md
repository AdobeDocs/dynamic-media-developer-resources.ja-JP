---
description: 会社固有の様々な設定値を設定します。
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 12%

---

# setCompanySettings{#setcompanysettings}

会社固有の様々な設定値を設定します。

構文

## 認証済みユーザータイプ {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-a472da6c57c74a94a179dda081004888}

**入力 (setCompanySettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社の取り扱い。 |
| overwriteMode | `xsd:string` | いいえ | アセットの上書きモード。 |
| retainPublishState | `xsd:boolean` | いいえ | に設定 `true` アセットの再アップロード時に公開状態を保持する。 |
| defaultSourceProfileHandle | `xsd:string` | いいえ | デフォルトのソースカラープロファイルとして使用する IccProfile アセット。 |
| defaultDisplayProfileHandle | `xsd:string` | いいえ | 初期設定の表示カラープロファイルとして使用する IccProfile アセット。 |
| iptcExifMappingXsltHandle | `xsd:string` | いいえ | IPTC および EXIF メタデータを IPS メタデータフィールドにマッピングするために使用される XSL アセット。 |
| xmpMappingXsltHandle | `xsd:string` | いいえ | IPS メタデータフィールドへのXMPメタデータのマッピングに使用される XSL アセット。 |
| diskSpaceWarningMin | `xsd:int` | いいえ | 警告メッセージが送信される前に使用可能な最小空きディスク容量 (KB)。 |
| emailTrashCleanupWarning | `xsd:boolean` | いいえ | に設定 `true` を使用して、アセットをごみ箱から空にしたときに会社管理者に通知を送信できます。 |

**出力 (setCompanySettingsReturn)**

IPS API はこの操作に対する応答を返しません。

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
