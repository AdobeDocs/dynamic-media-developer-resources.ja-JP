---
title: インジケーターを設定
description: セットインジケーターは、タッチデバイスでビューアを使用する際に、スウォッチの上に表示される一連のドットです。 スクロール ボタンが使用できない場合は、ドットを使用してサムネールのページ内を移動できます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: b1e6734e-a341-45d7-b771-daeb0527cd00
TQID: 'https://experienceleague.adobe.com/y4QBgUjYMAh5-FlbA32Zgg0Peve1FcO-qhDxc0Ypv4M'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 263
ht-degree: 0%

---

# インジケーターを設定{#set-indicator}

セットインジケーターは、タッチデバイスでビューアを使用する際に、スウォッチの上に表示される一連のドットです。 スクロール ボタンが使用できない場合は、ドットを使用してサムネールのページ内を移動できます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

セット インジケーターの&#x200B;**CSS プロパティ**

Set インジケーターコンテナの外観は、次のCSS クラスセレクターで制御されます。

```
.s7zoomviewer .s7setindicator
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>セットインジケーターの16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 背景が白いセットインジケーターを作成するには：

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

個々のセットインジケーターのドットの表示は、CSS クラスセレクターで制御されます。

`.s7zoomviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>セットインジケーターのドットの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>セットインジケーターのドットの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p>左余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p>上余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右余白</span> </p> </td> 
   <td colname="col2"> <p>右マージン（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom </span> </p> </td> 
   <td colname="col2"> <p>下余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>境界線の半径（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Set indicator dotは`state`属性セレクターをサポートしており、異なるサムネール状態に異なるスキンを適用するために使用できます。 特に、`state="selected"`はサムネールの現在のページに対応し、`state="unselected"`はデフォルトのドット状態に対応します。

例 – 2 ピクセルの水平余白、5 ピクセルの上余白、1 ピクセルの下余白、12 ピクセルの半径、デフォルトのカラー、およびアクティブなカラーを使用して、15 x 15 ピクセル#D5D3D3設定するインジケータードット#939393作成します。

```
.s7zoomviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7zoomviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
