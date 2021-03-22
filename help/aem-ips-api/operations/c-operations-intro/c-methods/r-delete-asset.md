---
description: アセットを削除します。
seo-description: アセットを削除します。
seo-title: deleteAsset
solution: Experience Manager
title: deleteAsset
uuid: 47f700e0-04bf-4d33-a18a-d938f7e9e326
feature: Dynamic Mediaクラシック，SDK/API，アセット管理
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 11%

---


# deleteAsset{#deleteasset}

アセットを削除します。

構文

## 認証済みユーザータイプ{#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、アセットに対する読み取りおよび削除のアクセス権を持っている必要があります。

## パラメータ {#section-0eed164e278b456fbdfb7a50727a0416}

**入力(deleteAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | フォルダーが属する会社ーのハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | 削除するアセットのハンドル。 |

**出力(deleteAssetParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-d5657289f5234bb0a613dcf691507958}

このサンプルコードは、特定の会社から任意のタイプのアセットを削除します。 アセットハンドルが必要です。このハンドルは、別の操作から取得する必要があります。

**リクエスト**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**応答**

なし
