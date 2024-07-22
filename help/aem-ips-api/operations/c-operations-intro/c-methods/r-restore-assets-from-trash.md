---
description: ごみ箱からアセットを復元します。
solution: Experience Manager
title: restoreAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b1cde1a9-d726-4ebc-9d49-ee72a6b56fc9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 10%

---

# restoreAssetsFromTrash{#restoreassetsfromtrash}

ごみ箱からアセットを復元します。

構文

## 許可されているユーザータイプ {#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-200a61d040c94e489a85241b29cd499a}

**入力（restoreAssetsFromTrashParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 復元するアセットを持つ会社へのハンドル。 |
| assetHandleArray | `types:HandleArray` | はい | 復元するアセットのハンドルの配列。 |

**出力（restoreAssetsFromTrashReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | ごみ箱から正常に削除されたアセットの数。 |
| warningCount | `xsd:int` | はい | 操作がごみ箱からアセットを復元しようとしたときに生成された警告の数。 |
| errorCount | `xsd:int` | はい | ごみ箱からアセットを復元しようとしたときに生成されたエラーの数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作がごみ箱からアセットを復元しようとした際に警告を生成した、アセットに関連付けられている詳細の配列。 |
| errorDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作がごみ箱からアセットを復元しようとした際にエラーが発生したアセットに関連付けられている詳細の配列。 |

## 例 {#section-98fe0394b0634ca397c395f14f8a9358}

このコードサンプルでは、ごみ箱からアセットを復元します。 応答は、操作が正常に完了したことを示します。

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
