---
title: SocialShare.bearing
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

スマート切り抜きビデオビューアの設定属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> ボタンコンテナのスライドアニメーションの方向を指定します。 </p> <p> に設定する場合 <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>または <span class="codeph"> 右</span>を指定した場合、追加の境界チェックなしでパネルが指定の方向にロールアウトするので、外側のコンテナによってパネルがクリップされる可能性があります。 </p> <p>に設定する場合 <span class="codeph"> fit-vertical</span>を指定した場合、まず、基本パネルの位置が SocialShare の下部に移動し、その基本位置から下部、右部または左側にパネルがロールアウトされようとします。 試行のたびに、外側のコンテナによってパネルが切り取られているかどうかを確認します。 すべての試行が失敗した場合、コンポーネントは、基本パネルの位置を上に移動し、上、右、左の方向でロールアウトの試行を繰り返します。 </p> <p>に設定する場合 <span class="codeph"> フィットラテラル</span>の場合、コンポーネントは同様のロジックを使用します。 ただし、まずベースを右に移動し、右、下、上のロールアウト方向を試してから、ベースを左に移動し、左、下、上のロールアウト方向を試します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```
