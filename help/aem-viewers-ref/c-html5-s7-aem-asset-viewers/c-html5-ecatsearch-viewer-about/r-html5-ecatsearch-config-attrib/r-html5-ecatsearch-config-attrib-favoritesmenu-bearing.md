---
description: ボタンコンテナのスライドアニメーションの方向を指定します。
solution: Experience Manager
title: FavoritesMenu.bearing
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,User
exl-id: 2466a288-59c2-4a5e-b0bd-ff5b42dcacdb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

ボタンコンテナのスライドアニメーションの方向を指定します。

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>、<span class="codeph"> right</span>に設定すると、追加の境界チェックなしで、パネルが指定の方向にロールアウトし、外側のコンテナによってパネルが切り取られます。 </p> <p><span class="codeph"> fit-vertical</span>に設定すると、コンポーネントは、まずパネルの基本位置をお気に入りメニューの下部に移動し、その基本位置から次のいずれかの方向にパネルをロールアウトしようとします。下、右、左 試行のたびに、外側のコンテナによってパネルが切り取られているかどうかがチェックされます。 すべての試行が失敗した場合、コンポーネントは基本パネルの位置を上に移動し、上、右、左の方向からロールアウト試行を繰り返します。 </p> <p><span class="codeph"> fit-lateral</span>に設定した場合、コンポーネントは同様のロジックを使用します。 ベースは、まず右、下、上のロールアウト方向に移動します。 次に、ベースを左に移動し、左、下、上のロールアウト方向を試します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
