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
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---


# 方向{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p>メイン表示とサムネールでのページの表示方法を指定します。 また、ユーザがビューアのユーザインターフェイスを操作してカタログフレーム間を変更する方法も指定します。 </p> <p><span class="codeph"> left </span>を使用すると、最初のページの右揃えと、最後のページの左揃えが設定されます。 左から右へのレンダリング順序で、個々のページのサブ画像をステッチします。 また、右から左のスライド表示を使用してカタログを進めるようにメインアニメーションを設定します（<span class="codeph"> PageView.frametransition </span>がslideに設定されている場合）。 最後に、左から右の塗りつぶし順にサムネールが設定されます。 </p> <p>同様に、<span class="codeph"> right </span>を使用すると、最初のページの左揃えと最後のページの右揃えが設定されます。 右から左にレンダリングする順序で、個々のページのサブ画像をステッチします。 また、左から右のスライド表示を使用してカタログを進めるようにメインアニメーションを設定します（<span class="codeph"> PageView.frametransition </span>がslideに設定されている場合）。 最後に、サムネールの順序を逆にして、サムネール表示を右から左、上から下の方向に塗りつぶします。 </p> <p><span class="codeph"> auto </span>が設定されている場合、ロケールが<span class="codeph"> ja；に設定されているとき、ビューアは<span class="codeph"> right </span>モードを適用します。</span>それ以外の場合は、<span class="codeph">左</span>モードを使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-a66ce10d6c0b449883f654e7e0657e2c}

（オプション）

## 初期設定 {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## 例 {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
