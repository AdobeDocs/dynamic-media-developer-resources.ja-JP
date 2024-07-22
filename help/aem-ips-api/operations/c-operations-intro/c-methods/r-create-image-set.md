---
description: 画像セットを作成します。
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 13%

---

# createImageSet{#createimageset}

画像セットを作成します。

構文

## 許可されているユーザータイプ {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーには、宛先フォルダーに対する読み取り/書き込みアクセス権が必要です。

## パラメーター {#section-03d22ba7d290477e91c25ca1d4439200}

**入力（createImageSetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 画像セットが属する会社のハンドル。 |
| folderHandle | `xsd:string` | はい | フォルダーへのハンドル。 |
| name | `xsd:string` | はい | 画像セット名。 |
| タイプ | `xsd:string` | はい | 画像セットのタイプ |
| thumbAssetHandle | `xsd:string` | いいえ | 新しい画像セットのサムネールとして機能するアセットのハンドル。 指定しない場合、IPS はセットによって参照される最初の画像アセットを使用しようとします。 |

**出力**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| assetHandle | `xsd:string` | はい | 新しい画像セットへのハンドル。 |

## 例 {#section-385fe3b0af8044b0a2451336ec137fc5}

このコードサンプルでは、会社、フォルダー、名前およびタイプで指定された画像セットを作成します。 応答は、新しく作成された画像セットのアセットハンドルです。

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
