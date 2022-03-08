---
description: 関連アセットのグループのプロジェクトを取得します。
solution: Experience Manager
title: getProjects
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7262ed7-7419-4d6b-86ed-f3ad4657d654
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 22%

---

# getProjects{#getprojects}

関連アセットのグループのプロジェクトを取得します。

構文

## 認証済みユーザータイプ {#section-337649866b1f4098844d1974ed7ab5d0}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-8d549237b8c440b4872a0a086ddc00a1}

**入力 (getProjectsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社への取り扱い。 |

**出力 (getProjectsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| projectArray | `types:ProjectArray` | はい | 会社に関連付けられたプロジェクトの配列。 |

## 例 {#section-8b12d0b948f644f68bf9a16060d3849a}

このコード例では、プロジェクト配列内のすべてのプロジェクトハンドルを返します。

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
