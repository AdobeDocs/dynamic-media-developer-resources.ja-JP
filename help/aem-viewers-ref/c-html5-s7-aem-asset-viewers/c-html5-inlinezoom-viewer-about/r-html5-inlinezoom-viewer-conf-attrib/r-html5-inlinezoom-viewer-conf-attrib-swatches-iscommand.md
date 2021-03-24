---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インラインズーム
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

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

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

（オプション）

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

なし

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

ビューアのURLで指定する場合。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

設定データで指定する場合。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
