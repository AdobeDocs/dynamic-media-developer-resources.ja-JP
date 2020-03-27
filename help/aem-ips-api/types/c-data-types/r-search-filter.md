---
description: 検索をより効率的に行うための検索条件の定義に役立つフィルタ。
seo-description: 検索をより効率的に行うための検索条件の定義に役立つフィルタ。
seo-title: SearchFilter
solution: Experience Manager
title: SearchFilter
topic: Scene7 Image Production System API
uuid: 85a434d3-51a5-4e68-901e-70585c0e8b20
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SearchFilter{#searchfilter}

検索をより効率的に行うための検索条件の定義に役立つフィルタ。

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
   <td colname="col1"> <span class="codeph"> フォ <span class="varname"> ルダ</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 検索するフォルダを指定します。 全体および全体の会社を検索する場合は、空白のままにします。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">次に設定： 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> True</span>:名前の付いたフォルダーとすべてのサブフォルダーを検索する場合。 </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> False</span>:名前の付いたフォルダーのみを検索する場合。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">検索で返すアセットタイプのリスト。 例えば、 <span class="codeph"> image</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> excludeAssetTypeArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3"> 検索から除外するアセットタイプを指定します。 例えば、image. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">検索で返すアセットのサブタイプのリスト。 例えば、アセットセッ <span class="codeph"> トの場合</span>、MediaTypeサブタイプを検 <span class="codeph"> 索できます</span> 。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> strictSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>assetSubTypeArrayが渡されたときに、サブタイプのないアセットを返すかどうかを指定する <span class="codeph"> ブール型</span> （オプション）フラグ。 </p> <p>trueの場合、指定したサブタイプの1つを持つアセットのみが返されます。 </p> <p>falseの場合、サブタイプのないアセットも返されます。 </p> <p>デフォルトはfalseです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> excludeByproducts <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">次に設定： 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> True</span>:元のアセットのみを返す場合。 </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> False</span>:生成されたコンテンツを返す場合。 例えば、アップロードされたPDFの画像などです。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 検索するプロジェクトのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">指定する: 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E"><span class="codeph"> MarkedForPublish</span> （公開済みアセットのみを返す）。 </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672"><span class="codeph"> NotMarkedForPublish</span> （未公開アセットのみを返す）。 </li> 
    </ul> <p>注意：すべての発行済み状態タイプを検索する <i>には</i> 、空白のままにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> ごみ <span class="varname"> 箱状</span> 態 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">指定する: 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> ごみ箱の状態</span> に関係なくアセットを返す場合は「任意」。 </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> NotInTrashを使用して</span> 、「通常」のアセットを返します。 </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6"><span class="codeph"> ごみ箱から</span> 、アセットを返す場合。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

