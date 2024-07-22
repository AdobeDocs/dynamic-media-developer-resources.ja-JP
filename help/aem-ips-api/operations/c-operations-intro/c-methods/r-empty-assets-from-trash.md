---
title: emptyAssetsFromTrash
description: IPS ごみ箱からアセットを空にします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 6%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

IPS ごみ箱からアセットを空にします。

Assetsは、手動で空になるまで、またはゴミ箱から出るまで、ゴミ箱に入っています。 手動で空にした場合、システムから最終的にパージされるまで、次のクリーンアップジョブ（通常は夜間）までゴミ箱に残ります。 ごみ箱からタイムアウトすると、アセットは、その同じクリーンアップアクティビティの一環としてクリーンアップされます。 タイムアウトは設定可能です（デフォルトは 7 日）。

## 許可されているユーザータイプ {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-8e1fb0ee3aae453581e99ef76e298569}

**入力（emptyAssetsFromTrashParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | xsd:string | はい | アセットを所有する会社へのハンドル。 |
| assetHandleArray | 型：HandleArray | はい | ごみ箱から空にする項目を表すハンドルの配列。 |

**出力（emptyAssetsFromTrashParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | xsd:Int | はい | アセット数がごみ箱から正常に空になりました。 |
| warningCount | xsd:Int | はい | 操作がごみ箱からアセットを空にしようとしたときに生成された警告の数。 |
| errorCount | xsd:Int | はい | 操作がごみ箱からアセットを空にしようとしたときに生成されたエラーの数。 |
| warningDetailArray | タイプ：AssetOperationFaultArray | いいえ | 操作がごみ箱からアセットを空にしようとした際に警告を生成した、アセットに関連付けられている詳細の配列。 |
| errorDetailArray | タイプ：AssetOperationFaultArray | いいえ | 操作がごみ箱から空にしようとした際にエラーが発生したアセットに関連付けられている詳細の配列。 |

## 例 {#section-6154a873b6c342bf92e2036280cafdcf}

このコードサンプルでは、会社のハンドルと、ごみ箱から空にするアセットへのハンドルを含むアセットハンドル配列を使用しています。

**リクエスト**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**応答**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
