---
title: SetIndicator.autohide
description: SetIndicator.autohide
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`制限`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[, <span class="varname"> limit</span> ]</span> </p> </td> 
   <td colname="col2"> <p> ページ数と実行時のコンポーネントサイズに応じて、自動非表示の動作を設定します。 </p> <p> <span class="codeph"> 0を指定すると、</span> 自動非表示がオフになります。 </p> <p> <span class="codeph"> 1</span> を指定すると、自動非表示が有効になります。次の条件の1つ以上がtrueになった場合、コンポーネントのドットは非表示になります。 </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">ドット付きの行は、実行時のコンポーネントの幅よりも幅が広くなります。 </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">このコンポーネントに設定されているページ数が、<span class="codeph"><span class="varname"> limit</span></span>パラメーターで設定されている制限を超えています。 </li> 
     </ul> </p> <p> <span class="codeph"><span class="varname"> limit</span></span>を<span class="codeph"> -1</span>に設定すると、2番目の自動非表示条件が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,10`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
