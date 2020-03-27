---
description: 画像セットを更新します。
seo-description: 画像セットを更新します。
seo-title: updateImageSet
solution: Experience Manager
title: updateImageSet
topic: Scene7 Image Production System API
uuid: df118ba3-d86f-4005-928e-76a5a9f899fc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateImageSet{#updateimageset}

画像セットを更新します。

構文

## パラメータ {#section-3be47dbbce474ce78676b05e163492e3}

**入力(updateImageSetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 変更する画像セットを含む会社のハンドル。 |
| ` *`assetHandle`*` | `xsd:string` | はい | 変更する画像セットのハンドル。 |
| ` *`memberArray`*` | `types:ImageSetMemberUpdateArray` | いいえ | 画像セットのメンバをリセットします。 |
| ` *`thumbAssetHandle`*` | `xsd:string` | いいえ | 画像セットのサムネールとして機能するアセットのハンドル。 |

**出力(updateImageSetReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`シーケンス`*` |  |  |  |

## 例 {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**リクエスト**

```java
<updateImageSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|381</assetHandle> 
  <memberArray> 
    <items> 
      <assetHandle>a|374</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|375</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|376</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
  </memberArray> 
  <thumbAssetHandle>a|376</thumbAssetHandle> 
</updateImageSetParam>
```

**応答**

```java
<updateImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

