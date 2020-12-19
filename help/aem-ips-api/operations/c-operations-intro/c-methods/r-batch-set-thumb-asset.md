---
description: 1つ以上のアセットのサムネール画像を設定します。
seo-description: 1つ以上のアセットのサムネール画像を設定します。
seo-title: batchSetThumbAsset
solution: Experience Manager
title: batchSetThumbAsset
topic: Scene7 Image Production System API
uuid: 16c298a7-bb07-4643-824b-8f864d7f0290
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 13%

---


# batchSetThumbAsset{#batchsetthumbasset}

1つ以上のアセットのサムネール画像を設定します。

構文

## サムネールアセットタイプ{#section-4edc2a6a8f824213b0aaddb1d437268c}

使用できるサムネールアセットタイプは、次のとおりです。

* 画像
* 調整済みのビュー
* マスク
* テンプレート
* PsdTemplate

## 認証済みユーザータイプ{#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、ターゲットアセットに対する読み取り/書き込みアクセス権と、サムアセットに対する読み取りアクセス権を持つ必要があります。

## パラメータ {#section-9c6efa000b384b3db6c013def20cf40b}

**入力(batchSetThumbAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | アセットを含む会社へのハンドル。 |
| ` *`updateArray`*` | `types:ThumbAssetUpdateArray` | はい | 更新の配列です。 |

**出力(batchSetThumbAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | はい | 正常に設定されたサムネールの数です。 |
| ` *`warningCount`*` | `xsd:int` | はい | 操作がサムネールの設定を試行したときに生成された警告の数です。 |
| ` *`errorCount`*` | `xsd:int` | はい | 操作がサムネールの設定を試行したときに生成されたエラーの数です。 |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときに警告を生成したアセットに関連付けられた詳細の配列です。 |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が更新を適用しようとしたときにエラーが発生したアセットに関連付けられた詳細の配列です。 |

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

