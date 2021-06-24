---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: c2aeb45f-879b-4a53-b571-744fc73d04fd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 2Dスピンセットの場合に、スピン方向の変更を許可するかどうかを指定します。 </p> <p><span class="codeph"> 1 </span>に設定した場合、コンポーネントはジェスチャの開始時に、主なドラッグ方向またはスワイプ方向（水平方向と垂直方向）を識別します。 その後、ジェスチャーが終わるまでその方向を維持します。 例えば、ユーザーが水平方向のスピンを開始し、ドラッグ操作を垂直方向に続行すると、コンポーネントは垂直方向のスピンを実行しません。代わりに、マウスまたはスワイプの水平移動のみを考慮します。 </p> <p>値<span class="codeph"> 0 </span>を指定すると、ユーザーはジェスチャの進行中にいつでもスピン方向を変更できます。 スピンセットが1Dの場合、この設定は影響を受けません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
