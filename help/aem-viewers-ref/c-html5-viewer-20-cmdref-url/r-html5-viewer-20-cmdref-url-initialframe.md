---
title: initialFrame
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
TQID: 'https://experienceleague.adobe.com/v4kG-OcDN3wmdHDClJHeLR8d2SNcMa5sRQo89Qwig4I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 2%

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
   <td colname="col2"> <p> ビューアが読み込み時に表示するゼロ ベースのフレーム インデックスを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>デバイスが縦向きの場合のスプレッド内のページのゼロから始まるインデックス。 「左から右」の環境の場合、<span class="codeph"> 0</span>は「左ページ」を意味し、<span class="codeph"> 1</span>は「右ページ」を意味します。 「右から左」の環境の場合は逆です。<span class="codeph"> 0</span>は「右ページ」を意味し、<span class="codeph"> 1</span>は「左ページ」を意味します。 </p> <p>指定しない場合、<span class="codeph"> 0</span>はデフォルトで想定されます。 デバイスが横方向にある場合は無視されます。 </p> </td> 
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
