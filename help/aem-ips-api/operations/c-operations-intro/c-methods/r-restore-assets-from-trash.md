---
description: アセットをゴミ箱から復元します。
solution: Experience Manager
title: restoreAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b1cde1a9-d726-4ebc-9d49-ee72a6b56fc9
TQID: 'https://experienceleague.adobe.com/VeC7td4UAm7HX4azZATUoBf-ZLS00aF7OOipZqmVbdw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 10%

---

# restoreAssetsFromTrash{#restoreassetsfromtrash}

アセットをゴミ箱から復元します。

構文

## 承認済みユーザータイプ {#section-15e887782c7d4ace897ff02c6ad5baa0}

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
| successCount | `xsd:int` | はい | 正常にゴミ箱から削除されたアセットの数。 |
| warningCount | `xsd:int` | はい | 操作がゴミ箱からアセットを復元しようとしたときに生成された警告の数。 |
| errorCount | `xsd:int` | はい | ゴミ箱からアセットを復元しようとしたときに生成されたエラーの数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作がアセットをごみ箱から復元しようとしたときに警告を生成したアセットに関連付けられた詳細の配列。 |
| errorDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作がアセットをごみ箱から復元しようとしたときにエラーを生成したアセットに関連付けられた詳細の配列。 |

## 例 {#section-98fe0394b0634ca397c395f14f8a9358}

このコードサンプルは、アセットをゴミ箱から復元します。 応答は、操作が正常に完了したことを示します。

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
