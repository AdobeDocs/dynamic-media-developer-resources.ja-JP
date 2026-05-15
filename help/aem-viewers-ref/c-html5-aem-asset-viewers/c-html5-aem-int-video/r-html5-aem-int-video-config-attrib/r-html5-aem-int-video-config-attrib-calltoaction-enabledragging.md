---
title: CallToAction.enabledragging
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 21db58df-b76e-4a78-afc4-5e0188cb8896
TQID: 'https://experienceleague.adobe.com/eiQujFJFBcZ5zd0tOLP8wekg3f8j9ssSCNx05tGoW-A'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 88
ht-degree: 5%

---

# CallToAction.enabledragging{#calltoaction-enabledragging}

インタラクティブビデオビューアの設定属性。

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> ユーザーがマウスまたはタッチジェスチャーを使用してサムネールをスクロールできるようにする機能を有効または無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td colname="col2"> <p> は<span class="codeph"> 0 ～ 1 </span>の範囲にあり、実際の速度の間違った方向への移動のパーセント値です。 </p> <p><span class="codeph"> 1 </span>に設定すると、マウスと共に移動します。 </p> <p><span class="codeph"> 0 </span>に設定すると、間違った方向に移動できません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```
