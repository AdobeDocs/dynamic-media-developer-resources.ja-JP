---
description: 複数のアセットを互いに独立して移動します。 これは、assetMoveArrayに含まれるAssetMove型を使用して実行されます。 各AssetMoveフィールドには、保存先フォルダが含まれています。
seo-description: 複数のアセットを互いに独立して移動します。 これは、assetMoveArrayに含まれるAssetMove型を使用して実行されます。 各AssetMoveフィールドには、保存先フォルダが含まれています。
seo-title: moveAssets
solution: Experience Manager
title: moveAssets
topic: Dynamic Media Image Production System API
uuid: 178f9979-fff5-45ce-a001-1263d1770ea8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 8%

---


# moveAssets{#moveassets}

複数のアセットを互いに独立して移動します。 これは、assetMoveArrayに含まれるAssetMove型を使用して実行されます。 各AssetMoveフィールドには、保存先フォルダが含まれています。

構文

## 認証済みユーザータイプ{#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-7d47f663474b41cc83439288ac133cc5}

**入力(moveAssetsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | アセットを移動する会社へのハンドル。 |
| `*`assetMoveArray`*` | `types:AssetMoveArray` | はい | アセット移動配列。 アセットとアセットの保存先フォルダが含まれます。 |

**出力(moveAssetsReturn)**

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
   <td colname="col4"> アセット数が正常に移動されました。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 操作が警告を移動しようとしたときに生成したアセットの数です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 操作がアセットの移動を試みたときにエラーが発生したアセットの数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AssetOperationFaultArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <span class="codeph"> 次を含む</span>AssetOperationFaults: 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">警告をスローしたアセット。 </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">警告コード。 </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">警告の理由です。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AssetOperationFaultArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <span class="codeph"> 次を含む</span>AssetOperationFaults: 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">エラーをスローしたアセット。 </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">エラーコード。 </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">エラーの理由。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

このコードサンプルを使用すると、`assetMoveArray`で指定された特定の場所にアセットを移動できます。 この配列は、アセットハンドルとそのフォルダハンドルを含む。 この応答は、アセットが正常に移動されたことを示します。

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

