---
description: インタラクティブビデオビューアの設定属性。
seo-description: インタラクティブビデオビューアの設定属性。
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: b3978280-7826-44c0-bd25-357e145121f8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# SocialShare.bearing{#socialshare-bearing}

インタラクティブビデオビューアの設定属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> ボタンコンテナのスライドアニメーションの方向を指定します。 をに設定すると、 <span class="codeph"></span><span class="codeph"> 、</span>、 <span class="codeph"> left</span>、 <span class="codeph"></span>またはright upの各境界を指定した方向にロールアウトされ、追加のチェックは行われないので、パネルが外側のコンテナでクリップされる場合があります。 </p> <p>fit-verticalに設定する <span class="codeph"> と</span>、コンポーネントはまずパネルの基本の位置をSocialShareの下部に移動し、その基本の場所から次のいずれかの方向にパネルをロールアウトしようとします。下、右、左 試行のたびに、外側のコンテナによってパネルが切り取られているかどうかがチェックされます。 すべての試行が失敗すると、パネルの基本の位置を上に移動し、上、右、左の方向からロールアウト試行を繰り返します。 </p> <p>fit-lateralを設定すると <span class="codeph"></span>、コンポーネントは同じロジックを使用しますが、基本をまず右に移動し、右、下、上のロールアウト方向を試します。 次に、ベースを左に移動し、左、下、上のロールアウト方向を試します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```

