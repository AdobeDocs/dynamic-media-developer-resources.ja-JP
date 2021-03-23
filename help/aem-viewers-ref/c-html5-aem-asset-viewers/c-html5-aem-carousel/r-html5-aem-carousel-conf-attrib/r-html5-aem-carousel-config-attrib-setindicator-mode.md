---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
uuid: cfb549c2-e0cf-46c3-b5b7-219c8c1bee94
feature: Dynamic Mediaクラシック，ビューア，SDK/API，カルーセルバナー
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 5%

---


# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numeric|dotted</span> </p> </td> 
   <td colname="col2"> <p> 設定インジケーターのレンダリングスタイルを設定します。 </p> <p><span class="codeph"> dotted</span>に設定すると、コンポーネントはすべてのページに対して同じインジケーターをレンダリングします。 </p> <p><span class="codeph"> numeric</span>に設定すると、各インジケーター要素内に1から始まるページ番号が配置されます。 </p> <p><span class="codeph">数値</span>操作モードは、タッチ入力が可能なデバイスではサポートされません。 その代わりに、コンポーネントはこのようなデバイスで<span class="codeph"> dotted</span>を使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`dotted`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
