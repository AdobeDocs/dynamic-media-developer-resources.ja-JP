---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
TQID: 'https://experienceleague.adobe.com/eTB-wD8G7HGSDgohQn-FsCeFL1GHMBiqzNUtT3nw5n4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 127
ht-degree: 3%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 2D スピンセットがある場合に、スピン方向の変更を許可するかどうかを指定します。 </p> <p><span class="codeph"> 1 </span>に設定すると、コンポーネントは、ジェスチャーの開始時に主要なドラッグまたはスワイプの方向（水平方向と垂直方向の比較）を特定します。 その後、ジェスチャーが終了するまでその方向を維持します。 例えば、ユーザーが水平方向のスピンを開始し、ドラッグのジェスチャーを垂直方向に継続することを決定した場合、コンポーネントは垂直方向のスピンを実行しません。 代わりに、マウスまたはスワイプの水平方向の動きのみを考慮します。 </p> <p>値<span class="codeph"> 0 </span>を指定すると、ユーザーはジェスチャーの進行中にいつでもスピン方向を変更できます。 スピンセットが1Dの場合、この設定は影響しません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
