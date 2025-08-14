---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> シングルクリックまたはタップによるズームアクションのマッピングを設定します。 なし <span class="codeph"> 設定すると </span> シングルクリック/タップズームが無効になります。 スピンに設定した場合 <span class="codeph"> 画像をクリックする </span>、1 回のズームステップでズームします。Ctrl キーを押しながらクリックすると、1 回のズームステップでズームします。 <span class="codeph"> reset </span> に設定すると、画像を 1 回クリックするだけで、ズームが初期スピンレベルにリセットされます。 zoomReset <span class="codeph"> では、現在 </span> ズーム率が指定した制限以上の場合はリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

オプション。

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` デスクトップコンピューターの場合 `none`、タッチデバイスの場合です。

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
