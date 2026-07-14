---
description: ICC プロファイルメタデータフィールドを設定します。
solution: Experience Manager
title: batchSetIccProfileFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
TQID: 'https://experienceleague.adobe.com/YmeLGJ9N-W-JOU7oG7utN4d1Q2pV17wtqocdrwYD-lQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 12%

---

# batchSetIccProfileFields{#batchseticcprofilefields}

ICC プロファイルメタデータフィールドを設定します。

構文

## 承認済みユーザータイプ {#section-f6f7caf9434b4f469518dab64b76c0f4}

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
| companyHandle | `xsd:string` | はい | ICC プロファイルを含む会社に対して処理します。 |
| 配列を更新 | `xsd:string` | はい | ICC プロファイルの更新の配列。 |

**Output （batchSetIccProfileFields）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | ICC プロファイルフィールドを正常に設定した数。 |
| warningCount | `xsd:int` | はい | 操作がICC プロファイルフィールドを設定しようとしたときに生成された警告の数。 |
| errorCount | `xsd:int` | はい | 操作がICC プロファイルフィールドを設定しようとしたときに生成されたエラーの数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときに警告を生成したアセットに関連付けられた詳細の配列。 |
| errorDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときにエラーを生成したアセットに関連付けられた詳細の配列。 |

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

