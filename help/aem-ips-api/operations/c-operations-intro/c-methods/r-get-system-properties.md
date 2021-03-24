---
description: 1回のリクエストですべてのシステムプロパティを取得します。
solution: Experience Manager
title: getSystemProperties
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 17%

---


# getSystemProperties{#getsystemproperties}

1回のリクエストですべてのシステムプロパティを取得します。

構文

## 認証済みユーザータイプ{#section-fc311ce90a54400fa95b9dd36b756e23}

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

次のコード例は、システムプロパティの配列を返します。 応答が短い間は切り捨てられました。

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

