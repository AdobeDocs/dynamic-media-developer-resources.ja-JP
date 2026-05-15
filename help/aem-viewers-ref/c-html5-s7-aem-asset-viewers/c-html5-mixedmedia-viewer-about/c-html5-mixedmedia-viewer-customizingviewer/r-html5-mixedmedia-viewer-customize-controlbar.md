---
title: コントロールバー
description: コントロールバーは、再生/一時停止ボタンやボリュームコントロールなど、ビデオビューアで使用できるすべてのユーザーインターフェイスコントロールを含む長方形の領域です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
TQID: 'https://experienceleague.adobe.com/IfJ-ukIT31IS8sE6EWSqTl7k4uav08CsDHvS4bSh-Bc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 0%

---

# コントロールバー{#control-bar}

コントロールバーは、再生/一時停止ボタンやボリュームコントロールなど、ビデオビューアで使用できるすべてのユーザーインターフェイスコントロールを含む長方形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

コントロールバーは、常に使用可能なビューア全体の幅を使用します。 ビデオビューアコンテナに対して、CSSで色、高さ、垂直位置を変更できます。

次のCSS クラスセレクターは、コントロールバーの外観を制御します。

```
.s7mixedmediaviewer .s7controlbar
```

## コントロールバーのCSS プロパティ {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
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

30 ピクセルの高さのグレーのコントロールバーを使用して、混在メディアビューアを設定する。

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
