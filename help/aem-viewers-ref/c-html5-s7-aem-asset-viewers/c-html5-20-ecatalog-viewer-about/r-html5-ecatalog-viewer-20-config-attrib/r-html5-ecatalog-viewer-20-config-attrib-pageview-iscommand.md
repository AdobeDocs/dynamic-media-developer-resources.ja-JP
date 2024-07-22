---
title: PageView.iscommand
description: PageView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d1b05fe7-901b-4030-9b71-e4e0e5191abf
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---

# PageView.iscommand{#pageview-iscommand}

` [PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> ページ画像に適用される画像サービングコマンド文字列。 URL で指定されている場合、<span class="codeph"> &amp;</span> と <span class="codeph"> =</span> は、それぞれ <span class="codeph"> %26</span> と <span class="codeph"> %3D</span> として HTTP エンコードする必要があります。 </p> <p> <p>メモ：画像サイズ変更操作コマンドはサポートされていません。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-df5a0604766b4ac2b9a6742b377e427c}

オプション。

## 初期設定 {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

なし

## 例 {#section-813de2905d6c44c0991cfe0931581462}

ビューアの URL で指定された場合。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

設定データで指定された場合。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
