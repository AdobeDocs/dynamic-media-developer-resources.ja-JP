---
description: グループを作成または編集します。
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
TQID: 'https://experienceleague.adobe.com/VTDPxH7rjfnALgRNc-Md6NLKZfOrRk6CqQhGi0JNZs4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 17%

---

# saveGroup{#savegroup}

グループを作成または編集します。

構文

## 承認済みユーザータイプ {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-743610e98dd5494baffcbad6401038eb}

**入力（saveGroupParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 保存するグループを持つ会社へのハンドル。 |
| groupHandle | `xsd:string` | いいえ | グループへのハンドル。 |
| name | `xsd:string` | はい | グループ名： |
| isSystemDefined | `xsd:boolean` | はい | `false`が既定値です。 |

**出力（saveGroupReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| groupHandle | `xsd:string` | はい | グループハンドル： |

## 例 {#section-26eee227ff1f4edabb7fa1240b4d9999}

このコードサンプルは、特定の会社に属するグループを作成します。 グループが既に存在する場合は、指定したパラメーター値を使用して保存されます。

**リクエスト**

```java
<ns1:saveGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:name>My Other Group</ns1:name>
   <ns1:isSystemDefined>false</ns1:isSystemDefined>
</ns1:saveGroupParam>
```

**応答**

```java
<saveGroupReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupHandle>281</groupHandle>
</saveGroupReturn>
```
