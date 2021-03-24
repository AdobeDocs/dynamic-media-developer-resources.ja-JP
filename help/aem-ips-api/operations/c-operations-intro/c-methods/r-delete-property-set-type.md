---
description: プロパティセットの種類、および関連するプロパティセットとプロパティを削除します。
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 11%

---


# deletePropertySetType{#deletepropertysettype}

プロパティセットの種類、および関連するプロパティセットとプロパティを削除します。

構文

## 認証済みユーザータイプ{#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-1c8973f5d35f44b4a6a483a41609e455}

**入力(deletePropertySetTypeParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | はい | 削除するプロパティセットの種類のハンドル。 |

**出力(deletePropertySetTypeParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-85faa2e3411a4e23aa6489037f7ce078}

このコードの例では、プロパティセットの種類を削除するために、IPS Webサービスサーバーに送信される`deletePropertySetTypeParam`内のフィールドとして、種類のハンドルを使用します。

**リクエスト**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**応答**

なし
