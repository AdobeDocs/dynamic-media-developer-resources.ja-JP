---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: 3336c4d2-0d1d-4c6f-8163-8a84a8be8c20
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '70'
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

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

なし

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

ビューアのURLで指定する場合。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

設定データで指定する場合。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
