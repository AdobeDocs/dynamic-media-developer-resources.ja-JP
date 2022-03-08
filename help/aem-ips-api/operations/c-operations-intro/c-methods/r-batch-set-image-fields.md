---
description: 1 つ以上の画像アセットの画像固有のフィールドを設定します。
solution: Experience Manager
title: batchSetImageFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 10%

---

# batchSetImageFields{#batchsetimagefields}

1 つ以上の画像アセットの画像固有のフィールドを設定します。

構文

## 認証済みユーザータイプ {#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-4969815cf67c4d11b13bb2017b3604e8}

**入力 (batchSetImageFields)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 画像アセットを含む会社へのハンドル。 |
| updateArray | `types:ImageFieldUpdateArray` | はい | 画像フィールドの配列が更新されます。 |

**出力 (batchSetImageFields)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | 正常に設定された画像フィールドの数。 |
| warningCount | `xsd:int` | はい | 操作が画像フィールドの設定を試みたときに生成された警告の数です。 |
| errorCount | `xsd:int` | はい | 操作が画像フィールドの設定を試行した際に生成されたエラーの数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときに警告が生成されたアセットに関連付けられた詳細の配列。 |
| errorDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときにエラーが発生したアセットに関連付けられた詳細の配列。 |

## 例 {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

次の例では、更新配列の 2 つの画像のフィールドにデータを設定します。 この配列では、画像はアセットハンドルで指定され、ピクセル単位の解像度、X 位置および Y 位置のアンカー座標およびユーザーデータを含みます。 応答は、両方の画像のフィールドが正常に設定されたことを示します。

**リクエスト**

```java
<batchSetImageFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|140626|1|102524</assetHandle>
         <resolution>72</resolution>
         <anchorX>50</anchorX>
         <anchorY>100</anchorY>
         <userData>nada1</userData>
      </items>
      <items>
         <assetHandle>a|96680|1|64865</assetHandle>
         <resolution>150</resolution>
         <anchorX>100</anchorX>
         <anchorY>50</anchorY>
         <userData>nada2</userData>
      </items>
   </updateArray>
</batchSetImageFieldsParam>
```

**応答**

```java
<batchSetImageFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetImageFieldsReturn>
```
