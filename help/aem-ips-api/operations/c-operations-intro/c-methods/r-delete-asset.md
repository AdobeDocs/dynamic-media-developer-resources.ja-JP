---
description: アセットを削除します。
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 9%

---

# deleteAsset{#deleteasset}

アセットを削除します。

構文

## 許可されているユーザータイプ {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーには、アセットに対する読み取りおよび削除のアクセス権が必要です。

## パラメーター {#section-0eed164e278b456fbdfb7a50727a0416}

**入力（deleteAssetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | フォルダーが属する会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | 削除するアセットへのハンドル。 |

**出力（deleteAssetParam）**

IPS API は、この操作に対して応答を返しません。

## 例 {#section-d5657289f5234bb0a613dcf691507958}

このサンプルコードは、特定の会社から任意のタイプのアセットを削除します。 別の操作から取得する必要があるアセットハンドルが必要です。

**リクエスト**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**応答**

なし
