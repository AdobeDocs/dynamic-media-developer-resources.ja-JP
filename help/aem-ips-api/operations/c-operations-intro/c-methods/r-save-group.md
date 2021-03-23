---
description: グループを作成または編集します。
seo-description: グループを作成または編集します。
seo-title: saveGroup
solution: Experience Manager
title: saveGroup
uuid: d1631a55-7f1d-48b4-8b35-fd5a05277219
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 18%

---


# saveGroup{#savegroup}

グループを作成または編集します。

構文

## 認証済みユーザータイプ{#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-743610e98dd5494baffcbad6401038eb}

**入力(saveGroupParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 保存するグループを持つ会社へのハンドル。 |
| `*`groupHandle`*` | `xsd:string` | いいえ | グループへのハンドル。 |
| `*`name`*` | `xsd:string` | はい | グループ名。 |
| `*`isSystemDefined`*` | `xsd:boolean` | はい | `false` がデフォルトです。 |

**出力(saveGroupReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`groupHandle`*` | `xsd:string` | はい | グループハンドル |

## 例 {#section-26eee227ff1f4edabb7fa1240b4d9999}

このコードのサンプルを使用すると、特定の会社に属するグループを作成できます。 グループが既に存在する場合は、指定したパラメータ値で保存されます。

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

