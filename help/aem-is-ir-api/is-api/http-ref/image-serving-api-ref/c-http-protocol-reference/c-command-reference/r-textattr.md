---
description: テキストレイヤーの属性。 rtfコマンドとして使用できないテキストレイヤーの追加属性を指定します。
seo-description: テキストレイヤーの属性。 rtfコマンドとして使用できないテキストレイヤーの追加属性を指定します。
seo-title: textAttr
solution: Experience Manager
title: textAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 07b3d263-2ed6-4363-83e1-3b841e9967c5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# textAttr{#textattr}

テキストレイヤーの属性。 rtfコマンドとして使用できないテキストレイヤーの追加属性を指定します。

` textAttr= *`ResantiAliasingresModewordWrap`*[, *``*[, *``*[, *``*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span></span> </p> </td> 
  <td class="stentry"> <p>フォントサイズを変更せずにテキストレイヤーを拡大・縮小する手段を提供します。 解像度の値を高くすると、カンバスサイズを基準にしてレンダリングされたテキストのサイズが大きくなります。値を小さくすると、テキストサイズが小さくなります。 テキストの解像度(ドット/インチ（0より大きい整数）)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> アンチエ <span class="varname"> イリア </span> ス </span> </p> </td> 
  <td class="stentry"> <p>テキストレンダリングエンジンで使用するアンチエイリアスモードを制御します。 </p> <p> <span class="codeph"> off| norm| crisp|シャープ| strong|スムーズ </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> オフ </span> </p> </td> 
      <td class="stentry"> <p>テキストのアンチエイリアスを無効にします。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norm </span> </p> </td> 
      <td class="stentry"> <p>標準テキストのアンチエイリアスモードを有効にします（初期設定）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> パリ </span> </p> </td> 
      <td class="stentry"> <p>「Photoshopアンチエイリアシングモード」を選 <span class="codeph"> 択します( </span> テキ <span class="codeph"> ストPs= </span> のみ)。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 鋭い </span> </p> </td> 
      <td class="stentry"> <p>「Photoshopアンチエイリアスモード」で「シャープ」を <span class="codeph"> 選択します( </span> テキ <span class="codeph"> ストPs= </span> のみ)。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 強 </span> </p> </td> 
      <td class="stentry"> <p>「Photoshopアンチエイリアスモード（強）」 <span class="codeph"> を選択し </span> ます( <span class="codeph"> textPs= </span> のみ)。 </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストのレンダリング時にresを使用する方法を制御します </p> <p> <span class="codeph"> fixedRes| autoRes| maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>指定した解像度を使用します。 </p> <p>テキストを合成キャンバスに対して正確なサイズでレンダリングする場合に使用します。 テキストボックスが小さすぎる場合、テキストが（指定した場合）レイヤーサイズに合わせて切り抜かれる場合があります。 これは、textPs=でサポ <span class="varname"> ートさ </span> れる唯一のresMode <span class="codeph"> オプションで </span>す。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>レイヤーの長方形をテキストで埋めるのに最適な解像度になるように、解像度を自動的に調整します。 </p> <p>テキストボックスが切り捨てられるおそれがなく、できる限り埋まるようにテキストサイズを自動的に調整する場合に使用します。 折り返しを有効にすると、最終的な解像度でテキストが再び折り返される場合があります。 <span class="varname"> autoResが選 </span> 択されている場合、 <span class="codeph"> resは無 </span> 視されます。 textPs=ではサポー <span class="codeph"> トされませ </span>ん。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>指定した解像度を使用します。必要に応じて、テキストがレイヤー領域に切り詰められないように減らします。 </p> <p>クリッピングが発生しない限り、指定した解像度でテキストをレンダリングする場合に使用します。 クリッピングの場合、解像度は自動的に下がり、すべてのテキストがテキストボックス内に完全に収まるようになります。 折り返しを有効にすると、最終的な解像度でテキストが再び折り返される場合があります。 textPs=ではサポー <span class="codeph"> トされませ </span>ん。 </p> </td> 
     </tr> 
    </table> </p> <p>テキストレイヤーのサイズがsize=で指定されていない場合、または幅のみが指定されている場合、「autoRes」と「maxRes」の設定は無視され、指定された解像度を使用してテキストがレンダリングされます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 折り <span class="varname"> 返 </span> し </span> </p> </td> 
  <td class="stentry"> <p>折り返しモードを指定します。 </p> <p> <span class="codeph"> ラップ| noWrap| nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>ワードラップを無効にします。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> まとめる </span> </p> </td> 
      <td class="stentry"> <p>標準のワードラップを有効にします。 </p> <p>必要に応じて、長い単語を改行します。 <span class="codeph"> textPs=では折り返 </span> しのみがサポ <span class="codeph"> ートされま </span>す。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>改行しないワードラップを有効にします。 </p> <p>単語の末尾が切り捨てられた場合でも、単語を改行しない。 通常、長い単語が壊れないように <span class="codeph"> 、autoRes </span> または <span class="codeph"> maxRes </span> と組み合わせて使用されます。 </p> </td> 
     </tr> 
    </table> </p> <p>折り返し <span class="codeph"> とnbwrapの両方 </span> が、単語の境界とハ <span class="codeph"></span> イフンに対して自動的に折り返されます。 </p> </td> 
 </tr> 
</table>

## プロパティ {#section-114ca0b8585b403c873e2251478ad1d5}

テキストレイヤー属性。 画像、べた塗りおよびエフェクトレイヤーでは無視されます。 に対して指定さ `layer=0` れた場合に適用されま `layer=comp`す。

## 初期設定 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 関連項目 {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
