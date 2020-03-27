---
description: 1つ以上のアセットをプロジェクトに追加します。
seo-description: 1つ以上のアセットをプロジェクトに追加します。
seo-title: addProjectAssets
solution: Experience Manager
title: addProjectAssets
topic: Scene7 Image Production System API
uuid: 48abea17-058e-4469-bb16-0abee8ef5214
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addProjectAssets{#addprojectassets}

1つ以上のアセットをプロジェクトに追加します。

構文

## 認証されたユーザータイプ {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

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
| ` *`companyHandle`*` | `xsd:string` | はい | 現在のプロジェクトに関連付けられている会社に対する処理。 |
| ` *`projectHandle`*` | `xsd:string` | はい | アセットを追加するプロジェクトの処理。 |
| ` *`projectHandleArray`*` | `xsd:HandleArray` | はい | 現在のプロジェクトに追加するアセットの配列。 |

**出力(addProjectAssetsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | はい | 正常に追加されたアセットの数。 |
| ` *`warningCount`*` | `xsd:int` | はい | 操作でプロジェクトにアセットを追加しようとしたときに生成された警告の数です。 |
| ` *`errorCount`*` | `xsd:int` | はい | 操作がプロジェクトにアセットを追加しようとしたときに生成されたエラーの数です。 |
| ` *`warningDetailHandle`*` | `xsd:AssetOperationFaultArray` | いいえ | 操作でプロジェクトに追加しようとしたときに、アセットによって生成された警告の配列です。 |
| ` *`companyHandle`*` | `xsd:AssetOperationFaultArray` | いいえ | 操作でプロジェクトに追加しようとしたときに、アセットによって生成されたエラーの配列です。 |

## 例 {#section-bee5be2402f54cb9a3a02cc07def4135}

次の例では、アセットハンドル配列内の1つのアセット（ハンドルで参照）を、要求で指定されたプロジェクトに追加します。 応答が返されると、操作は正常に完了し `successCount` まし `1`た。

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

