---
description: IPSのごみ箱からアセットを空にします。
solution: Experience Manager
title: emptyAssetsFromTrash
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 7%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

IPSのごみ箱からアセットを空にします。

アセットは、手動で空にするか、ごみ箱からタイムアウトするまで、ごみ箱に格納されます。 手動で空にした場合は、最終的にシステムからパージされる次のクリーンアップジョブ（通常は夜間）まで、ゴミ箱に入ります。 ごみ箱からタイムアウトした場合、同じクリーンアップアクティビティの一環としてアセットが消去されます。 タイムアウトは設定できます（デフォルトは7日）。

## 許可されたユーザーの種類 {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## パラメータ {#section-8e1fb0ee3aae453581e99ef76e298569}

**入力(emptyAssetsFromTrashParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | アセットを所有する会社へのハンドル。 |
| `*`assetHandleArray`*` | `types:HandleArray` | はい | ごみ箱から空にする項目を表すハンドルの配列。 |

**出力(emptyAssetsFromTrashParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:Int` | はい | 正常にごみ箱から空にされたアセットの数。 |
| `*`warningCount`*` | `xsd:Int` | はい | 操作でごみ箱からアセットを空にしようとしたときに生成される警告の数です。 |
| `*`errorCount`*` | `xsd:Int` | はい | 操作でごみ箱からアセットを空にしようとしたときに生成されたエラーの数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作でごみ箱から削除しようとしたときに警告が生成されたアセットに関連付けられた詳細の配列。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作でアセットをごみ箱から空にしようとしたときにエラーが発生したアセットに関連付けられた詳細の配列。 |

## 例 {#section-6154a873b6c342bf92e2036280cafdcf}

このコードサンプルは、会社のハンドルと、ごみ箱から空にするアセットへのハンドルを含むアセットハンドル配列を使用します。

**リクエスト**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**応答**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
