---
description: ズーム画像に適用される画像サービングコマンド文字列。
solution: Experience Manager
title: ZoomView.iscommand
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブ画像
role: Developer,User
exl-id: 1c24973e-1daf-4d9d-b97c-fb6a18f506ed
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 7%

---

# ZoomView.iscommand{#zoomview-iscommand}

ズーム画像に適用される画像サービングコマンド文字列。

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> URLで指定する場合、 <span class="codeph"> &amp;</span>と<span class="codeph"> =</span>はすべて、 <span class="codeph"> %26</span>と<span class="codeph"> %3D</span>にそれぞれHTTPエンコードする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

なし

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

ビューアのURLで指定する場合：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

configデータで指定する場合：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
