---
description: プロパティセットの種類、および関連するプロパティセットとプロパティを削除します。
seo-description: プロパティセットの種類、および関連するプロパティセットとプロパティを削除します。
seo-title: deletePropertySetType
solution: Experience Manager
title: deletePropertySetType
topic: Scene7 Image Production System API
uuid: 7a5232cc-fa3a-4dac-bf88-8b954dd37c87
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deletePropertySetType{#deletepropertysettype}

プロパティセットの種類、および関連するプロパティセットとプロパティを削除します。

構文

## 認証されたユーザータイプ {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-1c8973f5d35f44b4a6a483a41609e455}

**入力(deletePropertySetTypeParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | はい | 削除するプロパティセットの種類のハンドル。 |

**出力(deletePropertySetTypeParam)**

IPS APIはこの操作に対する応答を返しません。

## 例 {#section-85faa2e3411a4e23aa6489037f7ce078}

次のコード例では、プロパティセットの種類を削除するために、IPS Webサー `deletePropertySetTypeParam` バに送信されるのフィールドとして、種類のハンドルを使用します。

**リクエスト**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**応答**

なし
