---
description: FlyoutZoomView.iscommand
solution: Experience Manager
title: FlyoutZoomView.iscommand
feature: Dynamic Media Classic，ビューア，SDK/API，インラインズーム
role: Developer,User
exl-id: 2ae17dc8-2728-4ee5-ba88-45d78a0f4d9a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 6%

---

# FlyoutZoomView.iscommand{#flyoutzoomview-iscommand}

` [FlyoutZoomView.|<containerId>_flyout.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> </p> <p>FlyoutZoomViewのメイン画像とズームインビューに適用される画像サービングコマンド文字列。 URLで指定する場合は、必ず<span class="codeph"> &amp;</span>と<span class="codeph"> =</span>のすべての出現箇所を<span class="codeph"> %26</span>と<span class="codeph"> %3D</span>にそれぞれHTTPエンコードしてください。 </p> <p> <p>注意： 画像のサイズ変更操作コマンドはサポートされていません。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

なし

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

ビューアのURLで指定する場合：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

設定データで指定する場合：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
