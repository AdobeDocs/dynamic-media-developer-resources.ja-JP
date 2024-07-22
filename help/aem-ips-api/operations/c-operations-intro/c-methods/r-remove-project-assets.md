---
description: プロジェクトからアセットを削除します。 アセットを破棄しません。
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 10%

---

# removeProjectAssets{#removeprojectassets}

プロジェクトからアセットを削除します。 アセットを破棄しません。

構文

## 許可されているユーザータイプ {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-169d8e317417415b87df86242f65710e}

**入力（removeProjectAssetsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 移動するアセットを含む会社へのハンドル。 |
| projectHandle | `xsd:string` | はい | 移動するプロジェクトアセットへのハンドル。 |
| assetHandleArray | `types:HandleArray` | はい | 移動するアセットへのハンドルの配列。 |

**出力（removeProjectAssetsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | アセット数が正常に削除されました。 |
| warningCount | `xsd:int` | はい | 操作がプロジェクトからアセットを削除しようとしたときに生成された警告の数。 |
| errorCount | `xsd:int` | はい | 操作がプロジェクトからアセットを削除しようとしたときに生成されたエラーの数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作がプロジェクトからアセットを削除しようとしたときに警告が発生したアセットに関連付けられた詳細の配列。 |
| errorDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作がアセットをプロジェクトから削除しようとしたときにエラーが発生したアセットに関連付けられた詳細の配列。 |

## 例 {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

このコードサンプルでは、（プロジェクトハンドルで指定された）プロジェクトから 2 つのアセットを削除します。

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
