---
description: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,Business Practitioner
exl-id: 3fd5b907-faf6-4d36-8ee1-79f3ace781d4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> シングルクリック/タップとズーム操作との対応関係を設定します。<span class="codeph"> none </span>に設定すると、シングルクリック/タップによるズームが無効になります。 <span class="codeph"> zoom </span>に設定すると、画像をクリックした場合に1段階ズームインします。Ctrlキーを押しながらクリックすると、1段階ズームアウトします。 <span class="codeph"> reset </span>に設定すると、画像をシングルクリックした場合に、初期のズームレベルまでズームがリセットされます。 <span class="codeph"> zoomReset </span>の場合、現在のズーム率が指定の限界値以上であればリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`zoomReset` （デスクトップコンピューターの場合） `none` （タッチデバイスの場合）

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
