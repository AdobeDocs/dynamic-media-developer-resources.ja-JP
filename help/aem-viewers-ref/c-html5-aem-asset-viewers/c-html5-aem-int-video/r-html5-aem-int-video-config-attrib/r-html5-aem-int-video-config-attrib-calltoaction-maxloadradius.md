---
title: CallToAction.maxloadradius
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# CallToAction.maxloadradius{#calltoaction-maxloadradius}

インタラクティブビデオビューアの設定属性。

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> コンポーネントのプリロード動作を指定します。 </p> <p><span class="codeph">-1 に設定すると </span> コンポーネントの初期化時またはアセットの変更時に、すべてのサムネールが同時に読み込まれます。 </p> <p><span class="codeph"> 0 に設定すると </span> 表示されているサムネールのみが読み込まれます。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> に設定して、表示可能な領域の周りの非表示の行/列のプリロード数を定義します。 </p> </td> 
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
