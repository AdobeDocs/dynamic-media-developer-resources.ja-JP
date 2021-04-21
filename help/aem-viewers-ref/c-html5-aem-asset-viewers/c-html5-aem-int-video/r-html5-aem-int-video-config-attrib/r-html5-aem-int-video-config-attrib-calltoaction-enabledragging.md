---
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
title: CallToAction.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 21db58df-b76e-4a78-afc4-5e0188cb8896
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 5%

---

# CallToAction.enabledragging{#calltoaction-enabledragging}

インタラクティブビデオビューアの設定属性。

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> マウスまたはタッチジェスチャを使用してサムネールをスクロールする機能を有効または無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td colname="col2"> <p> が<span class="codeph"> 0-1 </span>の範囲にあり、実際の速度の誤った方向への移動のパーセント値です。 </p> <p><span class="codeph"> 1 </span>に設定すると、マウスと共に移動します。 </p> <p><span class="codeph"> 0 </span>に設定した場合、間違った方向に移動することはできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```
