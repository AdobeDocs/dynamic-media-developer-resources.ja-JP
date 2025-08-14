---
title: InteractiveSwatches.direction
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 4%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

インタラクティブビデオビューアの設定属性。

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> スウォッチがビューに表示される方法を指定します。 </p> <p>左 <span class="codeph"> に設定 </span> ると、左から右への塗り潰し順序を設定できます。 </p> <p>[ 右 <span class="codeph"> 設定 ] を選択すると </span> ビューが右から左、上から下の方向に埋められるように順序が逆になります。 </p> <p>自動 <span class="codeph"> が設定され </span> いる場合、ロケールが「<span class="codeph"> ja </span>」に設定されているとコンポーネントは右モードを適用し、それ以外の場合は左 <span class="codeph"> ード </span> 使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
