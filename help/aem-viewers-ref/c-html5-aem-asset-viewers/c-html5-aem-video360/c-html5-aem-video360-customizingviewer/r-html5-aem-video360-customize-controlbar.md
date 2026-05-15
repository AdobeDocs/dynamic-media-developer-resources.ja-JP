---
title: コントロールバー
description: コントロールバーは、再生/一時停止ボタンやボリュームコントロールなど、ビデオビューアで使用できるすべてのユーザーインターフェイスコントロールを含む長方形の領域です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 06078310-8aeb-449f-919a-ce88ddc8c4b3
TQID: 'https://experienceleague.adobe.com/xWTbcn5GR0BexFz9tX8hy0aElmGPEcAsUhWJ-VSLqI0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 0%

---

# コントロールバー{#control-bar}

コントロールバーは、再生/一時停止ボタンやボリュームコントロールなど、ビデオビューアで使用できるすべてのユーザーインターフェイスコントロールを含む長方形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

コントロールバーは、常に使用可能なビューア全体の幅を使用します。 ビデオビューアコンテナに対して、CSSで色、高さ、垂直位置を変更できます。

次のCSS クラスセレクターは、コントロールバーの外観を制御します。

```
.s7video360viewer .s7controlbar
```

## コントロールバーのCSS プロパティ {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p>パディングを含む上部境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下</span> </p> </td> 
   <td colname="col2"> <p> パディングを含む下部境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>コントロールバーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>コントロールバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 高さ30 ピクセルのグレーのコントロール バーをビデオ ビューア コンテナの上部に配置して、ビデオ ビューアを設定します。

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
