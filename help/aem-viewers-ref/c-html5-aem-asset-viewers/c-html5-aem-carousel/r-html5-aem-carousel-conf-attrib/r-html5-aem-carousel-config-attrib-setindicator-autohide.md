---
title: SetIndicator.autohide
description: SetIndicator.autohide
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`limit`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> limit</span>]</span> </p> </td> 
   <td colname="col2"> <p> ページ数と実行時のコンポーネントサイズに応じて自動非表示動作を設定します。 </p> <p> <span class="codeph"> 0</span>：自動非表示をオフにします。 </p> <p> <span class="codeph">1</span> 自動非表示を有効にします。 次の条件の 1 つ以上が true の場合、コンポーネントはドットを非表示にします。 </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">ドットの付いた行の幅が、実行時のコンポーネントの幅よりも広くなる。 </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">このコンポーネントに設定されたページの数が、<span class="codeph"><span class="varname"> limit</span></span> パラメーターで設定された制限を超えています。 </li> 
     </ul> </p> <p> 制限 <span class="codeph"><span class="varname">-1</span></span> を <span class="codeph"> に設定すると </span>2 番目の自動非表示条件が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,10`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
