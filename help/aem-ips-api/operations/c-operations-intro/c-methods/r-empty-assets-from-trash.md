---
title: emptyAssetsFromTrash
description: IPS のごみ箱からアセットを削除します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 7%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

IPS のごみ箱からアセットを削除します。

アセットは、手動で空にするか、ごみ箱からタイムアウトするまで、ごみ箱に入っています。 手動で空にした場合は、次のクリーンアップジョブ（通常は夜間）が最後にシステムからパージされるまで、ごみ箱に入ります。 ごみ箱からタイムアウトした場合、同じクリーンアップアクティビティの一環として、アセットが消去されます。 タイムアウトは設定できます（デフォルトは 7 日）。

## 認証済みユーザータイプ {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-8e1fb0ee3aae453581e99ef76e298569}

**入力 (emptyAssetsFromTrashParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | xsd:string | はい | アセットを所有する会社へのハンドル。 |
| assetHandleArray | types:HandleArray | はい | ごみ箱から削除する項目を表すハンドルの配列。 |

**出力 (emptyAssetsFromTrashParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | xsd:Int | はい | ごみ箱から正常に削除されたアセットの数。 |
| warningCount | xsd:Int | はい | 操作でごみ箱からアセットを空にしようとしたときに生成される警告の数です。 |
| errorCount | xsd:Int | はい | 操作でごみ箱からアセットを空にしようとした際に生成されたエラーの数。 |
| warningDetailArray | types:AssetOperationFaultArray | いいえ | 操作でごみ箱から削除しようとしたときに警告が発生したアセットに関連付けられた詳細の配列。 |
| errorDetailArray | types:AssetOperationFaultArray | いいえ | 操作でごみ箱からアセットを空にしようとした際にエラーが発生したアセットに関連付けられた詳細の配列。 |

## 例 {#section-6154a873b6c342bf92e2036280cafdcf}

このコードサンプルは、会社のハンドルと、ごみ箱から空にするアセットへのハンドルを含むアセットハンドル配列を使用します。

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
