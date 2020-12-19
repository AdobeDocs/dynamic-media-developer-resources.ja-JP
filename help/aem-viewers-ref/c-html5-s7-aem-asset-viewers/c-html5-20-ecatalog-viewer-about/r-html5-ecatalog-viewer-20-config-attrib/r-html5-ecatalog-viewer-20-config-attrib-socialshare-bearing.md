---
description: 'null'
seo-description: 'null'
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: e48b39bb-c23d-42ce-9dc6-6e8b0d9b04ea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral  </span> </p> </td> 
   <td colname="col2"> <p> ボタンコンテナのスライドアニメーションの方向を指定します。 </p> <p> <span class="codeph"> up </span> 、 <span class="codeph"> down </span> 、 <span class="codeph"> left </span> 、または<span class="codeph"> right </span>に設定すると、追加の境界チェックなしで、パネルは指定した方向にロールアウトします。 この動作により、外側のコンテナでパネルが切り取られる場合があります。 </p> <p><span class="codeph"> fit-vertical </span>に設定した場合、コンポーネントでは、まずパネルの基本の位置をSocialShareの下部に移動し、その基本の場所から見て、下、右、左のいずれかから、パネルをロールアウトしようとします。 試行のたびに、外側のコンテナでパネルが切り取られているかどうかを確認します。 すべての試行が失敗すると、パネルの基本の位置を上に移動して、上、右、左の方向からロールアウト試行を繰り返します。 </p> <p><span class="codeph"> fit-lateral </span>に設定した場合、コンポーネントはfit-verticalと同じロジックを使用しますが、ベースを右から順に右、下、上方向に移動し、ベースを左に移動し、左、下、上方向にロールアウトします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8e843b967237426e9a8b3cd0f27b9820}

（オプション）

## 初期設定 {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## 例 {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
