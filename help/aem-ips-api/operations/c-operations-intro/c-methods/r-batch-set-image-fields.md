---
description: 1つまたは複数の画像アセットの画像固有のフィールドを設定します。
solution: Experience Manager
title: batchSetImageFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
TQID: 'https://experienceleague.adobe.com/J3mCGBUY4Ws5Wq18tHWrHQJNElW5gYvwSQ2yKF-NhsM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 8%

---

# batchSetImageFields{#batchsetimagefields}

1つまたは複数の画像アセットの画像固有のフィールドを設定します。

構文

## 承認済みユーザータイプ {#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-4969815cf67c4d11b13bb2017b3604e8}

**入力（batchSetImageFields）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 画像アセットを含む会社へのハンドル。 |
| updateArray | `types:ImageFieldUpdateArray` | はい | 画像フィールドの配列が更新されます。 |

**Output （batchSetImageFields）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | 正常に設定された画像フィールドの数。 |
| warningCount | `xsd:int` | はい | 操作が画像フィールドを設定しようとしたときに生成された警告の数です。 |
| errorCount | `xsd:int` | はい | 操作が画像フィールドを設定しようとしたときに生成されたエラーの数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときに警告を生成したアセットに関連付けられた詳細の配列。 |
| errorDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときにエラーを生成したアセットに関連付けられた詳細の配列。 |

## 例 {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

次の使用例は、更新配列内の2つの画像のフィールドにデータを設定します。 配列では、画像はアセットハンドルで指定され、ピクセル、x位置およびy位置のアンカー座標、ユーザーデータの解像度が含まれます。 応答は、両方の画像のフィールドが正常に設定されたことを示します。

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
