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
ht-degree: 4%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> ダブルクリック/タップとスピン操作のマッピングを設定します。 を <span class="codeph"> なし </span> ダブルクリック/タップによるスピンを無効にします。 次に設定した場合： <span class="codeph"> ズーム </span>をクリックすると、画像が 1 回のスピンステップでスピンします。Ctrl キーを押しながらクリックすると、1 つのスピンステップをスピンアウトします。 を <span class="codeph"> リセット </span> を指定すると、画像をシングルクリックした場合にスピンが初期のスピンレベルにリセットされます。 の場合 <span class="codeph"> zoomReset </span>、現在のスピン率が指定された制限以上の場合はリセットが適用され、それ以外の場合はスピンが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

（オプション）

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`reset` デスクトップコンピューターの場合： `zoomReset` （タッチデバイス）。

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
