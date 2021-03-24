---
description: フォントメタデータフィールドを設定します。
solution: Experience Manager
title: batchSetFontFields
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 14%

---


# batchSetFontFields{#batchsetfontfields}

フォントメタデータフィールドを設定します。

## 認証済みユーザータイプ{#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-836f5948d00a46e98ccb62f0573e4e68}

**入力(batchSetFontFieldsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | フォントを含む会社へのハンドル。 |
| `*`updateArray`*` | `types:FontFieldUpdateArray` | はい | フォントフィールドの更新の配列。 |

**出力(batchSetFontFieldsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | はい | 正常に設定されたフォントフィールドの数です。 |
| `*`warningCount`*` | `xsd:int` | はい | 操作がフォントフィールドの設定を試行したときに生成された警告の数です。 |
| `*`errorCount`*` | `xsd:int` | はい | 操作がフォントフィールドの設定を試行したときに生成されたエラーの数です。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときに警告を生成したアセットに関連付けられた詳細の配列です。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときにエラーが発生したアセットに関連付けられた詳細の配列です。 |

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

