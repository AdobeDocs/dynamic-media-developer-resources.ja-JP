---
title: FavoritesMenu.bearing
description: ボタンコンテナのスライドアニメーションの方向を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

ボタンコンテナのスライドアニメーションの方向を指定します。

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> に設定する場合 <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>または <span class="codeph"> 右</span>を指定した場合、パネルは特別な境界チェックなしで指定した方向にロールアウトされ、外側のコンテナによってパネルがクリップされます。 </p> <p>に設定する場合 <span class="codeph"> fit-vertical</span>の場合、コンポーネントは、まず、基本パネルの位置をお気に入りメニューの下部に移動します。 このような基本位置から、次のいずれかの方向にパネルをロールアウトしようとします。下、右、左 試行のたびに、外側のコンテナによってパネルが切り取られているかどうかを確認します。 すべての試行が失敗した場合、コンポーネントは、基本パネルの位置を上に移動し、上、右、左の方向からロールアウト試行を繰り返します。 </p> <p>に設定する場合 <span class="codeph"> フィットラテラル</span>の場合、コンポーネントは同様のロジックを使用します。 ベースは、まず右、下、上のロールアウト方向を試して、右に移動します。 次に、ベースを左に移動し、左、下、上のロールアウト方向を試します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
