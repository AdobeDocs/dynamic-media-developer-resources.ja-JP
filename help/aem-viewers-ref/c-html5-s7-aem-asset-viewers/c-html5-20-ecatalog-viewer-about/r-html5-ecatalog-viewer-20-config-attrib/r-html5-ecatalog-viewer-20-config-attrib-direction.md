---
title: 方向
description: メインビューとサムネールでページを表示する方法を指定します。 また、ユーザがカタログフレーム間を変更するためにビューアのユーザ インタフェースとどのようにやり取りするかについても指定します。
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
   <td colname="col2"> <p>メインビューとサムネールでページを表示する方法を指定します。 また、ユーザがカタログフレーム間を変更するためにビューアのユーザ インタフェースとどのようにやり取りするかについても指定します。 </p> <p>左 </span><span class="codeph"> 使用すると、最初のページに右揃えが設定され、最後のページに左揃えが設定されます。 ページの個々のサブ画像をステッチして、左から右にレンダリングする順序を設定します。 また、PageView.frametransition </span> がスライドに設定されている場合は、右から左にスライドするアニメーションを使用してカタログを進め <span class="codeph"> ようにメイン ビューを設定します。 最後に、サムネールは左から右への塗りつぶし順序に設定されます。 </p> <p>同様に、右 </span> ージ <span class="codeph"> 使用すると、最初のページには左揃えが設定され、最後のページには右揃えが設定されます。 右から左にレンダリングする順序で個々のページサブ画像をステッチします。 また、メイン ビューで左から右へのスライド アニメーションを使用してカタログを進めるように設定します（PageView.frametransition </span> がスライド <span class="codeph"> 設定されている場合）。 最後に、サムネールの順序を反転して、サムネール表示を右から左、上から下の方向に埋めます。 </p> <p><span class="codeph"> auto </span> が設定されていると、locale が <span class="codeph"> ja<span class="codeph"> 設定されているときに、ビューアは右 </span> モードを適用します。それ以外の場合は </span> 左 </span> モード <span class="codeph"> 使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-a66ce10d6c0b449883f654e7e0657e2c}

オプション。

## 初期設定 {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## 例 {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
