---
description: プロジェクト内のアセットの割り当てまたは更新。
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6e6e9bd-5ee2-4750-9182-49e7a3e3486c
TQID: 'https://experienceleague.adobe.com/J5X6PS7L7YCH6J9ClzAUo24O44fMWxNqPnILckRBbUI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 16%

---

# setProjectAssets{#setprojectassets}

プロジェクト内のアセットの割り当てまたは更新。

構文

## 承認済みユーザータイプ {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**入力（setProjectAssetsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyName | `xsd:string` | はい | 会社のハンドル。 |
| projectHandle | `xsd:string` | はい | プロジェクトハンドル： |
| assetHandleArray | `types:HandleArray` | はい | プロジェクトに関連付けるアセットハンドルの配列。 |

**出力（setProjectAssetsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | 正常に追加されたアセットの数。 |

## 例 {#section-33c1a909c3dc4aa98da474c23a036596}

このコードサンプルでは、プロジェクトにアセットを割り当てます。 リクエストは、1の成功回数を返します。

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
