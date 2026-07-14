---
description: 複数のアセットを互いに独立して移動します。 これは、assetMoveArrayに含まれるAssetMove タイプを使用して実現します。 各AssetMove フィールドには、宛先フォルダーが含まれます。
solution: Experience Manager
title: moveAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e5bb2188-d262-4324-9f71-68634b6af654
TQID: 'https://experienceleague.adobe.com/zrKcnSbPFbQhujXvLkBkao6tYgGHcIZ-Yl2CUkj-usc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 202
ht-degree: 8%

---

# moveAssets{#moveassets}

複数のアセットを互いに独立して移動します。 これは、assetMoveArrayに含まれるAssetMove タイプを使用して実現します。 各AssetMove フィールドには、宛先フォルダーが含まれます。

構文

## 承認済みユーザータイプ {#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-7d47f663474b41cc83439288ac133cc5}

**入力（moveAssetsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 移動するアセットを持つ会社へのハンドル。 |
| assetMoveArray | `types:AssetMoveArray` | はい | アセット移動配列。 アセットとアセットの宛先フォルダーが含まれます。 |

**出力（moveAssetsReturn）**

<table id="table_FD902FAB4F98413C8A051270ADD7D9C7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 必須 </th> 
   <th colname="col4" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> アセット数を正常に移動しました。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">個のwarningCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 操作が移動しようとしたときに警告を生成したアセットの数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 操作が移動しようとしたときにエラーを生成したアセットの数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">種類：AssetOperationFaultArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <span class="codeph">個のAssetOperationFaults</span>のうち、次のものが含まれています： 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">警告を投げかけたAssets。 </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">警告コード。 </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">警告の理由。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">種類：AssetOperationFaultArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <span class="codeph">個のAssetOperationFaults</span>のうち、次のものが含まれています： 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">Assetsはミスを投げつけた。 </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">エラーコード： </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">エラーの理由。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

このコード サンプルは、`assetMoveArray`で指定された特定の場所にアセットを移動します。 配列には、アセットハンドルとそのフォルダーハンドルが含まれます。 応答は、アセットが正常に移動されたことを示します。

**リクエスト**

```java
<moveAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetMoveArray>
      <items>
          <assetHandle>a|942|1|579</assetHandle>
          <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
      <items>
         <assetHandle>a|943|1|580</assetHandle>
         <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
   </assetMoveArray>
</moveAssetsParam>
```

**応答**

```java
<moveAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</moveAssetsReturn>
```

