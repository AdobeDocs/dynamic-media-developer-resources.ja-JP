---
description: 画像セットを作成します。
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
TQID: 'https://experienceleague.adobe.com/os4DfkGa5cTZfMN1vc5HeA8Qvauvwb5Q0dZ2P3HFI-c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 13%

---

# createImageSet{#createimageset}

画像セットを作成します。

構文

## 承認済みユーザータイプ {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、宛先フォルダーへの読み取り/書き込みアクセス権を持っている必要があります。

## パラメーター {#section-03d22ba7d290477e91c25ca1d4439200}

**入力（createImageSetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 画像セットが属する会社へのハンドル。 |
| folderHandle | `xsd:string` | はい | フォルダーへのハンドル。 |
| name | `xsd:string` | はい | 画像セット名。 |
| タイプ | `xsd:string` | はい | 画像セットの種類： |
| thumbAssetHandle | `xsd:string` | いいえ | 新しい画像セットのサムネールとして機能するアセットのハンドル。 指定しない場合、IPSはセットで参照される最初の画像アセットを使用しようとします。 |

**出力**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| assetHandle | `xsd:string` | はい | 新しい画像セットへのハンドル。 |

## 例 {#section-385fe3b0af8044b0a2451336ec137fc5}

このコードサンプルは、会社、フォルダー、名前、タイプで指定された画像セットを作成します。 応答は、新しく作成された画像セットのアセットハンドルです。

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

