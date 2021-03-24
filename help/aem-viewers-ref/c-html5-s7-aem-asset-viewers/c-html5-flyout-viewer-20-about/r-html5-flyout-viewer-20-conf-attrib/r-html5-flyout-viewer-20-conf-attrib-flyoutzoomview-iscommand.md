---
description: FlyoutZoomView.iscommand
solution: Experience Manager
title: FlyoutZoomView.iscommand
feature: Dynamic Mediaクラシック，ビューア，SDK/API，フライアウト
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---


# FlyoutZoomView.iscommand{#flyoutzoomview-iscommand}

` [FlyoutZoomView.|<containerId>_flyout.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> </p> <p>FlyoutZoomViewのメイン画像とズームインされた表示に適用される画像サービングコマンド文字列。 URL内で指定する場合は、<span class="codeph"> &amp;</span>および<span class="codeph"> =</span>をすべて<span class="codeph"> %26</span>および<span class="codeph"> %3D</span>としてHTTPエンコードしてください。 </p> <p> <p>注意： 画像サイズ変更操作コマンドはサポートされていません。 </p> </p> </td> 
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
