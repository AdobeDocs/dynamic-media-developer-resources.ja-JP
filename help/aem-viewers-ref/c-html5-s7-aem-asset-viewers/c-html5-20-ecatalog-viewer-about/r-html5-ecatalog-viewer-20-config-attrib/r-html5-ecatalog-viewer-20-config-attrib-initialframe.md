---
description: InitialFrame
solution: Experience Manager
title: InitialFrame
feature: Dynamic Mediaクラシック，ビューア，SDK/API,eCatalog
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 8%

---


# InitialFrame{#initialframe}

` initialFrame= *`frame`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> frame</span></span> </p> </td> 
   <td colname="col2"> <p> ビューアの読み込み時に表示する、0を基準とする見開きのインデックスを指定します。 このインデックスは、横置きモードでの見開きのインデックスと一致します。 ビューアを縦長に回転すると、<span class="codeph"> frameIdx</span>が指す見開きの左端のページが表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-fc7c012c91d1419b8a5bb60d28e17327}

（オプション）

## 初期設定 {#section-bbc6ebad3af54fd79837515c270e6ddf}

`0`

## 例 {#section-cbc6684eb22e4d0883edc4b3d5742336}

ビューアのURLで指定する場合。

```
initialFrame=2
```

