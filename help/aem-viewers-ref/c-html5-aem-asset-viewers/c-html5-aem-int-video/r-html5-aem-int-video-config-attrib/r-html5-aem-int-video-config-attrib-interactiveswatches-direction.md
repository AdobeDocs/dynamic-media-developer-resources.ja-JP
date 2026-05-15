---
title: InteractiveSwatches.direction
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
TQID: 'https://experienceleague.adobe.com/Rl1O2CZOwu8Fp9kNIrHIGV2Ef09ssznrrrRV5J3-Gfc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 3%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

インタラクティブビデオビューアの設定属性。

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> スウォッチがビュー内で塗りつぶされる方法を指定します。 </p> <p>左から右への入力順序を設定するには、<span class="codeph">を左から</span>に設定します。 </p> <p><span class="codeph">に設定すると、ビューが右から左、上から下の方向に塗りつぶされるように、順序が逆になります。</span> </p> <p><span class="codeph">自動</span>が設定されている場合、ロケールが「<span class="codeph"> ja </span>」に設定されている場合、コンポーネントは右モードを適用します。それ以外の場合は、<span class="codeph">左</span>が使用されます。 </p> </td> 
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
