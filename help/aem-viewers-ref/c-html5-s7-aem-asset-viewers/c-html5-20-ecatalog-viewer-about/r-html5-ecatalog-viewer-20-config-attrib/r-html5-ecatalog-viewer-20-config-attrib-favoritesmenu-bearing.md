---
title: FavoritesMenu.bearing
description: ボタンコンテナのスライドアニメーションの方向を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 1%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

ボタンコンテナのスライドアニメーションの方向を指定します。

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 上|下|左|右|フィット – 垂直|フィット – 横 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span> または <span class="codeph"> right</span> に設定すると、パネルは余分な境界チェックなしで指定した方向にロールアウトされ、外部コンテナによってパネルがクリップされます。 </p> <p><span class="codeph"> fit-vertical</span> に設定した場合、コンポーネントはまず、ベースパネルの位置を「お気に入り」メニューの一番下に移動します。 このようなベースの場所から、下、右、左のいずれかの方向にパネルを展開しようとします。 試行のたびに、コンポーネントはパネルが外部コンテナによってクリップされているかどうかを確認します。 すべての試行が失敗した場合、コンポーネントは基本パネルの位置を上に移動し、ロールアウトの試行を上、右、左から繰り返そうとします。 </p> <p>fit-lateral<span class="codeph"> に設定 </span> ると、コンポーネントは同様のロジックを使用します。 ベースは最初に右に移動し、右、下、上のロールアウト方向を試します。 次に、ベースを左に移動し、左、下、上のロールアウト方向を試します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
