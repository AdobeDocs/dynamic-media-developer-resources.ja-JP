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
ht-degree: 3%

---

# CallToAction.direction{#calltoaction-direction}

インタラクティブビデオビューアの設定属性。

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> ビュー内でのサムネイルの埋め込み方法を指定します。 </p> <p>左 <span class="codeph"> に設定 </span> ると、左から右への塗り潰し順序を設定できます。 </p> <p>[ 右 <span class="codeph"> 設定 ] を選択すると </span> ビューが右から左、上から下の方向に埋められるように順序が逆になります。 </p> <p>ロケール <span class="codeph"> 「ja」 </span> ードに設定されている場合にコンポーネントが右モードを適用する <span class="codeph"> は、自動 </span> ードに設定します。それ以外の場合は、左 <span class="codeph"> ード </span> 使用されます。 </p> </td> 
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
