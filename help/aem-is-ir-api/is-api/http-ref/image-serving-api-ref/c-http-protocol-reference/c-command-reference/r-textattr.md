---
title: textAttr
description: テキストレイヤー属性。 rtf コマンドとして使用できないテキストレイヤーの追加属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# textAttr{#textattr}

テキストレイヤー属性。 rtf コマンドとして使用できないテキストレイヤーの追加属性を指定します。

` textAttr= *`res`*[, *`antiAliasing`*[, *`resMode`*[, *`wordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span> </span> </p> </td> 
  <td class="stentry"> <p>フォントサイズを変更せずにテキストレイヤーを拡大・縮小する手段を提供します。 解像度の値を大きくすると、キャンバス サイズに対して相対的にレンダリングされるテキストのサイズが大きくなり、値を小さくするとテキスト サイズが小さくなります。 1 インチあたりのドット数（0 より大きい整数）のテキスト解像度。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> antiAliasing </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストレンダリングエンジンで使用されるアンチエイリアスモードを制御します。 </p> <p> <span class="codeph"> off |標準 |鮮明 | シャープ |強 |滑らかな </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> off </span> </p> </td> 
      <td class="stentry"> <p>テキストのアンチエイリアシングを無効にします。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 標準 </span> </p> </td> 
      <td class="stentry"> <p>標準テキストアンチエイリアスモードを有効にします（デフォルト）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> </span><span class="codeph"> 鮮明に </p> </td> 
      <td class="stentry"> <p>Photoshop アンチエイリアシング モード <span class="codeph"> クリスプ </span> スを選択します（<span class="codeph"> textPs= </span> のみ）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> sharp </span> </p> </td> 
      <td class="stentry"> <p>「Photoshop アンチエイリアシング」を選択 <span class="codeph">、「シャープ </span> イリアス」を選択します（<span class="codeph"> textPs= </span> のみ）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 強 </span> </p> </td> 
      <td class="stentry"> <p>Photoshop アンチエイリアシング モード <span class="codeph"> 強 </span> を選択します（<span class="codeph"> textPs= </span> のみ）。 </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストのレンダリング時の解像度の使用方法をコントロールします </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>指定した解像度を使用します。 </p> <p>合成キャンバスに対して正確なサイズでテキストをレンダリングする場合は、を使用します。 テキストボックスが小さすぎると、テキストがレイヤーサイズに切り取られる場合があります（指定した場合）。 これは、<span class="codeph"> textPs= </span> でサポートされている唯一の <span class="varname"> resMode </span> オプションです。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>解像度を自動的に調整して、レイヤーレコードをテキストで最適に塗りつぶします。 </p> <p>切り捨てのリスクを避けるために、テキストボックスができるだけ埋められるようにテキストサイズを自動調整するために使用します。 ワードラップが有効な場合、テキストは最終的な解像度で再度折り返されます。 autoRes </span> が選択されている場合、<span class="varname"> res </span> は無視 <span class="codeph"> れます。 <span class="codeph"> textPs= </span> ではサポートされていません。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>指定した解像度を使用します。必要に応じて、テキストがレイヤーレクトに切り捨てられないようにする場合は、解像度を下げます。 </p> <p>クリッピングが発生しない限り、を使用して、指定した解像度でテキストをレンダリングします。 クリッピングがある場合は、すべてのテキストがテキストボックス内に完全に含まれるように、解像度が自動的に下げられます。 ワードラップが有効な場合、テキストは最終的な解像度で再度折り返されます。 <span class="codeph"> textPs= </span> ではサポートされていません。 </p> </td> 
     </tr> 
    </table> </p> <p>テキストレイヤーのサイズが size=で指定されていない場合、または幅のみが指定されている場合、「autoRes」および「maxRes」の設定は無視されます。 この場合、テキストのレンダリングには指定の解像度が使用されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap </span> </span> </p> </td> 
  <td class="stentry"> <p>ラッピング モードを指定します。 </p> <p> <span class="codeph"> ラップ | noWrap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>ワードラップを無効にします。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> wrap </span> </p> </td> 
      <td class="stentry"> <p>標準のワードラップを有効にします。 </p> <p>必要なら長い言葉を使っても大丈夫だ。 <span class="codeph"> textPs= </span> は、折り返し </span> のみサポ <span class="codeph"> トします。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>改行なしのワードラップを有効にします。 </p> <p>単語の末尾が切り詰められても、単語を区切らないようにします。 通常 <span class="codeph">autoRes </span> または <span class="codeph"> maxRes </span> と一緒に使用して、長い単語が壊れないようにします。 </p> </td> 
     </tr> 
    </table> </p> <p></span><span class="codeph"> 折り返しと nbwrap の両方 <span class="codeph">、単語の境界とハイフン </span> 自動的に折り返します。 </p> </td> 
 </tr> 
</table>

## プロパティ {#section-114ca0b8585b403c873e2251478ad1d5}

テキストレイヤーの属性。 画像、単色、エフェクトのレイヤーで無視されます。 `layer=comp` に対して指定されている場合は、`layer=0` に適用されます。

## 初期設定 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 関連項目 {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
