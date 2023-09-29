---
title: textAttr
description: テキストレイヤーの属性。 rtf コマンドとして使用できないテキスト画層の追加属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 1%

---

# textAttr{#textattr}

テキストレイヤーの属性。 rtf コマンドとして使用できないテキスト画層の追加属性を指定します。

` textAttr= *`res`*[, *`antiAliasing`*[, *`resMode`*[, *`wordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span> </span> </p> </td> 
  <td class="stentry"> <p>フォントサイズを変更せずに、テキストレイヤーを拡大・縮小する手段を提供します。 解像度の値を大きくすると、カンバスサイズを基準にレンダリングされたテキストのサイズが大きくなります。値を小さくすると、テキストサイズが小さくなります。 ドット/インチ（0 より大きい整数）単位のテキスト解像度。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> antiAliasing </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストレンダリングエンジンで使用されるアンチエイリアシングモードを制御します。 </p> <p> <span class="codeph"> オフ | norm | crisp | sharp | strong |スムーズ </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> オフ </span> </p> </td> 
      <td class="stentry"> <p>テキストのアンチエイリアスを無効にします。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norm </span> </p> </td> 
      <td class="stentry"> <p>標準テキストのアンチエイリアシングモードを有効にします（デフォルト）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> カリカリ </span> </p> </td> 
      <td class="stentry"> <p>Photoshopアンチエイリアシングモードを選択 <span class="codeph"> カリカリ </span> ( <span class="codeph"> textPs= </span> のみ )。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 鋭い </span> </p> </td> 
      <td class="stentry"> <p>Photoshopアンチエイリアシングモードを選択 <span class="codeph"> 鋭い </span> ( <span class="codeph"> textPs= </span> のみ )。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 強い </span> </p> </td> 
      <td class="stentry"> <p>Photoshopアンチエイリアシングモードを選択 <span class="codeph"> 強い </span> ( <span class="codeph"> textPs= </span> のみ )。 </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストのレンダリング時に res を使用する方法を制御します </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>指定した解像度を使用します。 </p> <p>テキストを合成キャンバスを基準に正確なサイズでレンダリングする場合に使用します。 テキストボックスが小さすぎる場合は、テキストがレイヤーサイズに合わせて切り取られる（指定した場合）ことがあります。 これが唯一の <span class="varname"> resMode </span> サポートされるオプション <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>解像度を自動的に調整して、テキストでレイヤーの直線を最適に埋めます。 </p> <p>切り捨てのリスクを伴うことなく、可能な限りテキストボックスが埋まるように、テキストサイズを自動的に調整する場合に使用します。 テキストの折り返しが有効な場合、最終的な解像度でテキストが再折り返される場合があります。 The <span class="varname"> res </span> 次の場合は無視されます： <span class="codeph"> autoRes </span> が選択されている。 ではサポートされていません <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>指定した解像度を使用します。必要に応じて、テキストがレイヤーの直線に切り捨てられないようにするために、この値を小さくします。 </p> <p>クリッピングが発生しない限り、指定した解像度でテキストをレンダリングする場合に使用します。 クリッピングがある場合は、すべてのテキストがテキストボックス内に完全に収まるように、解像度が自動的に下がります。 テキストの折り返しが有効な場合、最終的な解像度でテキストが再折り返される場合があります。 ではサポートされていません <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>テキストレイヤーのサイズが size=で指定されていない場合、または幅のみが指定されている場合、「autoRes」と「maxRes」の設定は無視されます。 その場合、指定された解像度を使用してテキストがレンダリングされます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap </span> </span> </p> </td> 
  <td class="stentry"> <p>ラッピングモードを指定します。 </p> <p> <span class="codeph"> 折り返し | noWrap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>ワードラップを無効にします。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> まとめる </span> </p> </td> 
      <td class="stentry"> <p>標準のワードラップを有効にします。 </p> <p>必要に応じて、長い言葉を壊します。 <span class="codeph"> textPs= </span> のみがサポート <span class="codeph"> 折り返し </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>改行なしのワードラップを有効にします。 </p> <p>単語が最後に切り捨てられても、単語を壊さないでください。 通常はで使用されます <span class="codeph"> autoRes </span> または <span class="codeph"> maxRes </span> 長い単語が壊れないようにするために。 </p> </td> 
     </tr> 
    </table> </p> <p>両方 <span class="codeph"> 折り返し </span> および <span class="codeph"> nbwrap </span> 単語の境界線とハイフンに対して自動ラップを行います。 </p> </td> 
 </tr> 
</table>

## プロパティ {#section-114ca0b8585b403c873e2251478ad1d5}

テキストレイヤーの属性。 画像、べた塗り、効果の各レイヤーで無視されます。 適用先 `layer=0` 指定されている場合 `layer=comp`.

## 初期設定 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 関連項目 {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
