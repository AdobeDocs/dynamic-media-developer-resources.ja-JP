---
description: 1 つ以上のアセットのサムネール画像を設定します。
solution: Experience Manager
title: batchSetThumbAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f7d7ddd9-a3c3-47c4-8da6-d693851d0d7f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 11%

---

# batchSetThumbAsset{#batchsetthumbasset}

1 つ以上のアセットのサムネール画像を設定します。

構文

## サムネールのアセットタイプ {#section-4edc2a6a8f824213b0aaddb1d437268c}

許可されるサムネールのアセットタイプは、次の要素で構成されます。

* 画像
* AdjustedView
* マスク
* テンプレート
* PsdTemplate

## 許可されているユーザータイプ {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーには、ターゲットアセットへの読み取り/書き込みアクセス権と、サムアセットへの読み取りアクセス権が必要です。

## パラメーター {#section-9c6efa000b384b3db6c013def20cf40b}

**入力（batchSetThumbAssetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | アセットを含む会社へのハンドル。 |
| updateArray | `types:ThumbAssetUpdateArray` | はい | 更新の配列。 |

**出力（batchSetThumbAssetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | 正常に設定されたサムネールの数。 |
| warningCount | `xsd:int` | はい | 操作でサムネールを設定しようとしたときに生成された警告の数。 |
| errorCount | `xsd:int` | はい | 操作でサムネールを設定しようとしたときに生成されたエラーの数です。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとした際に警告を生成したアセットに関連付けられた詳細の配列。 |
| errorDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときにエラーが発生したアセットに関連付けられた詳細の配列です。 |

## 例 {#section-6de69a8680c24c1486c5f01488393381}

**リクエスト**

```java
<batchSetThumbAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|234</assetHandle>
         <thumbAssetHandle>a|189</thumbAssetHandle>
      </items>
   </updateArray>
```

**応答**

```java
<batchSetThumbAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetThumbAssetReturn>
```
