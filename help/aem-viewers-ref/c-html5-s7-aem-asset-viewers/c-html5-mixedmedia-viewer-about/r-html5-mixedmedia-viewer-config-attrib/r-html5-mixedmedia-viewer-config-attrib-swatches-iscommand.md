---
title: Swatches.iscommand
description: Swatches.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3336c4d2-0d1d-4c6f-8163-8a84a8be8c20
TQID: 'https://experienceleague.adobe.com/A7LV2abrarLD794qk3NzbkR3WZfJQ1QttFBCwm80PeI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 63
ht-degree: 6%

---

# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> すべてのスウォッチに適用される画像サービングコマンド文字列。 URLで指定されている場合は、<span class="codeph"> &amp;</span>および<span class="codeph"> =</span>のすべての出現箇所を、それぞれ<span class="codeph"> %26</span>および<span class="codeph"> %3D</span>としてHTTP エンコードしてください。 </p> <p> <p>注意：画像サイズ変更の操作コマンドはサポートされていません。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

なし

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

ビューア URLで指定した場合。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

設定データで指定した場合。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
