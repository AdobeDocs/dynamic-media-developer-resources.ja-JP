---
description: プロジェクト内のアセットを割り当てるか、更新します。
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: b6e6e9bd-5ee2-4750-9182-49e7a3e3486c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 18%

---

# setProjectAssets{#setprojectassets}

プロジェクト内のアセットを割り当てるか、更新します。

構文

## 許可されたユーザーの種類 {#section-8d87939db6d547b48ca6d71771bbefa8}

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
| `*`companyName`*` | `xsd:string` | はい | 会社の担当。 |
| `*`projectHandle`*` | `xsd:string` | はい | プロジェクトハンドル。 |
| `*`assetHandleArray`*` | `types:HandleArray` | はい | プロジェクトに関連付けるアセットハンドルの配列。 |

**出力(setProjectAssetsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | はい | 正常に追加されたアセットの数。 |

## 例 {#section-33c1a909c3dc4aa98da474c23a036596}

このコードサンプルを使用すると、アセットをプロジェクトに割り当てることができます。 リクエストは、成功数1を返します。

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
