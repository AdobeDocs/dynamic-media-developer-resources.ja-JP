---
description: 特定の会社のユーザーを特定のグループに追加します。
seo-description: 特定の会社のユーザーを特定のグループに追加します。
seo-title: addGroupMembers
solution: Experience Manager
title: addGroupMembers
topic: Scene7 Image Production System API
uuid: 382d36a8-7c93-48e6-a54b-425c5e6414fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addGroupMembers{#addgroupmembers}

特定の会社のユーザーを特定のグループに追加します。

構文

## 認証されたユーザータイプ {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-b28434dcf2ca4b4ea431136aac33913e}

**入力(addGroupMembersParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社の取っ手。 |
| ` *`groupHandle`*` | `xsd:string` | はい | グループハンドル。 |
| ` *`userHandleArray`*` | `types:HandleArray` | はい | グループに追加するユーザーのハンドルの配列です。 |

**出力(addGroupMembersParam)**

IPS APIはこの操作に対する応答を返しません。

## 例 {#section-8f168b528aef4c4fa8c3d41f7686842f}

この例では、 ` *`addGroupMembersParamを使用して`*` 、ユーザーを1つの会社に追加します。 IPS APIはこの操作に対する応答を返しません。

**リクエスト**

```java
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**応答**

なし
