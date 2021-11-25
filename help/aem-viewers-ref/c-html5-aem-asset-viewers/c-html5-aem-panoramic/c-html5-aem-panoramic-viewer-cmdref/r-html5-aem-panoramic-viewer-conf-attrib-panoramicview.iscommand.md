---
title: PanoramicView.iscommand
description: パノラマビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: null
source-git-commit: 2726733691296fb86b0022ac61ac654848fe83cf
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# PanoramicView.iscommand{#panoramicview-iscommand}

パノラマビューアの設定属性。

` [PanoramicView.|<containerId>_panoramicView.]iscommand=isCommand `

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> 画像に適用される画像サービングコマンド文字列。  URL で指定する場合、 <span class="codeph"> &amp;</span> および <span class="codeph"> =</span> as <span class="codeph"> %26</span> および <span class="codeph"> %3D</span>、それぞれ。 </p> </td> 
  </tr> 
 </tbody> 
</table>


## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

デフォルトはありません。

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

ビューアの URL で指定する場合。

```
iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000
```

config データで指定する場合。

```
iscommand=op_sharpen=1&op_colorize=0xff0000
```
