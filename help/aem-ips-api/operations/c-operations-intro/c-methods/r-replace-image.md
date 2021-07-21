---
description: 画像アセットの画像データを置き換えます。
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 15%

---

# replaceImage{#replaceimage}

画像アセットの画像データを置き換えます。

構文

## 許可されたユーザーの種類 {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**入力(replaceImageParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | はい | 置き換える画像を含む会社へのハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | 置き換えるアセットのハンドル。 |
| `*`urlModifier`*` | `xsd:string` | はい | 新しい画像データを生成するImage Serverコマンド。 |

**出力(replaceImageReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | はい | 新しいアセットを処理します。 |

## 例 {#section-cebb93576bde4cb98cb27356ca66783b}

このコードサンプルは、画像を置き換え、`urlModifier`を置き換え時にImage Serverが何も実行しないことを指定するコマンドに適用します。

**リクエスト**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**応答**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```
