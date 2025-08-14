---
title: SearchFilter
description: 検索条件を定義して検索の効率を高めるのに役立つフィルター。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b3a26966-33c9-48ca-b0ed-d05fc0e2050f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 2%

---

# [!DNL SearchFilter]{#searchfilter}

検索条件を定義して検索の効率を高めるのに役立つフィルター。

構文

## パラメーター {#section-4c611d9bbe0d418d882632605fc4d29d}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> フォルダー </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 検索するフォルダーを指定します。 会社全体を検索する場合は、空白のままにします。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">に設定： 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> True</span>：指定したフォルダーとすべてのサブフォルダーを検索します。 </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> False</span>：指定したフォルダーのみを検索します。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">検索で返すアセットタイプのリスト。 例えば、<span class="codeph"> の画像 </span> です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3"> 検索から除外するアセットタイプを指定します。 例えば、画像です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">検索で返すアセットサブタイプのリスト。 例えば、<span class="codeph"> AssetSet</span> の場合、<span class="codeph"> MediaType</span> サブタイプを検索できます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> strictSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>assetSubTypeArray<span class="codeph"> が渡された場合に、サブタイプを含まないアセットを返すかどうか </span> 指定するオプションのブール値フラグ。 </p> <p>true の場合、指定されたサブタイプのいずれかが含まれるアセットのみが返されます。 </p> <p>false の場合、サブタイプのないアセットも返されます。 </p> <p>初期設定は false。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">に設定： 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> True</span>：元のアセットのみを返します。 </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> False</span>：生成されたコンテンツを返します。 例えば、アップロードされたPDFの画像などです。 </li> 
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
   <td colname="col3">以下を指定します。 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E">MarkedForPublish<span class="codeph"> を </span> リックして、公開されたアセットのみを返します。 </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672">NotMarkedForPublish<span class="codeph"> を </span> リックして、未公開のアセットのみを返します。 </li> 
    </ul> <p>メモ：公開済みの状態タイプを <i> すべて </i> 検索するには、空白のままにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">以下を指定します。 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> すべて </span> ごみ箱の状態に関係なく、アセットを返します。 </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph">NotInTrash</span>」をクリックして、「通常」のアセットを返します。 </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6">ごみ箱 <span class="codeph"> を </span> リックして、ごみ箱からアセットを返します。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
