---
description: IPSのごみ箱からアセットを空にします。
seo-description: IPSのごみ箱からアセットを空にします。
seo-title: emptyAssetsFromTrash
solution: Experience Manager
title: emptyAssetsFromTrash
topic: Scene7 Image Production System API
uuid: de11a7b0-cd4b-4717-8596-d39afbcf7e9c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# emptyAssetsFromTrash{#emptyassetsfromtrash}

IPSのごみ箱からアセットを空にします。

アセットは、手動で空にするか、ごみ箱からタイムアウトするまで、ごみ箱に保存されます。 手動で空にした場合は、次のクリーンアップジョブ（通常は夜間）までごみ箱に残り、最後にシステムから削除されます。 ごみ箱からタイムアウトした場合、同じクリーンアップ操作の一部としてアセットが消去されます。 タイムアウトは設定できます（デフォルトは7日間）。

## 認証されたユーザータイプ {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* ``

## パラメータ {#section-8e1fb0ee3aae453581e99ef76e298569}

**入力(emptyAssetsFromTrashParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | アセットを所有する会社のハンドル。 |
| ` *`assetHandleArray`*` | `types:HandleArray` | はい | ごみ箱から空にする項目を表すハンドルの配列です。 |

**出力(emptyAssetsFromTrashParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:Int` | はい | ごみ箱から正常に空にされたアセットの数。 |
| ` *`warningCount`*` | `xsd:Int` | はい | 操作でごみ箱からアセットを空にしようとしたときに生成された警告の数です。 |
| ` *`errorCount`*` | `xsd:Int` | はい | 操作でごみ箱からアセットを空にしようとしたときに発生したエラーの数です。 |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作でごみ箱から警告を空にしようとしたときに生成された、アセットに関連付けられた詳細の配列です。 |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作でごみ箱から削除しようとしたときにエラーが発生したアセットに関連付けられた詳細の配列です。 |

## 例 {#section-6154a873b6c342bf92e2036280cafdcf}

このコード例では、会社のハンドルと、ごみ箱から空にするアセットのハンドルを含むアセットハンドル配列を使用します。

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

