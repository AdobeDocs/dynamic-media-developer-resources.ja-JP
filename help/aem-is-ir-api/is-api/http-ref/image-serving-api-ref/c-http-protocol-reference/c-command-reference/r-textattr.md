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
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 1%

---


# textAttr{#textattr}

テキストレイヤーの属性。 rtfコマンドとして使用できないテキストレイヤーの追加属性を指定します。

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res  </span> </span> </p> </td> 
  <td class="stentry"> <p>フォントサイズを変更せずに、テキストレイヤーを拡大縮小する手段を提供します。 解像度の値を高くすると、カンバスサイズを基準にしてレンダリングされるテキストのサイズが大きくなります。値を小さくすると、テキストサイズが小さくなります。 テキストの解像度（ドット/インチ）（0より大きい整数）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> antiAliasing  </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストレンダリングエンジンで使用するアンチエイリアスモードを制御します。 </p> <p> <span class="codeph"> off | norm | crisp | sharp | strong |スムーズ  </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> オフ </span> </p> </td> 
      <td class="stentry"> <p>テキストのアンチエイリアスを無効にします。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norm  </span> </p> </td> 
      <td class="stentry"> <p>標準テキストのアンチエイリアシングモードを有効化（初期設定） </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> カリカリ  </span> </p> </td> 
      <td class="stentry"> <p>Photoshopのアンチエイリアスモード<span class="codeph"> crisp </span>を選択します（ <span class="codeph"> textPs= </span>のみ）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 鋭い  </span> </p> </td> 
      <td class="stentry"> <p>Photoshopのアンチエイリアシングモード<span class="codeph"> sharp </span>を選択します（ <span class="codeph"> textPs= </span>のみ）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 強 </span> </p> </td> 
      <td class="stentry"> <p>Photoshopのアンチエイリアスモード<span class="codeph"> strong </span>を選択します（ <span class="codeph"> textPs= </span>のみ）。 </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストのレンダリング時にresを使用する方法を制御します </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes  </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes  </span> </p> </td> 
      <td class="stentry"> <p>指定した解像度を使用します。 </p> <p>テキストを合成キャンバスに対して正確なサイズでレンダリングする場合に使用します。 テキストボックスが小さすぎる場合、テキストがレイヤーサイズに合わせて切り取られる場合があります（指定した場合）。 <span class="codeph"> textPs= </span>でサポートされる<span class="varname"> resMode </span>オプションはこれだけです。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes  </span> </p> </td> 
      <td class="stentry"> <p>レイヤーの長方形をテキストで埋めるのに最適な解像度になるように、解像度を自動的に調整します。 </p> <p>テキストボックスができる限り大きく埋まるように、テキストサイズを自動的に調整する場合に使用します。切り捨ての危険はありません。 折り返しを有効にすると、最終的な解像度でテキストが再折り返される場合があります。 <span class="varname"> autoRes </span> が選択されている場合、resは無視さ <span class="codeph">  </span> れます。<span class="codeph"> textPs= </span>ではサポートされていません。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes  </span> </p> </td> 
      <td class="stentry"> <p>指定した解像度を使用します。必要に応じて、テキストがレイヤーrectに切り捨てられないようにします。 </p> <p>クリッピングが発生しない限り、指定した解像度でテキストをレンダリングする場合に使用します。 クリッピングの場合、解像度は自動的に下がり、すべてのテキストがテキストボックス内に完全に収まるようになります。 折り返しを有効にすると、最終的な解像度でテキストが再折り返される場合があります。 <span class="codeph"> textPs= </span>ではサポートされていません。 </p> </td> 
     </tr> 
    </table> </p> <p>size=を使用してテキストレイヤーサイズを指定しない場合、または幅のみを指定した場合、「autoRes」と「maxRes」の設定は無視され、指定した解像度を使用してテキストがレンダリングされます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap  </span> </span> </p> </td> 
  <td class="stentry"> <p>折り返しモードを指定します。 </p> <p> <span class="codeph"> ラップ | noWrap | nbWrap  </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap  </span> </p> </td> 
      <td class="stentry"> <p>ワードラップを無効にします。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> まとめる </span> </p> </td> 
      <td class="stentry"> <p>標準のワードラップを有効にします。 </p> <p>必要に応じて、長い単語を区切ります。 <span class="codeph"> textPs= </span> では <span class="codeph"> 折り返しのみがサポートされ </span>ます。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap  </span> </p> </td> 
      <td class="stentry"> <p>改行しないワードラップを有効にします。 </p> <p>単語の末尾が切り捨てられても、単語を区切らない。 通常、長い単語が壊れないようにするために、<span class="codeph"> autoRes </span>または<span class="codeph"> maxRes </span>と組み合わせて使用します。 </p> </td> 
     </tr> 
    </table> </p> <p><span class="codeph">は、</span>と<span class="codeph"> nbwrap </span>の両方とも、単語の境界とハイフンに対して自動的にラップします。 </p> </td> 
 </tr> 
</table>

## プロパティ {#section-114ca0b8585b403c873e2251478ad1d5}

テキストレイヤー属性。 画像、べた塗りおよびエフェクトレイヤーでは無視されます。 `layer=comp`に対して指定した場合、`layer=0`に適用されます。

## 初期設定 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 関連項目 {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) 、 [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)、 [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
