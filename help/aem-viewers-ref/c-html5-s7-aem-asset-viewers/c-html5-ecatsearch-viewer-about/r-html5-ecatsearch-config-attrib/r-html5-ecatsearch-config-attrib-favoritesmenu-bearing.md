---
description: ボタンコンテナのスライドアニメーションの方向を指定します。
seo-description: ボタンコンテナのスライドアニメーションの方向を指定します。
seo-title: FavoritesMenu.bearing
solution: Experience Manager
title: FavoritesMenu.bearing
topic: Dynamic media
uuid: c3f415ad-f976-464a-9067-a5d526908352
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# FavoritesMenu.bearing{#favoritesmenu-bearing}

ボタンコンテナのスライドアニメーションの方向を指定します。

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> をに設定すると、 <span class="codeph"></span><span class="codeph"> 、</span><span class="codeph"> 、</span>left <span class="codeph"> 、</span>right up、またはright upのいずれかに設定した場合、追加の境界チェックを行わずに、指定した方向にパネルがロールアウトされ、外部コンテナによってパネルが切り取られます。 </p> <p>fit-verticalに設定すると <span class="codeph"></span>、コンポーネントはまずパネルの基本の位置をお気に入りメニューの下部に移動し、その基本の場所から次のいずれかの方向にパネルをロールアウトしようとします。下、右、左 試行のたびに、外側のコンテナでパネルが切り取られているかどうかがチェックされます。 すべての試行が失敗した場合、パネルの基本の位置を上に移動し、上、右、左の方向からロールアウト試行を繰り返します。 </p> <p>fit-lateralを設定すると <span class="codeph"></span>、コンポーネントでも同様のロジックが使用されます。 ベースが最初に右に移動し、右、下、上のロールアウト方向を試します。 次に、ベースを左に移動し、左、下、上のロールアウト方向を試します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
