---
description: ごみ箱からアセットを元に戻します。
seo-description: ごみ箱からアセットを元に戻します。
seo-title: restoreAssetsFromTrash
solution: Experience Manager
title: restoreAssetsFromTrash
topic: Scene7 Image Production System API
uuid: f7424d4c-7807-4de9-ad0c-f96364bf7b82
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 12%

---


# restoreAssetsFromTrash{#restoreassetsfromtrash}

ごみ箱からアセットを元に戻します。

構文

## 認証済みユーザータイプ{#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-200a61d040c94e489a85241b29cd499a}

**入力(restoreAssetsFromTrashParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 復元するアセットを含む会社へのハンドル。 |
| ` *`assetHandleArray`*` | `types:HandleArray` | はい | 復元するアセットのハンドルの配列。 |

**出力(restoreAssetsFromTrashReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | はい | 正常にごみ箱から削除されたアセットの数。 |
| ` *`warningCount`*` | `xsd:int` | はい | 操作がごみ箱からアセットを復元しようとしたときに生成された警告の数です。 |
| ` *`errorCount`*` | `xsd:int` | はい | ごみ箱からアセットを復元しようとしたときに発生したエラーの数。 |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作がごみ箱からアセットを復元しようとしたときに警告を生成したアセットに関連付けられた詳細の配列です。 |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作がごみ箱からアセットを復元しようとしたときにエラーが発生したアセットに関連付けられた詳細の配列です。 |

## 例 {#section-98fe0394b0634ca397c395f14f8a9358}

このコードサンプルを使用すると、ごみ箱からアセットを復元できます。 応答は、操作が正常に完了したことを示します。

**リクエスト**

```java
<restoreAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</restoreAssetsFromTrashParam>
```

**応答**

```java
<restoreAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</restoreAssetsFromTrashReturn
```

