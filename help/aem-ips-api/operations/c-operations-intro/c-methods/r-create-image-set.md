---
description: 画像セットを作成します。
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic,SDK/API，画像セット
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 14%

---

# createImageSet{#createimageset}

画像セットを作成します。

構文

## 許可されたユーザーの種類 {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、宛先フォルダーに対する読み取り/書き込みアクセス権を持っている必要があります。

## パラメータ {#section-03d22ba7d290477e91c25ca1d4439200}

**入力(createImageSetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 画像セットが属する会社のハンドル。 |
| `*`folderHandle`*` | `xsd:string` | はい | フォルダーのハンドル。 |
| `*`name`*` | `xsd:string` | はい | 画像セット名。 |
| `*`type`*` | `xsd:string` | はい | 画像セットのタイプ。 |
| `*`thumbAssetHandle`*` | `xsd:string` | いいえ | 新しい画像セットのサムネールとして機能するアセットのハンドル。 指定しなかった場合、IPSはセットが参照する最初の画像アセットを使用しようとします。 |

**出力**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | はい | 新しい画像セットのハンドル。 |

## 例 {#section-385fe3b0af8044b0a2451336ec137fc5}

このコードサンプルは、会社、フォルダ、名前、タイプで指定された画像セットを作成します。 応答は、新しく作成された画像セットのアセットハンドルです。

**リクエスト**

```java
<ns1:createImageSetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:name>My Image Set</ns1:name>
   <ns1:type>ImageSet</ns1:type>
</ns1:createImageSetParam>
```

**応答**

```java
<createImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <assetHandle>25741|22|841</assetHandle>
</createImageSetReturn>
```
