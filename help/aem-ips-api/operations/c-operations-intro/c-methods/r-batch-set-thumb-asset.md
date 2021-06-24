---
description: 1つ以上のアセットのサムネール画像を設定します。
solution: Experience Manager
title: batchSetThumbAsset
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Administrator
exl-id: f7d7ddd9-a3c3-47c4-8da6-d693851d0d7f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 13%

---

# batchSetThumbAsset{#batchsetthumbasset}

1つ以上のアセットのサムネール画像を設定します。

構文

## サムネールのアセットタイプ {#section-4edc2a6a8f824213b0aaddb1d437268c}

使用できるサムネールアセットタイプは次のとおりです。

* 画像
* 調整済みのビュー
* マスク
* テンプレート
* PsdTemplate

## 許可されたユーザーの種類 {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、ターゲットアセットに対する読み取り/書き込みアクセス権とサムアセットに対する読み取りアクセス権を持っている必要があります。

## パラメータ {#section-9c6efa000b384b3db6c013def20cf40b}

**入力(batchSetThumbAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | アセットを含む会社へのハンドル。 |
| `*`updateArray`*` | `types:ThumbAssetUpdateArray` | はい | 更新の配列。 |

**出力(batchSetThumbAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | はい | 正常に設定されたサムネールの数。 |
| `*`warningCount`*` | `xsd:int` | はい | 操作がサムネールの設定を試みたときに生成される警告の数です。 |
| `*`errorCount`*` | `xsd:int` | はい | 操作がサムネールの設定を試みたときに生成されたエラーの数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときに警告が生成されたアセットに関連付けられた詳細の配列。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときにエラーが発生したアセットに関連付けられた詳細の配列。 |

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
