---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> ダブルクリックまたはタップによるスピンアクションのマッピングを設定します。 <span class="codeph"> なし」に設定すると、ダブルクリック </span> スピンのタップが無効になります。 ズーム </span> を <span class="codeph"> に設定した場合、画像をクリックすると 1 回のスピンステップでスピンします。Ctrl キーを押しながらクリックすると、1 回のスピンステップでスピンします。 <span class="codeph"> reset </span> に設定すると、画像を 1 回クリックするだけで、スピンが初期スピンレベルにリセットされます。 zoomReset </span> では、現在 <span class="codeph"> スピン率が指定した制限以上の場合はリセットが適用され、それ以外の場合はスピンが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

オプション。

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

デスクトップコンピューターでは `reset`、タッチデバイスでは `zoomReset` を使用します。

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
