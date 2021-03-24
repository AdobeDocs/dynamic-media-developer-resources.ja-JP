---
description: アセットを特定のフォルダーに移動します。
solution: Experience Manager
title: moveAsset
feature: Dynamic Mediaクラシック，SDK/API，アセット管理
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 15%

---


# moveAsset{#moveasset}

アセットを特定のフォルダーに移動します。

構文

## 認証済みユーザータイプ{#section-e4f2d2a58132450aa36da6377134211e}

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
| `*`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | 移動するアセットのハンドル。 |
| `*`folderHandle`*` | `xsd:string` | はい | 宛先フォルダーへのハンドル。 |

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
