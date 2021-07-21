---
description: 検索条件を定義して検索をより効率的にするのに役立つフィルター。
solution: Experience Manager
title: SearchFilter
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: b3a26966-33c9-48ca-b0ed-d05fc0e2050f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# SearchFilter{#searchfilter}

検索条件を定義して検索をより効率的にするのに役立つフィルター。

構文

## パラメータ {#section-4c611d9bbe0d418d882632605fc4d29d}

<table id="table_57CEE262A33A4E898C6AFB30C93FD874"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> フォルダー</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 検索するフォルダーを指定します。 全体および会社全体を検索する場合は、空白のままにします。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">次に設定： 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> True</span>:指定したフォルダとすべてのサブフォルダを検索する。 </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> False</span>:指定したフォルダーのみを検索する場合。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">検索で返すアセットタイプのリストです。 例えば、<span class="codeph"> image</span>のようにします。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3"> 検索から除外するアセットタイプを指定します。 例えば、imageなど。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">検索で返すアセットサブタイプのリスト。 例えば、<span class="codeph"> AssetSet</span>の場合、<span class="codeph"> MediaType</span>サブタイプを検索できます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> strictSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><span class="codeph"> assetSubTypeArray</span>が渡された場合にサブタイプのないアセットを返すかどうかを指定する任意のブール型フラグです。 </p> <p>trueの場合、指定されたサブタイプの1つを持つアセットのみが返されます。 </p> <p>falseの場合、サブタイプのないアセットも返されます。 </p> <p>デフォルトはfalseです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">次に設定： 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> True</span>:元のアセットのみを返す場合。 </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> False</span>:生成されたコンテンツを返す。例えば、アップロードされたPDFからの画像などです。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 検索するプロジェクトに対して処理します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">指定する: 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E"><span class="codeph"> </span> MarkedForPublishtoは、公開済みのアセットのみを返します。 </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672"><span class="codeph"> </span> NotMarkedForPublishは、非公開のアセットのみを返します。 </li> 
    </ul> <p>注意：<i>すべての</i>公開済み状態タイプを検索する場合は、空白のままにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">指定する: 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> </span> ごみ箱の状態に関係なく、アセットを返す。 </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> </span> NotInTrashtoは「通常の」アセットを返します。 </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6"><span class="codeph"> </span> InTrashtoは、ごみ箱からアセットを返します。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
