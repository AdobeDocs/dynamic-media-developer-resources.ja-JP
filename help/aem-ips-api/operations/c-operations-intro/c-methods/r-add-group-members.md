---
description: 特定の会社のユーザーを特定のグループに追加します。
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c03525e3-6bc4-4c6a-bb5b-b0cb2e6f6d0d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 12%

---

# addGroupMembers{#addgroupmembers}

特定の会社のユーザーを特定のグループに追加します。

構文

## 認証済みユーザータイプ {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-b28434dcf2ca4b4ea431136aac33913e}

**入力 (addGroupMembersParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社への取り扱い。 |
| groupHandle | `xsd:string` | はい | グループハンドル。 |
| userHandleArray | `types:HandleArray` | はい | グループに追加するユーザーに対するハンドルの配列。 |

**出力 (addGroupMembersParam)**

IPS API はこの操作に対する応答を返しません。

## 例 {#section-8f168b528aef4c4fa8c3d41f7686842f}

この例では、 addGroupMembersParam を使用してユーザーを 1 つの会社に追加します。 IPS API はこの操作に対する応答を返しません。

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
