---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
uuid: 11458300-4a1b-4623-8ea1-db804daab3cf
feature: Dynamic Mediaクラシック，ビューア，SDK/API,eCatalog
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 6%

---


# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *``*[, *`脚`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 手順</span></span> </p> </td> 
   <td colname="col2"> <p> 倍または半分の解像度に達するために必要なズームインおよびズームアウト操作の回数を設定します。 1回のズーム操作で変化する解像度は、1ステップあたり2^1です。 1回のズーム操作で最大解像度までズームする場合は、<span class="codeph"> 0</span>に設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 制限</span></span> </p> </td> 
   <td colname="col2"> <p> 最大解像度の画像を基準とする最大ズーム解像度を指定します。 デフォルトは<span class="codeph"> 1.0</span>で、最大解像度以上にズームできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-636d35a4791447039f1902973f568320}

（オプション）

## 初期設定 {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## 例 {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
