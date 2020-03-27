---
description: ズーム画像に適用される画像サービングコマンド文字列。
seo-description: ズーム画像に適用される画像サービングコマンド文字列。
seo-title: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
topic: Dynamic media
uuid: 13dc11ed-52a4-45ae-bfae-ca034c8a3c87
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.iscommand{#zoomview-iscommand}

ズーム画像に適用される画像サービングコマンド文字列。

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> URLで指定する場合、 <span class="codeph"> &amp;と</span> =のすべては <span class="codeph"> %26</span> と%3DのそれぞれにHTTPエンコード <span class="codeph"></span><span class="codeph"></span>します。 </p> </td> 
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
