---
description: 関連アセットのグループのプロジェクトを取得します。
seo-description: 関連アセットのグループのプロジェクトを取得します。
seo-title: getProjects
solution: Experience Manager
title: getProjects
topic: Scene7 Image Production System API
uuid: 46ec9a5d-4414-4c9c-aaf2-0db654204b61
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

---


# getProjects{#getprojects}

関連アセットのグループのプロジェクトを取得します。

構文

## 認証済みユーザータイプ{#section-337649866b1f4098844d1974ed7ab5d0}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-8d549237b8c440b4872a0a086ddc00a1}

**入力(getProjectsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |

**出力(getProjectsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`projectArray`*` | `types:ProjectArray` | はい | 会社に関連付けられたプロジェクトの配列。 |

## 例 {#section-8b12d0b948f644f68bf9a16060d3849a}

次のコード例は、プロジェクト配列内のすべてのプロジェクトハンドルを返します。

**リクエスト**

```java
<ns1:getProjectsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getProjectsParam>
```

**応答**

```java
<getProjectsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <projectArray>
      <items>
         <projectHandle>47|My Project 1</projectHandle>
         <name>My Project 1</name>
      </items>
      <items>
         <projectHandle>47|My Project 2</projectHandle>
         <name>My Project 2</name>
      </items>
   </projectArray>
</getProjectsReturn>
```

