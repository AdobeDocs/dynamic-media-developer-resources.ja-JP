---
description: ICC プロファイルメタデータフィールドを設定します。
solution: Experience Manager
title: batchSetIccProfileFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 12%

---

# batchSetIccProfileFields{#batchseticcprofilefields}

ICC プロファイルメタデータフィールドを設定します。

構文

## 許可されているユーザータイプ {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**入力（batchSetIccProfileFields）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | ICC プロファイルを含む会社へのハンドル。 |
| 配列を更新 | `xsd:string` | はい | ICC プロファイルのアップデートの配列。 |

**出力（batchSetIccProfileFields）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | 正常に設定された ICC プロファイル フィールドの数です。 |
| warningCount | `xsd:int` | はい | 操作が ICC プロファイルフィールドを設定しようとしたときに生成された警告の数。 |
| errorCount | `xsd:int` | はい | 操作が ICC プロファイル フィールドを設定しようとしたときに生成されたエラーの数です。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとした際に警告を生成したアセットに関連付けられた詳細の配列。 |
| errorDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときにエラーが発生したアセットに関連付けられた詳細の配列です。 |

## 例 {#section-5dc90cfbd9b1411485b44859032f7cb9}

**リクエスト**

```java {.line-numbers}
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

```java {.line-numbers}
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```
