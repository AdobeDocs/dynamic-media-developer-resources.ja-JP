---
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
title: InteractiveSwatches.enabledragging
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インタラクティブビデオ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 5%

---


# InteractiveSwatches.enabledragging{#interactiveswatches-enabledragging}

インタラクティブビデオビューアの設定属性。

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> マウスまたはタッチジェスチャを使用してスウォッチをスクロールする機能を有効または無効にします。 </p> </td> 
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

