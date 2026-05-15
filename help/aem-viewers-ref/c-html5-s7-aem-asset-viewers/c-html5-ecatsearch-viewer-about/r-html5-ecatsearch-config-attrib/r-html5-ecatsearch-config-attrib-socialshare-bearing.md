---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fa094d84-927b-48f2-9c82-61f2a446158b
TQID: 'https://experienceleague.adobe.com/YQHHEkxD3goTHedA78xWDI59PaHnM-vOMdjcBa3TNq8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 186
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral </span> </p> </td> 
   <td colname="col2"> <p> ボタン コンテナのスライド アニメーションの方向を指定します。 </p> <p> <span class="codeph"> up </span>、<span class="codeph"> down </span>、<span class="codeph"> left </span>、または<span class="codeph"> right </span>に設定すると、パネルは追加の境界チェックなしで指定された方向にロールアウトされます。 この動作により、外部コンテナによってパネルがクリッピングされる可能性があります。 </p> <p><span class="codeph"> fit-vertical </span>に設定すると、コンポーネントは最初にベースパネルの位置をSocialShareの下部に移動し、そのベースパネルの位置から下部、右側、または左側からロールアウトしようとします。 コンポーネントは試行するたびに、パネルが外部コンテナによってクリップされているかどうかを確認します。 すべての試行が失敗した場合、コンポーネントはベースパネルの位置を上に移動し、上、右、左の方向からロールアウトを繰り返します。 </p> <p><span class="codeph"> fit-lateral </span>に設定すると、コンポーネントはfit-verticalと同様のロジックを使用しますが、代わりにベースを右、下、上のロールアウト方向に移動し、次にベースを左、下、上のロールアウト方向に移動します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8e843b967237426e9a8b3cd0f27b9820}

オプション。

## 初期設定 {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## 例 {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
