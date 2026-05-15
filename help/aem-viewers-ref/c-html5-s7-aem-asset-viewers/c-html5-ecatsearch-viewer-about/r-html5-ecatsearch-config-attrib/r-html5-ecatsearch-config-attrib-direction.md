---
title: 方向
description: 方向
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
TQID: 'https://experienceleague.adobe.com/tNKu0P8Sgoxas-opiWd1GWkuWYWDfXE0-j1A-p-j-jM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 206
ht-degree: 2%

---

# 方向{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>メインビューとサムネールでのページの表示方法を指定します。 また、ユーザーがビューアのユーザーインターフェイスとやり取りして、カタログフレーム間で変更する方法も指定します。 </p> <p><span class="codeph">が</span>から離れた場合、最初のページには右揃え、最後のページには左揃えが設定されます。 個々のページサブイメージをつなぎ合わせて、左から右にレンダリングします。 また、カタログを進めるために右から左へのスライドアニメーションを使用するようにメインビューを設定します（<span class="codeph"> PageView.frametransition </span>がスライドに設定されている場合）。 最後に、サムネールを左から右への塗りつぶし順序に設定します。 </p> <p>同様に、<span class="codeph">の右</span>を使用すると、最初のページには左揃え、最後のページには右揃えが設定されます。 個々のページサブイメージをつなぎ合わせて、右から左にレンダリングする順序を設定できます。 また、カタログを進めるために左右のスライドアニメーションを使用するようにメインビューを設定します（<span class="codeph"> PageView.frametransition </span>がスライドに設定されている場合）。 最後に、サムネールの順序を逆にして、サムネールビューを右から左、上から下の方向に塗りつぶします。 </p> <p><span class="codeph">の自動</span>が設定されている場合、ビューアは、ロケールが<span class="codeph"> jaに設定されている場合は<span class="codeph">の右</span> モードを適用します。それ以外の場合は</span>を使用し、残りの<span class="codeph"> モードを使用します。</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-a66ce10d6c0b449883f654e7e0657e2c}

オプション。

## 初期設定 {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## 例 {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
