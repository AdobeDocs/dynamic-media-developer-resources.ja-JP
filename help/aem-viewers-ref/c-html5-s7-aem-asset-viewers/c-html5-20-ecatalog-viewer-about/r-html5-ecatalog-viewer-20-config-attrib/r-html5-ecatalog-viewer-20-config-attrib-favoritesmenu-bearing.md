---
description: ボタンコンテナのスライドアニメーションの方向を指定します。
seo-description: ボタンコンテナのスライドアニメーションの方向を指定します。
seo-title: FavoritesMenu.bearing
solution: Experience Manager
title: FavoritesMenu.bearing
topic: Dynamic media
uuid: badc02ef-2724-41bb-9b00-c65966be8577
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 2%

---


# FavoritesMenu.bearing{#favoritesmenu-bearing}

ボタンコンテナのスライドアニメーションの方向を指定します。

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>、<span class="codeph"> right</span>に設定すると、追加の境界チェックなしで、指定したコンテナにパネルがロールアウトし、外部でパネルが切り取られます。 </p> <p><span class="codeph"> fit-vertical</span>に設定した場合、コンポーネントは、まずパネルの基本の位置をお気に入りメニューの下部に移動し、その基本の場所から次のいずれかの方向にパネルをロールアウトしようとします。bottom, right, left。 試行のたびに、外側のコンテナでパネルが切り取られているかどうかをチェックします。 すべての試行が失敗すると、パネルの基本の位置を上に移動し、上、右、左の方向からロールアウト試行を繰り返します。 </p> <p><span class="codeph"> fit-lateral</span>に設定した場合も、コンポーネントでは同じロジックが使用されます。 ベースが最初に右に移動し、右、下、上方向のロールアウトを試します。 次に、基本の位置を左に移動し、左、下、上方向のロールアウトを試します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
