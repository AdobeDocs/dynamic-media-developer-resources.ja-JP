---
description: バッチモードを使用してアセットのメタデータを設定します。
seo-description: バッチモードを使用してアセットのメタデータを設定します。
seo-title: batchSetAssetMetadata
solution: Experience Manager
title: batchSetAssetMetadata
topic: Scene7 Image Production System API
uuid: 88d8f279-988f-4956-b66f-60fa95cf511c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchSetAssetMetadata{#batchsetassetmetadata}

バッチモードを使用してアセットのメタデータを設定します。

構文

## 認証されたユーザータイプ {#section-5310d9fd00604cbf9756944900378855}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-7111ac93bc7747f69ba14db4ac3912b0}

**入力(batchSetAssetMetadataParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | バッチ操作で設定するメタデータを持つ会社のハンドル。 |
| ` *`updateArray`*` | `types:BatchMetadataUpdateArray` | はい | アセットに適用されたメタデータ更新の配列。 |

**出力(batchSetAssetMetadataParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | はい | 正常に設定されたメタデータの数。 |
| ` *`warningCount`*` | `xsd:int` | はい | 操作がメタデータを設定しようとしたときに生成された警告の数です。 |
| ` *`errorCount`*` | `xsd:int` | はい | 操作がメタデータを設定しようとしたときに生成されたエラーの数です。 |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作がアセットのメタデータをバッチ設定しようとした場合に警告を生成するアセットに関連付けられた詳細の配列です。 |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作がアセットのメタデータをバッチ設定しようとしたときにエラーを生成するアセットに関連付けられた詳細の配列です。 |

## 例 {#section-2de798ac920e4b47b971b1729a64395b}

**リクエスト**

```java
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

```java
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```

