---
description: フォントメタデータフィールドを設定します。
solution: Experience Manager
title: batchSetFontFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f38aa861-2a81-4663-967e-72611122f51b
TQID: 'https://experienceleague.adobe.com/IkKqBLa2j-YKPTp5Nsttxb8GgpPgcSee1zG0asjxNyQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 12%

---

# batchSetFontFields{#batchsetfontfields}

フォントメタデータフィールドを設定します。

## 承認済みユーザータイプ {#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-836f5948d00a46e98ccb62f0573e4e68}

**入力（batchSetFontFieldsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | フォントを含む会社に対して処理を行います。 |
| updateArray | `types:FontFieldUpdateArray` | はい | フォントフィールド更新の配列。 |

**Output （batchSetFontFieldsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | フォントフィールドを正常に設定した数。 |
| warningCount | `xsd:int` | はい | 操作がフォントフィールドを設定しようとしたときに生成された警告の数。 |
| errorCount | `xsd:int` | はい | 操作がフォントフィールドを設定しようとしたときに生成されたエラーの数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときに警告を生成したアセットに関連付けられた詳細の配列。 |
| errorDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときにエラーを生成したアセットに関連付けられた詳細の配列。 |

## 例 {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**リクエスト**

```javascript {.line-numbers}
<batchSetFontFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
          <assetHandle>a|450|14|19</assetHandle>
          <fontName>Bookman Old Style Font Name</fontName>
          <postscriptName>Bookman Old Style PostScript</postscriptName>
          <rtfName>Bookman Old Style RTF</rtfName>
          <fontFamily>Bookman Old Style Family</fontFamily>
          <style>BoldItalic</style>
          <typeName>Open Type</typeName><type>OTF</type>
      </items>
   </updateArray>
</batchSetFontFieldsParam>
```

**応答**

```javascript {.line-numbers}
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```

