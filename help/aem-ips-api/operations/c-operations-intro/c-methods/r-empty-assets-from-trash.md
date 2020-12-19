---
description: IPSのごみ箱からアセットを削除します。
seo-description: IPSのごみ箱からアセットを削除します。
seo-title: emptyAssetsFromTrash
solution: Experience Manager
title: emptyAssetsFromTrash
topic: Scene7 Image Production System API
uuid: de11a7b0-cd4b-4717-8596-d39afbcf7e9c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 7%

---


# emptyAssetsFromTrash{#emptyassetsfromtrash}

IPSのごみ箱からアセットを削除します。

アセットは、手動で空にするか、ごみ箱からタイムアウトするまで、ごみ箱に入ります。 手動で空にした場合は、最後にシステムから削除される次のクリーンアップジョブ（通常は夜間）までごみ箱に入ります。 ごみ箱からタイムアウトした場合、同じクリーンアップアクティビティの一部として、アセットが消去されます。 タイムアウトは設定できます（デフォルトは7日間）。

## 認証済みユーザータイプ{#section-24dee2bf5f9f4714a64955c80f2803b4}

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
| ` *`companyHandle`*` | `xsd:string` | はい | アセットを所有する会社へのハンドル。 |
| ` *`assetHandleArray`*` | `types:HandleArray` | はい | ごみ箱から空にする項目を表すハンドルの配列です。 |

**出力(emptyAssetsFromTrashParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:Int` | はい | ごみ箱から正常に空にされたアセットの数です。 |
| ` *`warningCount`*` | `xsd:Int` | はい | 操作がごみ箱からアセットを空にしようとしたときに生成される警告の数です。 |
| ` *`errorCount`*` | `xsd:Int` | はい | 操作がごみ箱からアセットを空にしようとしたときに生成されたエラーの数です。 |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作でごみ箱から削除しようとしたときに警告を生成したアセットに関連付けられた詳細の配列です。 |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作でアセットをごみ箱から削除しようとしたときにエラーが発生した、アセットに関連付けられた詳細の配列です。 |

## 例 {#section-6154a873b6c342bf92e2036280cafdcf}

このコードのサンプルでは、会社のハンドルと、ごみ箱から空にするアセットのハンドルを含むアセットハンドルの配列を使用します。

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

