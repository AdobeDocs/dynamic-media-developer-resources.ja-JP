---
description: プロジェクトからアセットを削除します。 アセットを破棄しません。
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 10%

---

# removeProjectAssets{#removeprojectassets}

プロジェクトからアセットを削除します。 アセットを破棄しません。

構文

## 許可されたユーザーの種類 {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-169d8e317417415b87df86242f65710e}

**入力(removeProjectAssetsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 移動するアセットを持つ会社へのハンドル。 |
| `*`projectHandle`*` | `xsd:string` | はい | 移動するプロジェクトアセットへのハンドル。 |
| `*`assetHandleArray`*` | `types:HandleArray` | はい | 移動するアセットに対するハンドルの配列。 |

**出力(removeProjectAssetsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | はい | アセット数が正常に削除されました。 |
| `*`warningCount`*` | `xsd:int` | はい | 操作でプロジェクトからアセットを削除しようとしたときに生成される警告の数です。 |
| `*`errorCount`*` | `xsd:int` | はい | 操作がプロジェクトからアセットを削除しようとしたときに生成されたエラーの数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作によってプロジェクトから削除が試みられたときに警告が生成されたアセットに関連付けられた詳細の配列。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作によってプロジェクトから削除されたときにエラーが発生したアセットに関連付けられた詳細の配列。 |

## 例 {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

このコード例では、プロジェクトから2つのアセットを削除します（プロジェクトハンドルで指定）。

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
