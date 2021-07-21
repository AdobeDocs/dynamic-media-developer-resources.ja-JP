---
description: アセットを特定のフォルダーに移動します。
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: c5357c1a-92ac-4f9c-957e-b62cb812796c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 15%

---

# moveAsset{#moveasset}

アセットを特定のフォルダーに移動します。

構文

## 許可されたユーザーの種類 {#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-dd0bbdf293aa4563af70a91f97c861f1}

**入力(moveAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社に取り扱う。 |
| `*`assetHandle`*` | `xsd:string` | はい | 移動するアセットに対して処理します。 |
| `*`folderHandle`*` | `xsd:string` | はい | 宛先フォルダーを処理します。 |

**出力(moveAssetReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-78333769f4f14e2886fdf06433c9d2ad}

このコードサンプルを使用すると、アセットをフォルダーに移動できます。

**リクエスト**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**応答**

なし
