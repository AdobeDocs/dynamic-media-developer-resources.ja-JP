---
description: フォントメタデータフィールドを設定します。
seo-description: フォントメタデータフィールドを設定します。
seo-title: batchSetFontFields
solution: Experience Manager
title: batchSetFontFields
topic: Scene7 Image Production System API
uuid: 0209865e-32b3-4bea-a508-05771a0365e1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchSetFontFields{#batchsetfontfields}

フォントメタデータフィールドを設定します。

## 認証されたユーザータイプ {#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-836f5948d00a46e98ccb62f0573e4e68}

**入力(batchSetFontFieldsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | フォントを含む会社のハンドル。 |
| ` *`updateArray`*` | `types:FontFieldUpdateArray` | はい | フォントフィールドの更新の配列。 |

**出力(batchSetFontFieldsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | はい | 正常に設定されたフォントフィールドの数です。 |
| ` *`warningCount`*` | `xsd:int` | はい | 操作がフォントフィールドを設定しようとしたときに生成された警告の数です。 |
| ` *`errorCount`*` | `xsd:int` | はい | 操作がフォントフィールドの設定を試みたときに生成されたエラーの数。 |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときに警告を生成したアセットに関連付けられた詳細の配列です。 |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときにエラーが発生したアセットに関連付けられた詳細の配列です。 |

## 例 {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**リクエスト**

```java
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

```java
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```

