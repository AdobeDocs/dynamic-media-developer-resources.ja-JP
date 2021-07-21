---
description: 1回のリクエストですべてのシステムプロパティを取得します。
solution: Experience Manager
title: getSystemProperties
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: b0ef16fd-1645-4e22-99bb-8c9269623168
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 18%

---

# getSystemProperties{#getsystemproperties}

1回のリクエストですべてのシステムプロパティを取得します。

構文

## 許可されたユーザーの種類 {#section-fc311ce90a54400fa95b9dd36b756e23}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## パラメータ {#section-b2a4fb7068424223aec87c50f0586d73}

**入力(getSystemPropertiesParam)**

なし

**出力(getSystemPropertiesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`propertyArray`*` | `types:PropertyArray` | はい | システムプロパティの配列。 |

## 例 {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

このコードサンプルは、システムプロパティの配列を返します。 簡潔にするために応答は切り捨てられました。

**リクエスト**

```java
<getSystemPropertiesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"/>
```

**応答**

```java
<getSystemPropertiesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"> 
   <propertyArray> 
      <items> 
         <name>SvgRenderEnabled</name> 
         <value>true</value> 
      </items> 
      <items> 
         <name>SwfRootUrl</name> 
         <value>/SWFs/</value> 
      </items> 
      ... 
   </propertyArray> 
</getSystemPropertiesReturn>
```
