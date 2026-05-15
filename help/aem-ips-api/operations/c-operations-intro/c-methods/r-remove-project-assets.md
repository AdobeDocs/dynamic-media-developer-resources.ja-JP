---
description: プロジェクトからアセットを削除します。 アセットを破棄しない。
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
TQID: 'https://experienceleague.adobe.com/GHGyYEF5H3Me5jKtkfd15Ok8KEk2hrRuVxrKCF7cZ-E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 179
ht-degree: 10%

---

# removeProjectAssets{#removeprojectassets}

プロジェクトからアセットを削除します。 アセットを破棄しない。

構文

## 承認済みユーザータイプ {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-169d8e317417415b87df86242f65710e}

**入力（removeProjectAssetsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 移動するアセットを持つ会社へのハンドル。 |
| projectHandle | `xsd:string` | はい | 移動するプロジェクトアセットへのハンドル。 |
| assetHandleArray | `types:HandleArray` | はい | 移動するアセットへのハンドルの配列。 |

**出力（removeProjectAssetsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | アセット数が正常に削除されました。 |
| warningCount | `xsd:int` | はい | 操作がプロジェクトからアセットを削除しようとしたときに生成された警告の数。 |
| errorCount | `xsd:int` | はい | 操作がプロジェクトからアセットを削除しようとしたときに生成されたエラーの数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作がプロジェクトから警告を削除しようとしたときに警告を生成したアセットに関連付けられている詳細の配列。 |
| errorDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作がプロジェクトから削除しようとしたときにエラーを生成したアセットに関連付けられた詳細の配列。 |

## 例 {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

このコードサンプルは、プロジェクト（プロジェクトハンドルで指定）から2つのアセットを削除します。

**リクエスト**

```java
<removeProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
      <items>a|739|1|537</items>
   </assetHandleArray>
</removeProjectAssetsParam>
```
