---
description: CarouselView.iscommand
solution: Experience Manager
title: CarouselView.iscommand
feature: Dynamic Mediaクラシック，ビューア，SDK/API，カルーセルバナー
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---


# CarouselView.iscommand{#carouselview-iscommand}

` [CarouselView.|<containerId>_carouselView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> バナーの画像に適用される画像サービングコマンド文字列です。 URLで指定する場合、すべての<span class="codeph"> &amp;</span>および<span class="codeph"> =</span>を<span class="codeph"> %26</span>および<span class="codeph"> %3D</span>としてHTTPエンコードする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

なし

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

ビューアのURLで指定する場合：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

configデータで指定する場合：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
