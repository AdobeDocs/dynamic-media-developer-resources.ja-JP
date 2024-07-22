---
description: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4e843866-75a5-4543-a275-e134b3aee75a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 8%

---

# SearchPanel.iscommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> すべてのサムネイルに適用される画像サービングコマンド文字列。 URL で指定されている場合、<span class="codeph"> &amp;</span> と <span class="codeph"> =</span> は、それぞれ <span class="codeph"> %26</span> と <span class="codeph"> %3D</span> として HTTP エンコードする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-df5a0604766b4ac2b9a6742b377e427c}

オプション。

## 初期設定 {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

なし

## 例 {#section-813de2905d6c44c0991cfe0931581462}

ビューアの URL で指定された場合。

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

設定データで指定された場合。

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
