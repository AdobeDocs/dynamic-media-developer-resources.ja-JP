---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,User
exl-id: e375f3ec-82f3-441d-9e01-d0ea5605bd25
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---

# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> すべてのスウォッチに適用される画像サービングコマンド文字列。 URLで指定する場合は、必ず<span class="codeph"> &amp;</span>と<span class="codeph"> =</span>のすべての出現箇所を<span class="codeph"> %26</span>と<span class="codeph"> %3D</span>にそれぞれHTTPエンコードしてください。 </p> <p> <p>注意： 画像のサイズ変更操作コマンドはサポートされていません。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

なし

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

ビューアのURLで指定する場合。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

設定データで指定する場合。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
