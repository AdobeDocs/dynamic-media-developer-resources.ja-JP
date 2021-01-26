---
description: プロジェクト内のアセットの割り当てまたは更新を行います。
seo-description: プロジェクト内のアセットの割り当てまたは更新を行います。
seo-title: setProjectAssets
solution: Experience Manager
title: setProjectAssets
topic: Dynamic Media Image Production System API
uuid: 98d18948-d387-4890-9c27-e8ab60cded1d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 18%

---


# setProjectAssets{#setprojectassets}

プロジェクト内のアセットの割り当てまたは更新を行います。

構文

## 認証済みユーザータイプ{#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**入力(setProjectAssetsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | はい | 会社ハンドル |
| `*`projectHandle`*` | `xsd:string` | はい | プロジェクトハンドル |
| `*`assetHandleArray`*` | `types:HandleArray` | はい | プロジェクトに関連付けるアセットハンドルの配列。 |

**出力(setProjectAssetsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | はい | 正常に追加されたアセットの数。 |

## 例 {#section-33c1a909c3dc4aa98da474c23a036596}

このコードのサンプルを使用すると、プロジェクトにアセットを割り当てることができます。 リクエストは、1の成功数を返します。

**リクエスト**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**応答**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```

