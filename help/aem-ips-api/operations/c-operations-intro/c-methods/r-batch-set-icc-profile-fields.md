---
description: ICCプロファイルメタデータフィールドを設定します。
seo-description: ICCプロファイルメタデータフィールドを設定します。
seo-title: batchSetIccProfileFields
solution: Experience Manager
title: batchSetIccProfileFields
topic: Scene7 Image Production System API
uuid: 163b9b36-85b6-4880-8029-8421b04f4a08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchSetIccProfileFields{#batchseticcprofilefields}

ICCプロファイルメタデータフィールドを設定します。

構文

## 認証されたユーザータイプ {#section-f6f7caf9434b4f469518dab64b76c0f4}

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
| ` *`companyHandle`*` | `xsd:string` | はい | ICCプロファイルを含む会社へのハンドル。 |
| ` *`更新配列`*` | `xsd:string` | はい | ICCプロファイルの更新の配列。 |

**出力(batchSetIccProfileFields)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | はい | 正常に設定されたICCプロファイルフィールドの数。 |
| ` *`warningCount`*` | `xsd:int` | はい | 操作がICCプロファイルフィールドの設定を試みたときに生成された警告の数です。 |
| ` *`errorCount`*` | `xsd:int` | はい | 操作がICCプロファイルフィールドの設定を試みたときに生成されたエラーの数。 |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときに警告を生成したアセットに関連付けられた詳細の配列です。 |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときにエラーが発生したアセットに関連付けられた詳細の配列です。 |

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

