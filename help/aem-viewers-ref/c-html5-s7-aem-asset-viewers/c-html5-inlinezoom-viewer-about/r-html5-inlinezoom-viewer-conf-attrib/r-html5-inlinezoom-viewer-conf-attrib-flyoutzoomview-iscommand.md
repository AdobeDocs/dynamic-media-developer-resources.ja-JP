---
title: FlyoutZoomView.iscommand
description: FlyoutZoomView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 2ae17dc8-2728-4ee5-ba88-45d78a0f4d9a
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---

# FlyoutZoomView.iscommand{#flyoutzoomview-iscommand}

` [FlyoutZoomView.|<containerId>_flyout.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> </p> <p>FlyoutZoomView のメイン画像とズームインビューに適用される画像サービングコマンド文字列。 URL で指定する場合、 <span class="codeph"> &amp;</span> および <span class="codeph"> =</span> as <span class="codeph"> %26</span> および <span class="codeph"> %3D</span>、それぞれ。 </p> <p> <p>注意：画像サイズ変更操作コマンドはサポートされていません。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

なし

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

ビューアの URL で指定する場合：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

設定データで指定する場合：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
