---
title: コントロールバー
description: コントロールバーは、再生/一時停止ボタンやボリュームコントロールなど、ビデオビューアで使用できるすべてのユーザインターフェイスコントロールを含み、その背後に配置する長方形の領域です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 06078310-8aeb-449f-919a-ce88ddc8c4b3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# コントロールバー{#control-bar}

コントロールバーは、再生/一時停止ボタンやボリュームコントロールなど、ビデオビューアで使用できるすべてのユーザインターフェイスコントロールを含み、その背後に配置する長方形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

コントロールバーは、常に、使用可能なビューアの幅全体を取ります。 CSS で、ビデオビューアのコンテナに対するカラー、高さ、垂直方向の位置を変更できます。

以下に示す CSS クラスセレクターで、コントロールバーの外観を制御します。

```
.s7video360viewer .s7controlbar
```

## コントロールバーの CSS プロパティ {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む上の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p> パディングを含む下の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — 高さが 30 ピクセルで、ビデオビューアのコンテナの上部に配置するグレーのコントロールバーを持つビデオビューアを設定するには、次のように記述します。

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
