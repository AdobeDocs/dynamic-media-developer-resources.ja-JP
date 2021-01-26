---
description: 1つ以上の画像アセットに対して、画像固有のフィールドを設定します。
seo-description: 1つ以上の画像アセットに対して、画像固有のフィールドを設定します。
seo-title: batchSetImageFields
solution: Experience Manager
title: batchSetImageFields
topic: Dynamic Media Image Production System API
uuid: e0ad7da4-cb28-4402-8b47-a600916d23b3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 9%

---


# batchSetImageFields{#batchsetimagefields}

1つ以上の画像アセットに対して、画像固有のフィールドを設定します。

構文

## 認証済みユーザータイプ{#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-4969815cf67c4d11b13bb2017b3604e8}

**入力(batchSetImageFields)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 画像アセットを含む会社へのハンドル。 |
| `*`updateArray`*` | `types:ImageFieldUpdateArray` | はい | 画像フィールドの配列が更新されます。 |

**出力(batchSetImageFields)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | はい | 正常に設定された画像フィールドの数。 |
| `*`warningCount`*` | `xsd:int` | はい | 操作が画像フィールドの設定を試行したときに生成された警告の数です。 |
| `*`errorCount`*` | `xsd:int` | はい | 操作が画像フィールドの設定を試行したときに生成されたエラーの数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときに警告を生成したアセットに関連付けられた詳細の配列です。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときにエラーが発生したアセットに関連付けられた詳細の配列です。 |

## 例 {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

次の使用例は、更新配列内の2つのイメージのフィールドにデータを設定します。 この配列では、画像はアセットハンドルによって指定され、ピクセル単位の解像度、x位置とy位置のアンカー座標、およびユーザデータを含みます。 この応答は、両方の画像のフィールドが正常に設定されたことを示します。

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

