---
title: ZoomView.iscommand
description: ズーム画像に適用される画像サービングコマンド文字列。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 1c24973e-1daf-4d9d-b97c-fb6a18f506ed
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 8%

---

# ZoomView.iscommand{#zoomview-iscommand}

ズーム画像に適用される画像サービングコマンド文字列。

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> URL で指定する場合、 <span class="codeph"> &amp;</span> および <span class="codeph"> =</span> はすべて、 <span class="codeph"> %26</span> および <span class="codeph"> %3D</span> として HTTP エンコードする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

なし

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

ビューアの URL で指定する場合：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

config データで指定する場合：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
