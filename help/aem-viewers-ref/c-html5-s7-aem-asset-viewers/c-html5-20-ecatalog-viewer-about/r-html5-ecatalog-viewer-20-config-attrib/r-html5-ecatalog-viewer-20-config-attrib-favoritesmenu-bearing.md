---
title: お気に入りメニュー.bearing
description: ボタン コンテナのスライド アニメーションの方向を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
TQID: 'https://experienceleague.adobe.com/zWVKT6TznkJpBNJ74-vkCnfNkgjBiGJ0dKRVsQnEwvs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# お気に入りメニュー.bearing{#favoritesmenu-bearing}

ボタン コンテナのスライド アニメーションの方向を指定します。

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>、または<span class="codeph"> right</span>に設定すると、パネルは余分な境界チェックなしで指定された方向にロールアウトされ、外部コンテナによってパネルがクリッピングされます。 </p> <p><span class="codeph"> fit-vertical</span>に設定すると、コンポーネントは最初にベースパネルの位置をお気に入りメニューの下部に移動します。 パネルをベースの場所（下、右、左）から次のいずれかの方向にロールアウトしようとします。 コンポーネントは、試行のたびに、パネルが外部コンテナによってクリップされているかどうかを確認します。 すべての試行が失敗した場合、コンポーネントはベースパネルの位置を上に移動し、上、右、左の方向からロールアウトを繰り返します。 </p> <p><span class="codeph"> fit-lateral</span>に設定すると、コンポーネントは同様のロジックを使用します。 ベースは最初に右にシフトされ、右、下、そして上方向に向かって進みます。 次に、ベースを左に移動し、左、下、上の方向にロールアウトします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
