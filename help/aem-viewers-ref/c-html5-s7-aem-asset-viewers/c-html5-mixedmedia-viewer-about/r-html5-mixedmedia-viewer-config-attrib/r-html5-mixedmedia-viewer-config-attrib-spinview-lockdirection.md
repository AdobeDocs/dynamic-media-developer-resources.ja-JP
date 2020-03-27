---
description: 'null'
seo-description: 'null'
seo-title: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
topic: Dynamic media
uuid: b46a3d78-e381-4351-a4f4-a228386df527
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 2Dスピンセットの場合に、スピンの方向の変更を許可するかどうかを指定します。 </p> <p>1に設定すると、 <span class="codeph"> ジ </span>ェスチャの開始時点でのプライマリのドラッグ方向またはスワイプ方向（水平方向と垂直方向）が指定されます。 その後、ジェスチャが終了するまでその方向を維持します。 例えば、ユーザーが水平スピンを開始した後で、垂直方向にドラッグジェスチャーを続行すると、コンポーネントは垂直スピンを実行しません。その代わりに、マウスまたはスワイプの水平方向の動きのみを考慮します。 </p> <p>値0を指定すると、 <span class="codeph"> ユ </span> ーザーはジェスチャーの進行中にいつでもスピンの方向を変更できます。 スピンセットが1Dの場合、この設定は影響を受けません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
