---
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インタラクティブビデオ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

インタラクティブビデオビューアの設定属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> ボタンコンテナのスライドアニメーションの方向を指定します。 <span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>、<span class="codeph"> right</span>に設定すると、追加の境界チェックなしで、指定したコンテナにパネルがロールアウトし、パネルが外側の方向にクリップされる場合があります。 </p> <p><span class="codeph"> fit-vertical</span>に設定した場合、コンポーネントでは、まずパネルの基本の位置をSocialShareの下部に移動し、その基本の場所から次のいずれかの方向にパネルをロールアウトしようとします。bottom, right, left。 試行のたびに、外側のコンテナによってパネルが切り取られているかどうかをチェックします。 すべての試行が失敗すると、パネルの基本の位置を上に移動し、上、右、左の方向からロールアウト試行を繰り返します。 </p> <p><span class="codeph"> fit-lateral</span>に設定した場合、コンポーネントは同じロジックを使用しますが、基本の位置をまず右に移動し、右、下、上方向へのロールアウトを試します。 次に、基本の位置を左に移動し、左、下、上方向のロールアウトを試します。 </p> </td> 
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

