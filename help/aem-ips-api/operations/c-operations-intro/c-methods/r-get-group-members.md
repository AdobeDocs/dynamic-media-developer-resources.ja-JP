---
description: 特定の会社およびグループに属するユーザーを取得します。
seo-description: 特定の会社およびグループに属するユーザーを取得します。
seo-title: getGroupMembers
solution: Experience Manager
title: getGroupMembers
topic: Scene7 Image Production System API
uuid: 02322b66-1c0c-4d84-a3eb-97a4fb605318
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 16%

---


# getGroupMembers{#getgroupmembers}

特定の会社およびグループに属するユーザーを取得します。

構文

## 認証済みユーザータイプ{#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-b798b06354c946abbb90fa72cc9c67fd}

**入力(getGroupMembersParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| ` *`groupHandle`*` | `xsd:string` |  | グループへのハンドル。 |

**出力(getGroupMembersReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`userHandleArray`*` | `type:HandleArray` | はい | ユーザーハンドルの配列。 |

## 例 {#section-aaa340dba6b64cce9bcd8303cf999166}

次のコードの例は、特定のグループに属するすべてのユーザーを含むユーザーハンドルの配列を返します。

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

