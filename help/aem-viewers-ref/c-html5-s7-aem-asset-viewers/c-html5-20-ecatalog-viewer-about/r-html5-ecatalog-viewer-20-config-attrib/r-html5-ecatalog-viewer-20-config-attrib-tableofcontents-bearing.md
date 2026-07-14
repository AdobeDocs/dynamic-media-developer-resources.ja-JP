---
title: TableOfContents.bearing
description: TableOfContents.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b140c9ba-353d-49ef-9e6b-f5bc45e0dbfd
TQID: 'https://experienceleague.adobe.com/i8oPW8fpqvU8JaUaJ-95swaFjD6YTHcqv21s3i7-L2g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 1%

---

# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> ドロップダウンパネルのアピアランスの方向を制御します。 </p> <p><span class="codeph"> fit-vertical</span>に設定すると、コンポーネントは最初にベースパネルの位置をボタンの下部に移動し、ベースパネルの位置から左右にロールアウトしようとします。 コンポーネントは、試行のたびに、パネルが外部コンテナによってクリップされているかどうかを確認します。 すべての試行が失敗した場合、コンポーネントはベースパネルの位置を上に移動し、ロールアウトの試行を左右に繰り返します。 </p> <p><span class="codeph"> fit-lateral</span>に設定すると、コンポーネントは同様のロジックを使用しますが、ロールアウト方向の下方向と上方向を試して、最初にベースを右にシフトします。 次に、ロールアウト方向を上下させながら、ベースを左に移動します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> ユーザーがアイドル状態のときにパネルを非表示にするドロップダウン自動非表示タイマーの遅延時間を秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-55436ddd78b04f538dbb9a7a8463feae}

オプション。

## 初期設定 {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## 例 {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`

