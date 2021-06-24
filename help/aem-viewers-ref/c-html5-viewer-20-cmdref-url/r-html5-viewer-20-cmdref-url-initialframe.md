---
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
title: initialFrame
feature: Dynamic Media Classic，ビューア，SDK/API
role: Developer,Business Practitioner
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# initialFrame{#initialframe}

すべてのビューアに共通のパラメーター。

>[!NOTE]
>
>このコマンドは、ビデオ画像ビューアには適用されません。

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> 読み込み時にビューアに表示する、0を基準とするフレームインデックスを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>デバイスが縦向きの場合の、見開き内のページの0を基準とするインデックス。 「左から右」の環境では、<span class="codeph"> 0</span>は「左ページ」を意味し、<span class="codeph"> 1</span>は「右ページ」を意味します。 「右から左」では、逆です。<span class="codeph"> 0</span>は「右ページ」を表し、<span class="codeph"> 1</span>は「左ページ」を表します。 </p> <p>指定しなかった場合、デフォルトでは<span class="codeph"> 0</span>と見なされます。 デバイスが横向きの場合は無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

（オプション）

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

デフォルトはありません。

## 例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
