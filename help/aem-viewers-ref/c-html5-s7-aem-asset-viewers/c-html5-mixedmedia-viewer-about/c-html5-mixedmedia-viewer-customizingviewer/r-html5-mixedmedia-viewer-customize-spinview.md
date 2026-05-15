---
title: スピンビュー
description: メインビューは、現在のアセットがスピンセットである場合のスピン画像で構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
TQID: 'https://experienceleague.adobe.com/i51Si1u-npMCR4Rum5-g3JRjShCBWXG54yam4BWpU84'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 1%

---

# スピンビュー{#spin-view}

メインビューは、現在のアセットがスピンセットである場合のスピン画像で構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

メイン ビューア領域の&#x200B;**CSS プロパティ**

表示領域の外観は、次のCSS クラスセレクターで制御されます。

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col2"> <p> スピンビューの16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – スピンビューを透明にします。

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
