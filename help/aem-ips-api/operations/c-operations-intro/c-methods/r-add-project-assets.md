---
description: プロジェクトに1つ以上のアセットを追加します。
solution: Experience Manager
title: addProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 60aa2846-b41e-4131-b465-82aa832434f7
TQID: 'https://experienceleague.adobe.com/-Oxu138gsQfcPHJ40r8zBEis4AIlNua-gU9DmrGmpF0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 178
ht-degree: 10%

---

# addProjectAssets{#addprojectassets}

プロジェクトに1つ以上のアセットを追加します。

構文

## 承認済みユーザータイプ {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

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
| companyHandle | `xsd:string` | はい | 現在のプロジェクトに関連付けられている会社に対する処理。 |
| projectHandle | `xsd:string` | はい | アセットを追加するプロジェクトを処理します。 |
| projectHandleArray | `xsd:HandleArray` | はい | 現在のプロジェクトに追加するアセットの配列。 |

**出力（addProjectAssetsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | 正常に追加されたアセットの数。 |
| warningCount | `xsd:int` | はい | 操作がアセットをプロジェクトに追加しようとしたときに生成された警告の数です。 |
| errorCount | `xsd:int` | はい | 操作がプロジェクトにアセットを追加しようとしたときに生成されたエラーの数。 |
| warningDetailHandle | `xsd:AssetOperationFaultArray` | いいえ | 操作がアセットをプロジェクトに追加しようとしたときにアセットによって生成された警告の配列。 |
| companyHandle | `xsd:AssetOperationFaultArray` | いいえ | 操作がアセットをプロジェクトに追加しようとしたときにアセットによって生成されたエラーの配列。 |

## 例 {#section-bee5be2402f54cb9a3a02cc07def4135}

次の使用例は、アセットハンドル配列内の1つのアセット（ハンドルで参照）を、リクエストで指定されたプロジェクトに追加します。 応答`successCount`が`1`を返すと、操作は正常に完了しました。

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
