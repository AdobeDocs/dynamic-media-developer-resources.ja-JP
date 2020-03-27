---
description: グループを作成または編集します。
seo-description: グループを作成または編集します。
seo-title: saveGroup
solution: Experience Manager
title: saveGroup
topic: Scene7 Image Production System API
uuid: d1631a55-7f1d-48b4-8b35-fd5a05277219
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveGroup{#savegroup}

グループを作成または編集します。

構文

## 認証されたユーザータイプ {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-743610e98dd5494baffcbad6401038eb}

**入力(saveGroupParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 保存するグループを持つ会社のハンドル。 |
| ` *`groupHandle`*` | `xsd:string` | いいえ | グループのハンドル。 |
| ` *`name`*` | `xsd:string` | はい | グループ名。 |
| ` *`isSystemDefined`*` | `xsd:boolean` | はい | `false` がデフォルトです。 |

**出力(saveGroupReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`groupHandle`*` | `xsd:string` | はい | グループハンドル。 |

## 例 {#section-26eee227ff1f4edabb7fa1240b4d9999}

このコード例では、特定の会社に属するグループを作成します。 グループが既に存在する場合は、指定したパラメータ値で保存されます。

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

