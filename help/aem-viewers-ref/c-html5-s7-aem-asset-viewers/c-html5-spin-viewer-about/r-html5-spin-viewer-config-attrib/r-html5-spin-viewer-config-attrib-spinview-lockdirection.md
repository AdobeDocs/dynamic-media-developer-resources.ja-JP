---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
topic: Dynamic Media
uuid: adea34ca-adbe-465e-8991-f39a7a81d611
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---


# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 2Dスピンセットの場合に、スピンの方向の変更を許可するかどうかを指定します。 </p> <p><span class="codeph"> 1 </span>に設定した場合、コンポーネントはジェスチャの開始での主なドラッグ方向またはスワイプ方向（水平方向と垂直方向）を識別します。 その後、ジェスチャーが終わるまで、その方向を維持します。 例えば、ユーザーが水平スピンを開始した後で、垂直方向にドラッグジェスチャーを続行すると、コンポーネントでは垂直スピンが実行されません。その代わりに、マウスまたはスワイプの水平方向の動きのみを考慮します。 </p> <p><span class="codeph"> 0 </span>の値は、ジェスチャの進行中にいつでもユーザーがスピン方向を変更できるようにします。 スピンセットが1Dの場合、この設定は影響を受けません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
