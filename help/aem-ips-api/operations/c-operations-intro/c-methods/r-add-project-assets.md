---
description: 1 つ以上のアセットをプロジェクトに追加します。
solution: Experience Manager
title: addProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 60aa2846-b41e-4131-b465-82aa832434f7
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 10%

---

# addProjectAssets{#addprojectassets}

1 つ以上のアセットをプロジェクトに追加します。

構文

## 許可されているユーザータイプ {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-20d498e971b6466298e60c8a77fc32b2}

**入力（addProjectAssetsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 現在のプロジェクトに関連付けられている会社を処理します。 |
| projectHandle | `xsd:string` | はい | アセットを追加するプロジェクトへのハンドル。 |
| projectHandleArray | `xsd:HandleArray` | はい | 現在のプロジェクトに追加するアセットの配列。 |

**出力（addProjectAssetsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | 正常に追加されたアセット数。 |
| warningCount | `xsd:int` | はい | 操作がアセットをプロジェクトに追加しようとしたときに生成された警告の数。 |
| errorCount | `xsd:int` | はい | 操作がアセットをプロジェクトに追加しようとしたときに生成されたエラーの数。 |
| warningDetailHandle | `xsd:AssetOperationFaultArray` | いいえ | 操作がアセットをプロジェクトに追加しようとしたときにアセットによって生成された警告の配列。 |
| companyHandle | `xsd:AssetOperationFaultArray` | いいえ | 操作がアセットをプロジェクトに追加しようとしたときにアセットによって生成されたエラーの配列。 |

## 例 {#section-bee5be2402f54cb9a3a02cc07def4135}

この例では、アセットハンドル配列内の単一のアセット（ハンドルによって参照）を、リクエストで指定されたプロジェクトに追加します。 応答 `successCount` が `1` を返したときに、操作が正常に完了しました。

**リクエスト**

```java {.line-numbers}
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**応答**

```java {.line-numbers}
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```
