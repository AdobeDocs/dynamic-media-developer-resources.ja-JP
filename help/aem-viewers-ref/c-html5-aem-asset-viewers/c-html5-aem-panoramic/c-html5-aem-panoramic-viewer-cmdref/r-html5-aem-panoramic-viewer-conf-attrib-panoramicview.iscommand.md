---
title: PanoramicView.iscommand
description: パノラマビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 4%

---

# PanoramicView.iscommand{#panoramicview-iscommand}

パノラマビューアの設定属性。

` [PanoramicView.|<containerId>_panoramicView.]iscommand=isCommand `

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> 画像に適用される画像サービングコマンド文字列。  URL で指定されている場合は、<span class="codeph"> &amp;</span> と <span class="codeph"> =</span> のすべての出現箇所を、それぞれ <span class="codeph"> %26</span> と <span class="codeph"> %3D</span> として HTTP エンコードしてください。 </p> </td> 
  </tr> 
 </tbody> 
</table>


## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

デフォルトはありません。

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

ビューアの URL で指定された場合。

```
iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000
```

設定データで指定された場合。

```
iscommand=op_sharpen=1&op_colorize=0xff0000
```
