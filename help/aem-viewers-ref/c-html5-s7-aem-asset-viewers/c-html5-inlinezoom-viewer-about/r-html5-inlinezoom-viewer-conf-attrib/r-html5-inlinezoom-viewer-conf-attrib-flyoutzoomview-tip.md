---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: df73235b-547e-4d47-aa76-1d2bd4aead9b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`duration`*[, *`count`*][, *`フェード`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>ヒントテキストが非表示になるまでの表示秒数を指定します。 に設定する場合 <span class="codeph"> -1</span>を指定した場合、ユーザーがフライアウトをアクティブにした場合でも、メッセージは常に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p>セット内の新しい画像を表示する際に、テキストが表示される回数を指定します。 値： <span class="codeph"> -1</span> は、セット内の任意の画像を表示する際に、テキストが常に表示されることを意味します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> フェード</span> </span> </p> </td> 
   <td colname="col2"> <p>テキストが表示または非表示になるときに行うフェードアニメーションの時間を指定します。 値： <span class="codeph"> 0</span> は、フェードトランジションがないことを意味します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

（オプション）

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
