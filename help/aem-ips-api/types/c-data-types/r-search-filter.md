---
description: 検索をより効率的に行うための検索条件の定義に役立つフィルター。
seo-description: 検索をより効率的に行うための検索条件の定義に役立つフィルター。
seo-title: SearchFilter
solution: Experience Manager
title: SearchFilter
topic: Dynamic Media Image Production System API
uuid: 85a434d3-51a5-4e68-901e-70585c0e8b20
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---


# SearchFilter{#searchfilter}

検索をより効率的に行うための検索条件の定義に役立つフィルター。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> folder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 検索するフォルダを指定します。 会社全体を検索する場合は、空白のままにします。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">次に設定： 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> True</span>:指定したフォルダーとすべてのサブフォルダーを検索するには </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> False</span>:名前付きのフォルダーのみを検索する場合。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">検索で返すアセットタイプのリスト。 例えば、<span class="codeph"> image</span>のように指定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3"> 検索から除外するアセットタイプを指定します。 例えば、image. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">検索で返すアセットのサブタイプのリスト。 例えば、<span class="codeph"> AssetSet</span>の場合、<span class="codeph"> MediaType</span>サブタイプを検索できます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> strictSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><span class="codeph"> assetSubTypeArray</span>が渡される場合に、サブタイプのないアセットを返すかどうかを指定する、オプションのブール型のフラグ。 </p> <p>trueの場合は、指定したサブタイプの1つを持つアセットのみが返されます。 </p> <p>falseの場合、サブタイプのないアセットも返されます。 </p> <p>初期設定はfalseです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">次に設定： 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> True</span>:元のアセットのみを返す場合。 </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> False</span>:生成されたコンテンツを返す。例えば、アップロードされたPDFからの画像。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 検索するプロジェクトへのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">指定する: 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E"><span class="codeph"> MarkedForPublish</span> を使用して、公開済みアセットのみを返します。 </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672"><span class="codeph"> NotMarkedForPublish</span> を呼び出すと、非公開アセットのみが返されます。 </li> 
    </ul> <p>注意：<i>すべての</i>公開状態タイプを検索するには、空白のままにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">指定する: 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> Any</span> を指定すると、ごみ箱の状態に関係なくアセットが返されます。 </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> NotInTrashを使用して、'normal'アセットを返</span> します。 </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6"><span class="codeph"> InTrashを使用して、ごみ箱からアセットを返</span> します。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

