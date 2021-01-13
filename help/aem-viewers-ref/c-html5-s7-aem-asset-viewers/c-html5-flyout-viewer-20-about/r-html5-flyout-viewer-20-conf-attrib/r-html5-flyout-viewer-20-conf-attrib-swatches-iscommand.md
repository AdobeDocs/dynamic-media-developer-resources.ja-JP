---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
topic: Dynamic media
uuid: a9928350-d9a9-49b0-8990-1f8b67d82f10
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---


# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> すべてのスウォッチに適用される画像サービングコマンド文字列です。 URL内で指定する場合は、<span class="codeph"> &amp;</span>および<span class="codeph"> =</span>をすべて<span class="codeph"> %26</span>および<span class="codeph"> %3D</span>としてHTTPエンコードしてください。 </p> <p> <p>注意： 画像サイズ変更操作コマンドはサポートされていません。 </p> </p> </td> 
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
