---
title: メインビューア領域
description: メインビュー領域は、360 ビデオが視聴される領域です。 サイズが指定されていない場合は、使用可能なデバイス画面に収まるように設定されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 912cb4b3-6409-48ed-9b9c-968b63718a1b
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# メインビューア領域{#main-viewer-area}

メインビュー領域は、360 ビデオが視聴される領域です。 サイズが指定されていない場合は、使用可能なデバイス画面に収まるように設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

表示領域の外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7video360viewer
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ビューアの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ビューアの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 16 進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-ee18025b182a42dc98052de5f133ddfe}

白の背景 (`#FFFFFF`) のビューアを設定し、サイズを 512 x 288 ピクセルにします。

```
.s7video360viewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
