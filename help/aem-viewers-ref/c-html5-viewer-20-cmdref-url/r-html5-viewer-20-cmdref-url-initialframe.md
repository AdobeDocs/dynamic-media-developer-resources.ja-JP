---
title: initialFrame
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---

# initialFrame{#initialframe}

すべてのビューアに共通のパラメーター。

>[!NOTE]
>
>このコマンドはビデオ画像ビューアには適用されません。

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> ビューアが読み込み時に表示するゼロベースのフレームインデックスを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>デバイスが縦になっている場合のスプレッド内のページのゼロベースのインデックス。 「左から右」の環境の場合、<span class="codeph">0 は「左ページ」 </span><span class="codeph">1</span> は「右ページ」を意味します。 「右から左」環境の場合は、逆になります。<span class="codeph"> 0</span> は「右ページ」、<span class="codeph"> 1</span> は「左ページ」を意味します。 </p> <p>指定しない場合、<span class="codeph"> 0</span> がデフォルトで想定されます。 デバイスが横向きの場合は無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

オプション。

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

デフォルトはありません。

## 例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
