---
title: SocialShare.bearing
description: SocialShare.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
TQID: 'https://experienceleague.adobe.com/sWilQyllf5wtlr-tP1kKtK4L0taRA6HWQW2Yh0MSefQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral </span> </p> </td> 
   <td colname="col2"> <p> ボタン コンテナのスライド アニメーションの方向を指定します。 </p> <p> <span class="codeph"> up </span>、<span class="codeph"> down </span>、<span class="codeph"> left </span>、または<span class="codeph"> right </span>に設定すると、パネルは余分な境界チェックなしで指定された方向にロールアウトされます。 この動作により、外部コンテナによってパネルがクリッピングされる可能性があります。 </p> <p><span class="codeph"> fit-vertical </span>に設定すると、コンポーネントは最初にベースパネルの位置をSocialShareの下部に移動し、そのベースパネルの位置から下部、右側、または左側からロールアウトしようとします。 コンポーネントは、試行のたびに、パネルが外部コンテナによってクリップされているかどうかを確認します。 すべての試行が失敗した場合、コンポーネントはベースパネルの位置を上に移動し、上、右、左の方向からロールアウトを繰り返します。 </p> <p><span class="codeph"> fit-lateral </span>に設定すると、コンポーネントはfit-verticalと同様のロジックを使用します。 ただし、ベースを右、下、上の順に移動し、次に左、下、上の順に移動します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8e843b967237426e9a8b3cd0f27b9820}

オプション。

## 初期設定 {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## 例 {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`

