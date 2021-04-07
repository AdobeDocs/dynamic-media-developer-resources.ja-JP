---
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
title: InteractiveSwatches.direction
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インタラクティブビデオ
role: 開発者、業務従事者
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '85'
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
