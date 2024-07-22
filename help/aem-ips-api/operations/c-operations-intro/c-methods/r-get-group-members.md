---
description: 特定の会社およびグループに属するユーザーを取得します。
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 14%

---

# getGroupMembers{#getgroupmembers}

特定の会社およびグループに属するユーザーを取得します。

構文

## 許可されているユーザータイプ {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-b798b06354c946abbb90fa72cc9c67fd}

**入力（getGroupMembersParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社へのハンドル。 |
| groupHandle | `xsd:string` |  | グループへのハンドル。 |

**出力（getGroupMembersReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userHandleArray | `type:HandleArray` | はい | ユーザーハンドルの配列。 |

## 例 {#section-aaa340dba6b64cce9bcd8303cf999166}

このコードサンプルでは、特定のグループに属するすべてのユーザーを含んだユーザーハンドル配列を返します。

**リクエスト**

```java
<ns1:getGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
</ns1:getGroupMembersParam>
```

**応答**

```java
<getGroupMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userHandleArray>
      <items>70|kmagnusson@adobe.com</items>
   </userHandleArray>
</getGroupMembersReturn>
```
