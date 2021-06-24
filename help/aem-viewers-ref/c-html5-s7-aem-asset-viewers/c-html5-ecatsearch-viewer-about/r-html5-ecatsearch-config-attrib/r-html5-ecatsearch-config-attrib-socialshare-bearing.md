---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,Business Practitioner
exl-id: fa094d84-927b-48f2-9c82-61f2a446158b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral  </span> </p> </td> 
   <td colname="col2"> <p> ボタンコンテナのスライドアニメーションの方向を指定します。 </p> <p> <span class="codeph"> up </span> 、 <span class="codeph"> down </span> 、 <span class="codeph"> left </span> 、または<span class="codeph"> right </span>に設定すると、追加の境界チェックなしで、パネルが指定の方向にロールアウトします。 この動作により、外側のコンテナによってパネルが切り取られる場合があります。 </p> <p><span class="codeph"> fit-vertical </span>に設定すると、コンポーネントは、まずパネルの基本の位置をSocialShareの下部に移動し、その基本の場所から下、右、左のいずれかからパネルをロールアウトしようとします。 試行のたびに、外側のコンテナによってパネルが切り取られているかどうかがチェックされます。 すべての試行が失敗した場合、コンポーネントは基本パネルの位置を上に移動し、上、右、左の方向からロールアウト試行を繰り返します。 </p> <p><span class="codeph"> fit-lateral </span>に設定した場合、コンポーネントではfit-verticalと同じロジックを使用しますが、代わりに、ベースを右から右、下、上方向に移動し、ベースを左に移動し、左、下、上方向に移動します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8e843b967237426e9a8b3cd0f27b9820}

（オプション）

## 初期設定 {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## 例 {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
