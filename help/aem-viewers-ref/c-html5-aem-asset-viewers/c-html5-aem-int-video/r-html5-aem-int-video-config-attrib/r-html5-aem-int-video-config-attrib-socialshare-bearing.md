---
title: SocialShare.bearing
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

インタラクティブビデオビューアの設定属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|フィット – 垂直|フィット – 横 </span> </p> </td> 
   <td colname="col2"> <p> ボタンコンテナのスライドアニメーションの方向を指定します。 <span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>、<span class="codeph"> right</span> に設定した場合、パネルは追加の境界チェックなしで指定した方向にロールアウトされ、パネルが外部コンテナによってクリップされる可能性があります。 </p> <p><span class="codeph"> fit-vertical</span> に設定した場合、コンポーネントはまず、基本パネルの位置を SocialShare の一番下に移動します。 次に、そのような基本位置から次のいずれかの方向にパネルを展開しようとします。 外側のコンテナがパネルをクリップしているかどうかをコンポーネントが毎回確認します。 すべての試行が失敗した場合、コンポーネントは基本パネルの位置を上に移動しようと試み、ロールアウトの試行を上、右、左の方向から繰り返します。 </p> <p><span class="codeph"> fit-lateral</span> に設定した場合、コンポーネントは同様のロジックを使用しますが、最初にベースを右に移動し、右、下、上のロールアウト方向を試します。 次に、ベースを左に移動し、ロールアウトの左、下、上の方向を試します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```
