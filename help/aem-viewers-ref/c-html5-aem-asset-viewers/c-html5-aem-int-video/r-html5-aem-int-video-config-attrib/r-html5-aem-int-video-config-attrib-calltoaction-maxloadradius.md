---
title: CallToAction.maxloadradius
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
TQID: 'https://experienceleague.adobe.com/t8aIHpXr-5-4FhRdZkiHRKgTVLCZEdl2jdSgaSjbT7Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 72
ht-degree: 4%

---

# CallToAction.maxloadradius{#calltoaction-maxloadradius}

インタラクティブビデオビューアの設定属性。

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> コンポーネントのプリロード動作を指定します。 </p> <p><span class="codeph"> -1</span>に設定すると、コンポーネントが初期化されたり、アセットが変更されたりすると、すべてのサムネールが同時に読み込まれます。 </p> <p><span class="codeph">に設定すると、表示されているサムネールのみが読み込まれます。</span> </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span>に設定して、表示領域の周りの非表示の行または列のプリロード数を定義します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`-1`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
