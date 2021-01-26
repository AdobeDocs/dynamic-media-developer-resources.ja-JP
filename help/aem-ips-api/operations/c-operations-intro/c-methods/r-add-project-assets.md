---
description: プロジェクトに1つ以上のアセットを追加します。
solution: Experience Manager
title: addProjectAssets
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 11%

---


# addProjectAssets{#addprojectassets}

プロジェクトに1つ以上のアセットを追加します。

構文

## 認証済みユーザータイプ{#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-20d498e971b6466298e60c8a77fc32b2}

**入力(addProjectAssetsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 現在のプロジェクトに関連付けられている会社に対するハンドル。 |
| `*`projectHandle`*` | `xsd:string` | はい | アセットを追加するプロジェクトの処理。 |
| `*`projectHandleArray`*` | `xsd:HandleArray` | はい | 現在のプロジェクトに追加するアセットの配列。 |

**出力(addProjectAssetsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | はい | 正常に追加されたアセットの数です。 |
| `*`warningCount`*` | `xsd:int` | はい | 操作がプロジェクトにアセットを追加しようとしたときに生成された警告の数です。 |
| `*`errorCount`*` | `xsd:int` | はい | 操作がプロジェクトにアセットを追加しようとしたときに生成されたエラーの数です。 |
| `*`warningDetailHandle`*` | `xsd:AssetOperationFaultArray` | いいえ | 操作がプロジェクトに追加しようとしたときにアセットによって生成された警告の配列です。 |
| `*`companyHandle`*` | `xsd:AssetOperationFaultArray` | いいえ | 操作がプロジェクトに追加しようとしたときにアセットによって生成されたエラーの配列です。 |

## 例 {#section-bee5be2402f54cb9a3a02cc07def4135}

次の使用例は、アセットハンドル配列内の1つのアセット（ハンドルで参照）を、要求で指定されたプロジェクトに追加します。 応答`successCount`が`1`を返すと、操作は正常に完了しました。

**リクエスト**

```java
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**応答**

```java
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```

