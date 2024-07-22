---
title: SocialShare.bearing
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ef45ba40-661c-4898-a4df-6293ad799a79
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

スマート切り抜きビデオビューアの設定属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|フィット – 垂直|フィット – 横 </span> </p> </td> 
   <td colname="col2"> <p> ボタンコンテナのスライドアニメーションの方向を指定します。 </p> <p> <span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>、<span class="codeph"> right</span> に設定した場合、パネルは余分な境界チェックなしで指定した方向にロールアウトされ、外部コンテナによってパネルがクリップされる可能性があります。 </p> <p><span class="codeph"> fit-vertical</span> に設定した場合、コンポーネントは最初に基本パネルの位置を SocialShare の下部に移動し、その基本の位置から下、右、または左にパネルをロールアウトしようとします。 試行のたびに、コンポーネントはパネルが外部コンテナによってクリップされているかどうかを確認します。 すべての試行が失敗した場合、コンポーネントは基本パネルの位置を上に移動し、上、右、左の方向でロールアウトの試行を繰り返そうとします。 </p> <p>fit-lateral</span> に設定 <span class="codeph"> ると、コンポーネントは同様のロジックを使用します。 ただし、最初にベースを右、下、上のロールアウト方向に移動し、次にベースを左、左、下、上のロールアウト方向に移動します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```
