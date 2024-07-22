---
title: CarouselView.enableHD
description: CarouselView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *` 数値 `*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> devicePixelRatio</span> が <span class="codeph"> 1</span> より大きいデバ <span class="codeph"> ス、つまりiPhone4 などの高密度ディスプレイを使用するデバイスの最適化を有効、制限、または無効にします。 </p> <p>アクティブの場合、デバイスのピクセル比が <span class="codeph"> 1 しかないかのようにコンポーネントが IS 画像リクエストのサイズを制限し </span> 帯域幅が削減されます。 </p> <p>以下の例を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 数 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> limit</span> 設定を使用する場合、コンポーネントは指定された制限までの高画素密度のみを有効にします。 </p> <p>以下の例を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
