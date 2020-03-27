---
description: 'null'
seo-description: 'null'
seo-title: 方向
solution: Experience Manager
title: 方向
topic: Dynamic media
uuid: 185824c5-d6f2-4e1b-99ac-726a295ec5f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 方向{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>メインビューとサムネールでのページの表示方法を指定します。 また、ユーザがビューアのユーザインターフェイスを操作してカタログフレーム間を変更する方法も指定します。 </p> <p>左揃 <span class="codeph"> えを </span> 使用すると、最初のページが右揃えになり、最後のページが左揃えになります。 左から右へのレンダリングの順序で個々のページのサブ画像をステッチします。 また、右から左のスライドアニメーションを使用してカタログを進めるようにメインビューを設定します( <span class="codeph"> PageView.frametransitionがslideに設定さ </span> れている場合)。 最後に、左から右の塗りつぶし順序にサムネールが設定されます。 </p> <p>同様に、rightを使 <span class="codeph"> 用す </span> ると、最初のページが左揃えになり、最後のページが右揃えになります。 右から左にレンダリングするために、個々のページのサブ画像をステッチします。 また、左から右のスライドアニメーションを使用してカタログを進めるようにメインビューを設定します( <span class="codeph"> PageView.frametransitionがslideに設定さ </span> れている場合)。 最後に、サムネールビューが右から左、上から下の方向に埋まるように、サムネールの順序を逆にします。 </p> <p>autoを設 <span class="codeph"> 定す </span> ると、ロケールがja；に設定されている場合、ビ <span class="codeph"> ューアは右モードを </span><span class="codeph"> 適用します。それ以 </span>外の場合は、左モード <span class="codeph"> が使用さ </span> れます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-a66ce10d6c0b449883f654e7e0657e2c}

（オプション）

## 初期設定 {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## 例 {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
