---
description: ICCプロファイルメタデータフィールドを設定します。
solution: Experience Manager
title: batchSetIccProfileFields
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 14%

---

# batchSetIccProfileFields{#batchseticcprofilefields}

ICCプロファイルメタデータフィールドを設定します。

構文

## 許可されたユーザーの種類 {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**入力(batchSetIccProfileFields)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | ICCプロファイルを含む会社に対して処理します。 |
| `*`配列の更新`*` | `xsd:string` | はい | ICCプロファイルの更新の配列。 |

**出力(batchSetIccProfileFields)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | はい | 正常に設定されたICCプロファイルフィールドの数。 |
| `*`warningCount`*` | `xsd:int` | はい | 操作がICCプロファイルフィールドの設定を試みたときに生成された警告の数です。 |
| `*`errorCount`*` | `xsd:int` | はい | 操作がICCプロファイルフィールドの設定を試みたときに生成されたエラーの数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときに警告が生成されたアセットに関連付けられた詳細の配列。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときにエラーが発生したアセットに関連付けられた詳細の配列。 |

## 例 {#section-5dc90cfbd9b1411485b44859032f7cb9}

**リクエスト**

```java
<batchSetIccProfileFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|1808|13|169</assetHandle>
         <class>Output</class>
         <colorSpace>CMYK</colorSpace>
         <pcsType>Luv</pcsType>
      </items>
   </updateArray>
</batchSetIccProfileFieldsParam>
```

**応答**

```java
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```
