---
title: TableOfContents.bearing
description: TableOfContents.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b140c9ba-353d-49ef-9e6b-f5bc45e0dbfd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> ドロップダウンパネルの外観の方向をコントロールします。 </p> <p>に設定する場合 <span class="codeph"> fit-vertical</span>を選択した場合、コンポーネントはまず、パネルの基本位置をボタンの下部に移動し、基本位置から右または左にパネルをロールアウトしようとします。 試行のたびに、外側のコンテナによってパネルが切り取られているかどうかを確認します。 すべての試行が失敗した場合、コンポーネントは基本パネルの位置を上に移動しようとし、右と左の方向にロールアウトの試行を繰り返します。 </p> <p>に設定する場合 <span class="codeph"> フィットラテラル</span>の場合は、同様のロジックが使用されますが、まずベースを右に移動し、下向きや上向きのロールアウト方向を試します。 次に、ベースを左に移動し、下方向と上方向のロールアウトを試みます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> ユーザーがアイドル状態のときにパネルを非表示にするドロップダウン自動非表示タイマーの遅延を秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-55436ddd78b04f538dbb9a7a8463feae}

（オプション）

## 初期設定 {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## 例 {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
