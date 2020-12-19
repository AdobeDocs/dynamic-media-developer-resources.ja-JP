---
description: インタラクティブビデオビューアの設定属性。
seo-description: インタラクティブビデオビューアの設定属性。
seo-title: InteractiveSwatches.direction
solution: Experience Manager
title: InteractiveSwatches.direction
topic: Dynamic media
uuid: 08095ab5-f74b-4da6-8f8d-df377995455e
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 4%

---


# InteractiveSwatches.direction{#interactiveswatches-direction}

インタラクティブビデオビューアの設定属性。

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> 表示内でのスウォッチの塗りつぶし方法を指定します。 </p> <p>左から右の塗りの順序を設定するには、<span class="codeph">左</span>に設定します。 </p> <p><span class="codeph"> right </span>に設定すると順序が逆になり、右から左、上から下に表示が入力されます。 </p> <p><span class="codeph"> auto </span>が設定されている場合、ロケールが" <span class="codeph"> ja </span>"に設定されていると、コンポーネントはrightモードを適用します。それ以外の場合は、<span class="codeph"> left </span>が使用されます。 </p> </td> 
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

