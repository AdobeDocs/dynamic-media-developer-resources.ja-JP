---
title: フォーカスハイライト
description: フォーカスされたビューアユーザーインターフェイス要素の周囲に表示される入力フォーカスのハイライトは、CSS クラスセレクターで制御されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 05ac1a70-c20d-4ddf-942c-181f101cb1d8
TQID: 'https://experienceleague.adobe.com/ek1dKx5wgrWFRzoCo1u82iM03gHWZJN4UqlQBVgnmv0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 1%

---

# フォーカスハイライト{#focus-highlight}

フォーカスされたビューアユーザーインターフェイス要素の周囲に表示される入力フォーカスのハイライトは、CSS クラスセレクターで制御されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS プロパティ**

アピアランスは、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer *:focus
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
   <td colname="col1"> <p> <span class="codeph">概要</span> </p> </td> 
   <td colname="col2"> <p>ハイライトのスタイルをフォーカスします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – すべてのビューアのユーザーインターフェイス要素のデフォルトのブラウザーフォーカスのハイライトを無効にするには、次のCSS セレクターをビューアのスタイルシートに追加します。

```
.s7video360viewer *:focus { 
 outline: none; 
}
```
