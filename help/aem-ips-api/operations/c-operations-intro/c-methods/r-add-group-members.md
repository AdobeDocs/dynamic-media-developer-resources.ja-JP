---
description: 特定の会社から特定のグループにユーザーを追加します。
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c03525e3-6bc4-4c6a-bb5b-b0cb2e6f6d0d
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 9%

---

# addGroupMembers{#addgroupmembers}

特定の会社から特定のグループにユーザーを追加します。

構文

## 許可されているユーザータイプ {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-b28434dcf2ca4b4ea431136aac33913e}

**入力（addGroupMembersParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社へのハンドル。 |
| groupHandle | `xsd:string` | はい | グループハンドル。 |
| userHandleArray | `types:HandleArray` | はい | グループに追加するユーザーへのハンドルの配列。 |

**出力（addGroupMembersParam）**

IPS API は、この操作に対して応答を返しません。

## 例 {#section-8f168b528aef4c4fa8c3d41f7686842f}

この例では、addGroupMembersParam を使用して、1 つの会社に 1 人のユーザーを追加します。 IPS API は、この操作に対して応答を返しません。

**リクエスト**

```java {.line-numbers}
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**応答**

なし
