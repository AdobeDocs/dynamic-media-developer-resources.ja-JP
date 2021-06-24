---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media Classic，ビューア，SDK/API，スピンセット
role: Developer,Business Practitioner
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> ダブルクリック/タップとスピン操作のマッピングを設定します。 <span class="codeph"> none </span>に設定すると、ダブルクリック/タップによるスピンが無効になります。 <span class="codeph"> zoom </span>に設定すると、画像をクリックした場合に1回のスピンステップでスピンします。Ctrlキーを押しながらクリックすると、1つのスピンステップがスピンアウトします。 <span class="codeph"> reset </span>に設定すると、画像をシングルクリックした場合に、初期のスピンレベルまでスピンがリセットされます。 <span class="codeph"> zoomReset </span>では、現在のスピン率が指定の限界値以上の場合はリセットが適用され、それ以外の場合はスピンが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

（オプション）

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`reset` （デスクトップコンピューターの場合） `zoomReset` （タッチデバイスの場合）

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
