---
description: バッチモードを使用してアセットのメタデータを設定します。
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 11%

---

# batchSetAssetMetadata{#batchsetassetmetadata}

バッチモードを使用してアセットのメタデータを設定します。

構文

## 許可されているユーザータイプ {#section-5310d9fd00604cbf9756944900378855}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-7111ac93bc7747f69ba14db4ac3912b0}

**入力（batchSetAssetMetadataParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | バッチ操作でメタデータを設定する会社へのハンドル。 |
| updateArray | `types:BatchMetadataUpdateArray` | はい | アセットに適用されたメタデータ更新の配列。 |

**出力（batchSetAssetMetadataParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | 正常に設定されたメタデータの数。 |
| warningCount | `xsd:int` | はい | 操作がメタデータを設定しようとしたときに生成された警告の数です。 |
| errorCount | `xsd:int` | はい | 操作がメタデータを設定しようとしたときに生成されたエラーの数です。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作がアセットのメタデータをバッチセットしようとすると警告を生成する、アセットに関連付けられた詳細の配列。 |
| errorDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作がアセットのメタデータをバッチセットしようとするとエラーが発生するアセットに関連付けられた詳細の配列。 |

## 例 {#section-2de798ac920e4b47b971b1729a64395b}

**リクエスト**

```java {.line-numbers}
<batchSetAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
<companyHandle>c|6</companyHandle>
<updateArray>
   <items>
      <assetHandleArray>
         <items>a|743|1|538</items>
         <items>a|744|1|539</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>400</value>
         </items>
      </updateArray>
   </items>
   <items>
      <assetHandleArray>
         <items>a|732|1|535</items>
         <items>a|739|1|537</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>300</value>
         </items>
      </updateArray>
   </items>
</updateArray>
</batchSetAssetMetadataParam>
```

**応答**

```java {.line-numbers}
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```
