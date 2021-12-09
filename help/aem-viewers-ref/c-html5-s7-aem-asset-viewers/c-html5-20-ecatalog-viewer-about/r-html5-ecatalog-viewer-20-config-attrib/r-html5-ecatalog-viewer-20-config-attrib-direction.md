---
title: 方向
description: メインビューとサムネールでのページの表示方法を指定します。 また、カタログフレーム間を変更するために、ユーザがビューアのユーザインターフェイスを操作する方法も指定します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7d3df37-3e8b-438f-8b24-035b6982dc14
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 2%

---

# 方向{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>メインビューとサムネールでのページの表示方法を指定します。 また、カタログフレーム間を変更するために、ユーザがビューアのユーザインターフェイスを操作する方法も指定します。 </p> <p>条件 <span class="codeph"> left </span> を使用すると、最初のページの右揃えを設定し、最後のページの左揃えを設定します。 個々のページサブ画像をステッチして、左から右へのレンダリング順序を指定します。 また、右から左のスライドアニメーションを使用してカタログを進めるようにメインビューを設定します ( 場合によっては <span class="codeph"> PageView.frametransition </span> を slide に設定した場合 )。 最後に、左から右の塗りの順序にサムネールが設定されます。 </p> <p>同様に、 <span class="codeph"> 右 </span> を使用すると、最初のページの左揃えが設定され、最後のページの右揃えが設定されます。 個々のページサブ画像をステッチして、右から左にレンダリングする順序を指定します。 また、左から右のスライドアニメーションを使用してカタログを進めるようにメインビューを設定します ( 場合によっては <span class="codeph"> PageView.frametransition </span> を slide に設定した場合 )。 最後に、サムネールの順序を逆にして、サムネールビューが右から左、上から下の方向に埋められるようにします。 </p> <p>条件 <span class="codeph"> auto </span> が設定されている場合、ビューアは適用されます <span class="codeph"> 右 </span> ロケールが <span class="codeph"> ja; </span>それ以外の場合は、 <span class="codeph"> left </span> モード。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-a66ce10d6c0b449883f654e7e0657e2c}

（オプション）

## 初期設定 {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## 例 {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
