---
title: SocialShare.bearing
description: SocialShare.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|フィット – 垂直|フィット – 横 </span> </p> </td> 
   <td colname="col2"> <p> ボタンコンテナのスライドアニメーションの方向を指定します。 </p> <p> <span class="codeph"> up </span>、<span class="codeph"> down </span>、<span class="codeph"> left </span>、または <span class="codeph"> right </span> に設定すると、パネルは余分な境界チェックを行わずに指定した方向にロールアウトされます。 この動作により、外部コンテナによってパネルがクリップされる可能性があります。 </p> <p>垂直方向の <span class="codeph"> 合 </span> に設定した場合、コンポーネントはまず基本パネルの位置を SocialShare の下部に移動し、そのような基本位置から下、右、または左からパネルをロールアウトしようとします。 外側のコンテナがパネルをクリップしているかどうかをコンポーネントが毎回確認します。 すべての試行が失敗した場合、コンポーネントはベースパネルの位置を上に移動し、ロールアウトの試行を上、右、左の方向から繰り返そうとします。 </p> <p>fit-lateral </span> に設定 <span class="codeph"> ると、コンポーネントは fit-vertical と同様のロジックを使用します。 ただし、最初に右、下、上のロールアウト方向を試行する際にベースを右にシフトし、次に左、下、上のロールアウト方向を試行する際にベースを左にシフトします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8e843b967237426e9a8b3cd0f27b9820}

オプション。

## 初期設定 {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## 例 {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
