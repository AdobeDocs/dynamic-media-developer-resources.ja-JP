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

---


# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral </span> </p> </td> 
   <td colname="col2"> <p> ボタンコンテナのスライドアニメーションの方向を指定します。 </p> <p> up、down、leftまたはrightに設 <span class="codeph"> 定すると、パ </span>ネルは指 <span class="codeph"> 定した方 </span><span class="codeph"></span><span class="codeph"></span>向にロールアウトされ、追加の境界チェックは行われません。 この動作により、外部のコンテナによってパネルが切り取られる場合があります。 </p> <p>fit-verticalを設定す <span class="codeph"></span>ると、コンポーネントは、まずパネルの基本の位置をSocialShareの下部に移動し、その基本の場所から、下、右、左のいずれかからパネルをロールアウトしようとします。 試行のたびに、外側のコンテナによってパネルが切り取られているかどうかを確認します。 すべての試行が失敗した場合、パネルの基本の位置を上に移動し、上、右、左の方向からロールアウト試行を繰り返します。 </p> <p>fit-lateralを設定すると、コンポーネントはfit-verticalと同じロジックを使用しますが、代わりに、ベースを右から順、下、上方向へと移動し、ベースを左、下、上方向へ移動し、左、下、上方向へ移動します。 <span class="codeph"></span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8e843b967237426e9a8b3cd0f27b9820}

（オプション）

## 初期設定 {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## 例 {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
