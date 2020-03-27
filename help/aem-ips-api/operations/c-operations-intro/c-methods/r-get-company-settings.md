---
description: 特定の会社のIPS設定を返します。
seo-description: 特定の会社のIPS設定を返します。
seo-title: getCompanySettings
solution: Experience Manager
title: getCompanySettings
topic: Scene7 Image Production System API
uuid: 28ee706d-aaef-45a1-9655-3805f158cdc3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getCompanySettings{#getcompanysettings}

特定の会社のIPS設定を返します。

構文

## 認証されたユーザータイプ {#section-3378c9c67029473a87d5f5d8c616b1f3}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-e146f479c2744baa8f68be8c8848c97f}

**入力(getCompanySettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 設定を取得する会社のハンドル。 |

**Output (getCompanySettingsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`設定`*` | `types:CompanySettings` | はい | 会社の設定 |

## 例 {#section-191f78995ecf473a95eadf7296204fd7}

このコード例は、特定の会社のすべてのIPS設定を返します。

**リクエスト**

```java
<ns1:getCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
</ns1:getCompanySettingsParam>
```

**応答**

```java
<getCompanySettingsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <settings>
      <metadataArray>
         <items>
            <name>Profile Class</name>
            <value>1</value>
            <longVal>1</longVal>
         </items>
         <items>
             <name>Default Color Profile</name>
             <value>1</value>
         </items>
      </metadataArray>
      <iccProfileInfo>
         <originalPath>Scene7SharedAssets/ICCColorProfiles/Adobe ICC Profiles/RGB Profiles/</originalPath>
         <originalFile>sRGB Color Space Profile.icm</originalFile>
         <fileSize>0</fileSize>
      </iccProfileInfo>
      </defaultDisplayProfile>
      <diskSpaceWarningMin>100000</diskSpaceWarningMin>
      <emailTrashCleanupWarning>true</emailTrashCleanupWarning>
   </settings>
</getCompanySettingsReturn>
```

