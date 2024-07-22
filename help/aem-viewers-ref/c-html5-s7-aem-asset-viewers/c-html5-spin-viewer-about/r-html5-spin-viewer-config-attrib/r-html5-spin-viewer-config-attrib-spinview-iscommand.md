---
title: SpinView.iscommand
description: SpinView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 6924e133-31f4-4c00-8bcc-25749b52a68d
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---

# SpinView.iscommand{#spinview-iscommand}

` [SpinView.|<containerId>_spinView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> スピン画像に適用される画像サービングコマンド文字列。 URL で指定されている場合、<span class="codeph"> &amp;</span> と <span class="codeph"> =</span> は、それぞれ <span class="codeph"> %26</span> と <span class="codeph"> %3D</span> として HTTP エンコードする必要があります。 </p> <p> <p>メモ：画像サイズ変更操作コマンドはサポートされていません。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

オプション。

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

なし

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

ビューアの URL で指定される場合：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

設定データで指定された場合：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
