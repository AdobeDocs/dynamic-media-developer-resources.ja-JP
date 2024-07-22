---
description: グループを作成または編集します。
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 17%

---

# saveGroup{#savegroup}

グループを作成または編集します。

構文

## 許可されているユーザータイプ {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-743610e98dd5494baffcbad6401038eb}

**入力（saveGroupParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 保存するグループを持つ会社へのハンドル。 |
| groupHandle | `xsd:string` | いいえ | グループへのハンドル。 |
| name | `xsd:string` | はい | グループ名。 |
| isSystemDefined | `xsd:boolean` | はい | デフォルトは `false` です。 |

**出力（saveGroupReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| groupHandle | `xsd:string` | はい | グループハンドル。 |

## 例 {#section-26eee227ff1f4edabb7fa1240b4d9999}

このコードサンプルでは、特定の会社に属するグループを作成します。 グループが既に存在する場合は、指定したパラメーター値で保存されます。

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
