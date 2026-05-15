---
title: Swatches.iscommand
description: Swatches.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: b5b0acab-4e11-4f6a-8cb1-be6d683d7384
TQID: 'https://experienceleague.adobe.com/wA1OOpLke-8bEv3ybBH4ECwo9QdVe0QiW599A416JmQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
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

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

オプション。

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

なし

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

ビューア URLで指定した場合。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

設定データで指定した場合。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
