---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 38c90d7f-ddbc-4123-b90d-02f9cabd785c
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> ダブルクリックまたはタップしてズームアクションへのマッピングを設定します。 なし </span> を <span class="codeph"> に設定すると、ダブルクリックやズームのタップが無効になります。 <span class="codeph"> ズームに設定した場合 </span> 画像をクリックすると、1 回のズームステップでズームします。Ctrl キーを押しながらクリックすると、1 回のズームステップでズームします。 リセット </span> に設定 <span class="codeph"> ると、画像を 1 回クリックするだけで、ズームが初期ズームレベルにリセットされます。 zoomReset </span> では、現在 <span class="codeph"> ズーム率が指定した制限以上の場合はリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-50bcd15223174bb79ce08b31ea03d682}

オプション。

## 初期設定 {#section-7564169749ff4a4996049ea1148cb2a5}

`reset` デスクトップコンピューターの場合 `zoomReset`、タッチデバイスの場合です。

## 例 {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom`
