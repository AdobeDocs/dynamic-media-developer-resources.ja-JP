---
description: ビデオ360ビューアの設定属性。
seo-description: ビデオ360ビューアの設定属性。
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic Media
uuid: 43217e2e-71c5-4c58-94e0-c6ed38e25a5b
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

ビデオ360ビューアの設定属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> ボタンコンテナのスライドアニメーションの方向を指定します。 </p> <p> <span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>、<span class="codeph"> right</span>に設定すると、追加の境界チェックなしで、指定した方向にパネルがロールアウトし、外部コンテナによってパネルが切り取られる可能性があります。 </p> <p><span class="codeph"> fit-vertical</span>に設定した場合、コンポーネントでは、まずパネルの基本の位置をSocialShareの下部に移動し、その基本の場所から見て、下、右、左のいずれかから、パネルをロールアウトしようとします。 試行のたびに、外側のコンテナでパネルが切り取られているかどうかをチェックします。 すべての試行が失敗すると、パネルの基本の位置を上に移動し、上、右、左の方向でロールアウト試行を繰り返します。 </p> <p><span class="codeph"> fit-lateral</span>に設定した場合も、コンポーネントでは同じロジックが使用されます。 ただし、基本の位置を最初に右に移動し、右、下、上のロールアウト方向を試してから、基本の位置を左に移動し、左、下、上のロールアウト方向を試します。 </p> </td> 
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

