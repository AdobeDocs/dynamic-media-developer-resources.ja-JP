---
description: 'null'
seo-description: 'null'
seo-title: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
topic: Dynamic media
uuid: b5dfb326-fbd8-4220-a44c-0d4f80b2a8fa
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 7%

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

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

なし

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

ビューアのURLで指定する場合。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

設定データで指定する場合。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
