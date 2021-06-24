---
description: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブ画像
role: Developer,Business Practitioner
exl-id: b3cc32ef-dd6c-47a3-9e55-86a43e874a84
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 7%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`番号`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> devicePixelRatio</span>が<span class="codeph"> 1</span>より大きいデバイスの最適化を有効、制限または無効にします。 iPhone4などの高密度ディスプレイを使用するデバイスに影響します。 アクティブにすると、デバイスのピクセル比が<span class="codeph"> 1</span>のように、コンポーネントでIS画像リクエストのサイズが制限され、帯域幅が削減されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 番号</span></span> </p> </td> 
   <td colname="col2"> <p> limit設定を使用すると、指定した制限値までの高ピクセル密度が有効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
