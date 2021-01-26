---
description: プロジェクトからアセットを削除します。 アセットを破棄しません。
seo-description: プロジェクトからアセットを削除します。 アセットを破棄しません。
seo-title: removeProjectAssets
solution: Experience Manager
title: removeProjectAssets
topic: Dynamic Media Image Production System API
uuid: bae09dc3-4328-4264-8fb2-e4f0c53546eb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 10%

---


# removeProjectAssets{#removeprojectassets}

プロジェクトからアセットを削除します。 アセットを破棄しません。

構文

## 認証済みユーザータイプ{#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-169d8e317417415b87df86242f65710e}

**入力(removeProjectAssetsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 移動するアセットを含む会社へのハンドル。 |
| `*`projectHandle`*` | `xsd:string` | はい | 移動するプロジェクトアセットのハンドル。 |
| `*`assetHandleArray`*` | `types:HandleArray` | はい | 移動するアセットに対するハンドルの配列。 |

**出力(removeProjectAssetsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | はい | アセット数が正常に削除されました。 |
| `*`warningCount`*` | `xsd:int` | はい | 操作がプロジェクトからアセットを削除しようとしたときに生成された警告の数です。 |
| `*`errorCount`*` | `xsd:int` | はい | 操作がプロジェクトからアセットを削除しようとしたときに生成されたエラーの数です。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作でプロジェクトから警告を削除しようとしたときに生成された、アセットに関連付けられた詳細の配列です。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作がプロジェクトからアセットを削除しようとしたときにエラーが発生した、アセットに関連付けられた詳細の配列です。 |

## 例 {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

次のコードのサンプルを使用すると、プロジェクトから2つのアセットを削除できます（プロジェクトハンドルで指定）。

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

