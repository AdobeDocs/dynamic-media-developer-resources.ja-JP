---
title: コントロールバー
description: コントロールバーは、スマート切り抜きビデオビューアで使用できるすべてのUI コントロール（再生/一時停止ボタンやボリュームコントロールなど）の背後にある長方形の領域です。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 8ea06e0a-705d-436a-9393-75a36381cba6
TQID: 'https://experienceleague.adobe.com/OYPgQ9LBIb-uYwT0WRexIchENJ-0PoH6lWOkkWilIiU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 178
ht-degree: 0%

---

# コントロールバー{#control-bar}

コントロールバーは、スマート切り抜きビデオビューアで使用できるすべてのUI コントロール（再生/一時停止ボタンやボリュームコントロールなど）の背後にある長方形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

コントロールバーは、常に使用可能なビューア全体の幅を使用します。 スマート切り抜きビデオビューアコンテナに対して、CSSで色、高さ、垂直位置を変更できます。

次のCSS クラスセレクターは、コントロールバーの外観を制御します。

```
.s7smartcropvideoviewer .s7controlbar
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

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

高さ30 ピクセルのグレーのコントロールバーを備えたスマート切り抜きビデオビューアを設定するには、スマート切り抜きビデオビューアコンテナの上部に配置します。

```
.s7smartcropvideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
