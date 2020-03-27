---
description: ビデオビューアの設定属性。
seo-description: ビデオビューアの設定属性。
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: d7d92d63-a4c2-4bd9-b0fd-fdfd47504a39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SocialShare.bearing{#socialshare-bearing}

ビデオビューアの設定属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> ボタンコンテナのスライドアニメーションの方向を指定します。 </p> <p> をに設定すると、 <span class="codeph"></span><span class="codeph"> 、</span><span class="codeph"> 、</span>left <span class="codeph"> 、</span>、またはright upの各境界を指定した方向にロールアウトし、追加のチェックを行わないでください。その結果、外部コンテナでパネルが切り取られる可能性があります。 </p> <p>fit-verticalを設定すると <span class="codeph"></span>、コンポーネントはまずパネルの基本の位置をSocialShareの下部に移動し、その基本の場所からパネルを下、右または左からロールアウトしようとします。 試行のたびに、外側のコンテナでパネルが切り取られているかどうかがチェックされます。 すべての試行が失敗すると、パネルの基本の位置を上に移動し、上、右、左の方向でロールアウト試行を繰り返します。 </p> <p>fit-lateralを設定すると <span class="codeph"></span>、コンポーネントでも同様のロジックが使用されます。 ただし、まずベースを右に移動し、右、下、上のロールアウト方向を試し、次にベースを左に移動し、左、下、上のロールアウト方向を試します。 </p> </td> 
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

