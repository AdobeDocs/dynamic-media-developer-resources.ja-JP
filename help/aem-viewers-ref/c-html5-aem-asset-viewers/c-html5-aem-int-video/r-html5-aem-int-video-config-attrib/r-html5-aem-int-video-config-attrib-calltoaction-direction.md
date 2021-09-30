---
title: CallToAction.direction
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---

# CallToAction.direction{#calltoaction-direction}

インタラクティブビデオビューアの設定属性。

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> ビュー内でのサムネールの表示方法を指定します。 </p> <p><span class="codeph"> left </span>に設定して、左から右への入力順序を設定します。 </p> <p><span class="codeph"> right </span>に設定すると順序が逆になり、右から左、上から下の方向に表示されます。 </p> <p>ロケールが<span class="codeph"> "ja" </span>に設定されている場合に、コンポーネントに正しいモードを適用させるには、 <span class="codeph"> auto </span>に設定します。それ以外の場合は、 <span class="codeph">左</span>が使用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
