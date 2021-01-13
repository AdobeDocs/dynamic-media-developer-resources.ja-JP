---
description: SetIndicator.autohide
solution: Experience Manager
title: SetIndicator.autohide
topic: Dynamic media
uuid: eb93ad7a-6176-47ed-92c6-2eb1afcac0eb
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---


# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`制限`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> limit</span>]</span> </p> </td> 
   <td colname="col2"> <p> ページ数と実行時のコンポーネントサイズに応じた自動非表示の動作を設定します。 </p> <p> <span class="codeph"> 0</span> に設定すると、自動非表示がオフになります。 </p> <p> <span class="codeph"> 1</span> は自動非表示を有効にします。次の条件の少なくとも1つがtrueになった場合、コンポーネントのドットは非表示になります。 </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">ドットのある行が実行時のコンポーネントの幅よりも広くなる。 </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">このコンポーネントに設定されたページ数が、<span class="codeph"><span class="varname"> limit</span></span>パラメーターで設定された制限を超えています。 </li> 
     </ul> </p> <p> <span class="codeph"><span class="varname"> limit </span></span>を<span class="codeph"> -1 </span>に設定すると、2番目の自動非表示条件が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,10`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
