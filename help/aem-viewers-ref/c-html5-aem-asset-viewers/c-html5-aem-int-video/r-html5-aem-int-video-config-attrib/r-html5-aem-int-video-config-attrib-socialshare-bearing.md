---
title: SocialShare.bearing
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
TQID: 'https://experienceleague.adobe.com/qKnLf2xkrrKsHuakGsY4V3hK6LwzuzvGRMSDE4RJKCc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

インタラクティブビデオビューアの設定属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> ボタン コンテナのスライド アニメーションの方向を指定します。 <span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>、または<span class="codeph"> right</span>に設定すると、パネルは指定された方向にロールアウトされ、追加の境界チェックが行われず、その結果、パネルが外部コンテナによってクリッピングされる可能性があります。 </p> <p><span class="codeph"> fit-vertical</span>に設定すると、コンポーネントは最初にベースパネルの位置をSocialShareの下部に移動します。 次に、そのようなベースの場所から次のいずれかの方向にパネルをロールアウトしようとします。下、右、左。 コンポーネントは、試行のたびに、パネルが外部コンテナによってクリップされているかどうかを確認します。 すべての試行が失敗した場合、コンポーネントはベースパネルの位置を上に移動し、上、右、左の方向からロールアウトを繰り返します。 </p> <p><span class="codeph"> fit-lateral</span>に設定すると、コンポーネントは同様のロジックを使用しますが、最初にベースを右にシフトし、右、下、上のロールアウト方向を試します。 次に、ベースを左に移動し、左、下、上のロールアウト方向を試します。 </p> </td> 
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
