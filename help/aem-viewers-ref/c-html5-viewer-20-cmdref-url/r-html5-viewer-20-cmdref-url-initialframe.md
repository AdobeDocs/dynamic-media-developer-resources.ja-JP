---
description: すべてのビューアに共通のパラメータ。
solution: Experience Manager
title: initialFrame
feature: Dynamic Mediaクラシック，ビューア，SDK/API
role: 開発者、業務従事者
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---

# initialFrame{#initialframe}

すべてのビューアに共通のパラメータ。

>[!NOTE]
>
>このコマンドはビデオ画像ビューアには適用されません。

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> 読み込み時にビューアに表示する、0を基準とするフレームインデックスを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>デバイスが縦向きの場合の、見開きページ内の0を基準とするインデックスです。 「左から右」の環境<span class="codeph"> 0</span>は「左ページ」を意味し、<span class="codeph"> 1</span>は「右ページ」を意味します。 「右から左」では、逆です。<span class="codeph"> 0</span>は「右ページ」を意味し、<span class="codeph"> 1</span>は「左ページ」を意味します。 </p> <p>指定しなかった場合、デフォルトでは<span class="codeph"> 0</span>と見なされます。 デバイスが横置きの場合は無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

（オプション）

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

初期設定はありません。

## 例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
