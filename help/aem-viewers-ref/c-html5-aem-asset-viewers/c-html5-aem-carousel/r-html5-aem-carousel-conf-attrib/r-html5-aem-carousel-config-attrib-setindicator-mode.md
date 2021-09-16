---
title: SetIndicator.mode
description: SetIndicator.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numeric|dotted</span> </p> </td> 
   <td colname="col2"> <p> 設定インジケーターのレンダリングスタイルを設定します。 </p> <p><span class="codeph"> dotted </span>に設定すると、コンポーネントはすべてのページに対して同じインジケーターをレンダリングします。 </p> <p><span class="codeph"> numeric</span>に設定すると、各インジケーター要素内に1から始まるページ番号が配置されます。 </p> <p><span class="codeph">数値</span>操作モードは、タッチ入力を持つデバイスではサポートされていません。 その代わりに、コンポーネントはこのようなデバイスで<span class="codeph"> dotted</span>を使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`dotted`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
