---
description: 特定の企業のユーザーを特定のグループに追加します。
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c03525e3-6bc4-4c6a-bb5b-b0cb2e6f6d0d
TQID: 'https://experienceleague.adobe.com/iwy99zQOP-peI6mJgDE8bp7NGN6bjH1g5MBN53gIkJw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 9%

---

# addGroupMembers{#addgroupmembers}

特定の企業のユーザーを特定のグループに追加します。

構文

## 承認済みユーザータイプ {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-b28434dcf2ca4b4ea431136aac33913e}

**入力（addGroupMembersParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドルです。 |
| groupHandle | `xsd:string` | はい | グループハンドルです。 |
| userHandleArray | `types:HandleArray` | はい | グループに追加するユーザーに対するハンドルの配列。 |

**出力（addGroupMembersParam）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-8f168b528aef4c4fa8c3d41f7686842f}

この例では、addGroupMembersParamを使用して、ユーザーを1つの会社に追加します。 IPS APIは、この操作に対する応答を返しません。

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
