---
title: emptyAssetsFromTrash
description: IPS ゴミ箱からアセットを空にします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
TQID: 'https://experienceleague.adobe.com/y-TOHfExSc5RL9-j0f-pU6uKXWuSKSrn9SG7w0e5jPg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 6%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

IPS ゴミ箱からアセットを空にします。

Assetsは、手動で空になるまで、またはゴミ箱からタイムアウトするまで、ゴミ箱に入っています。 手動で空にした場合、最終的にシステムからパージされるまで、次のクリーンアップジョブ（通常は毎晩）までゴミ箱に入れます。 アセットがゴミ箱からタイムアウトした場合、同じクリーンアップアクティビティの一環としてアセットが削除されます。 タイムアウトは設定可能です（デフォルトは7日間）。

## 承認済みユーザータイプ {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-8e1fb0ee3aae453581e99ef76e298569}

**Input （emptyAssetsFromTrashParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | xsd:string | はい | アセットを所有する会社へのハンドル。 |
| assetHandleArray | 型:HandleArray | はい | ゴミ箱から空にするアイテムを表すハンドルの配列。 |

**Output （emptyAssetsFromTrashParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | xsd:Int | はい | ゴミ箱から正常に空になったアセットの数。 |
| warningCount | xsd:Int | はい | 操作がゴミ箱からアセットを空にしようとしたときに生成された警告の数です。 |
| errorCount | xsd:Int | はい | 操作がゴミ箱からアセットを空にしようとしたときに生成されたエラーの数です。 |
| warningDetailArray | 型:AssetOperationFaultArray | いいえ | 操作がゴミ箱から警告を空にしようとしたときに発生したアセットに関連付けられた詳細の配列。 |
| errorDetailArray | 型:AssetOperationFaultArray | いいえ | 操作がゴミ箱から空にしようとしたときにエラーを生成したアセットに関連付けられた詳細の配列。 |

## 例 {#section-6154a873b6c342bf92e2036280cafdcf}

このコードサンプルでは、会社のハンドルと、ゴミ箱から空にするアセットへのハンドルを含むアセットハンドル配列を使用します。

**リクエスト**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**応答**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```

