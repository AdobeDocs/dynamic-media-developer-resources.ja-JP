---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Mediaクラシック，ビューア，SDK/API，スピンセット
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 重複クリック/タップとスピン操作を対応付けます。 <span class="codeph"> none </span>に設定すると、重複クリック/タップによるスピンが無効になります。 <span class="codeph"> zoom </span>を指定すると、画像をクリックした場合に1回のスピンステップでスピンします。Ctrlキーを押しながらクリックすると、1つのスピンステップをスピンアウトします。 <span class="codeph"> reset </span>に設定すると、画像をシングルクリックした場合に、初期のスピンレベルまでスピンがリセットされます。 <span class="codeph"> zoomReset </span>の場合、現在のスピン率が指定の限界値以上ならリセットが適用され、それ以外の場合はスピンが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

（オプション）

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`reset` （デスクトップコンピューターの場合） `zoomReset` タッチデバイスの場合。

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
