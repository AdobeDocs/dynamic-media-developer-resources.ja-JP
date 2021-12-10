---
title: SocialShare.bearing
description: SocialShare.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral </span> </p> </td> 
   <td colname="col2"> <p> ボタンコンテナのスライドアニメーションの方向を指定します。 </p> <p> に設定する場合 <span class="codeph"> up </span>, <span class="codeph"> down </span>, <span class="codeph"> left </span>または <span class="codeph"> 右 </span>を指定した場合、パネルは特別な境界チェックなしで指定した方向にロールアウトします。 この動作により、外側のコンテナによってパネルがクリップされる場合があります。 </p> <p>に設定する場合 <span class="codeph"> fit-vertical </span>を選択した場合、コンポーネントはまず、パネルの基本位置を SocialShare の下部に移動し、その基本位置から下、右、左のいずれかからパネルをロールアウトしようとします。 試行のたびに、外側のコンテナによってパネルが切り取られているかどうかを確認します。 すべての試行が失敗した場合、コンポーネントは、基本パネルの位置を上に移動し、上、右、左の方向からロールアウトの試行を繰り返します。 </p> <p>に設定する場合 <span class="codeph"> フィットラテラル </span>の場合、コンポーネントは fit-vertical と同じロジックを使用します。 ただし、ベースは右、下、上の順に右から順に移動し、次にベースを左に移動し、左、下、上のロールアウト方向を試します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8e843b967237426e9a8b3cd0f27b9820}

（オプション）

## 初期設定 {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## 例 {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
