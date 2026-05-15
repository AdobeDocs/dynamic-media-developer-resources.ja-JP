---
title: textAttr
description: テキストレイヤーの属性。 rtf コマンドとして使用できないテキストレイヤーの追加属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
TQID: 'https://experienceleague.adobe.com/7md74Pcl5SuFEi6v8mdpYTAxj3bJZTykMzg7bpT8Aqo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 458
ht-degree: 0%

---

# textAttr{#textattr}

テキストレイヤーの属性。 rtf コマンドとして使用できないテキストレイヤーの追加属性を指定します。

` textAttr= *`res`*[, *` アンチエイリアス `*[, *`resMode`*[, *`wordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span> </span> </p> </td> 
  <td class="stentry"> <p>フォントサイズを変更せずにテキストレイヤーを拡大・縮小する方法を提供します。 解像度の値を大きくすると、カンバスサイズに対するレンダリングされたテキストのサイズが大きくなります。値を小さくすると、テキストサイズが小さくなります。 1 インチあたりのドット数（0より大きい整数）のテキスト解像度。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> アンチエイリアス </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストレンダリングエンジンで使用されるアンチエイリアスモードを制御します。 </p> <p> <span class="codeph"> オフ | ノーム | クリスプ | シャープ | ストロング | スムーズ </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> </span>から<span class="codeph"> </p> </td> 
      <td class="stentry"> <p>テキストアンチエイリアスを無効にします。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> ノルム </span> </p> </td> 
      <td class="stentry"> <p>標準テキストのアンチエイリアスモードを有効にします（デフォルト）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> クリスプ </span> </p> </td> 
      <td class="stentry"> <p>Photoshop アンチエイリアスモード <span class="codeph">を選択すると、鮮明な</span> （<span class="codeph"> textPs= </span>のみ）が表示されます。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> シャープ </span> </p> </td> 
      <td class="stentry"> <p>Photoshop アンチエイリアシングモード <span class="codeph"> シャープ </span>を選択します（<span class="codeph"> textPs= </span>のみ）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph">強</span> </p> </td> 
      <td class="stentry"> <p>Photoshop アンチエイリアスモード <span class="codeph">強</span>を選択します（<span class="codeph"> textPs= </span>のみ）。 </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストをレンダリングする際のresの使用方法を制御します </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>指定した解像度を使用します。 </p> <p>テキストが合成されたカンバスに対して正確なサイズでレンダリングされる場合に使用します。 テキストボックスが小さすぎると、テキストがレイヤーサイズ（指定されている場合）にクリップされる場合があります。 これは、<span class="codeph"> textPs= </span>がサポートするresMode </span> オプションの中で唯一<span class="varname">個です。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph">件の自動応答</span> </p> </td> 
      <td class="stentry"> <p>解像度を自動的に調整して、レイヤーの長方形をテキストで最適に塗りつぶします。 </p> <p>を使用すると、テキストボックスが切り捨てられるリスクなしに、可能な限り塗りつぶされるようにテキストサイズを自動的に調整できます。 ワードラップが有効になっている場合、テキストは最終的な解像度で再ラッピングされる場合があります。 <span class="codeph"> autoRes </span>が選択されている場合、<span class="varname"> res </span>は無視されます。 <span class="codeph"> textPs= </span>ではサポートされていません。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>指定した解像度を使用します。必要に応じて解像度を下げて、レイヤーの矩形にテキストが切り捨てられるのを防ぎます。 </p> <p>クリッピングが発生しない限り、を使用して指定した解像度でテキストをレンダリングします。 クリッピングがある場合は、すべてのテキストがテキストボックス内に完全に含まれるように、解像度が自動的に減少します。 ワードラップが有効になっている場合、テキストは最終的な解像度で再ラッピングされる場合があります。 <span class="codeph"> textPs= </span>ではサポートされていません。 </p> </td> 
     </tr> 
    </table> </p> <p>テキストのレイヤーサイズがsize=で指定されていない場合、または幅のみが指定されている場合、「autoRes」および「maxRes」の設定は無視されます。 このような場合、指定した解像度を使用してテキストをレンダリングします。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap </span> </span> </p> </td> 
  <td class="stentry"> <p>ラッピングモードを指定します。 </p> <p> <span class="codeph"> ラップ | noWrap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>ワードラップを無効にします。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> </span>をラップ </p> </td> 
      <td class="stentry"> <p>標準的なワードラップを有効にします。 </p> <p>必要に応じて長い単語を破ります。 <span class="codeph"> textPs= </span>は<span class="codeph">回り込み</span>のみをサポートしています。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>改行なしのワードラップを有効にします。 </p> <p>単語の最後に切り捨てられたとしても、単語を絶対に壊さないこと。 通常、<span class="codeph">個のautoRes </span>または<span class="codeph">個のmaxRes </span>で使用して、長い単語が壊れないようにします。 </p> </td> 
     </tr> 
    </table> </p> <p><span class="codeph">は単語の境界とハイフンで</span>をラップし、<span class="codeph">は</span>を自動ラップします。 </p> </td> 
 </tr> 
</table>

## プロパティ {#section-114ca0b8585b403c873e2251478ad1d5}

テキストレイヤー属性。 画像レイヤー、単色レイヤー、エフェクトレイヤーでは無視されます。 `layer=comp`に指定されている場合は、`layer=0`に適用されます。

## 初期設定 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 関連項目 {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f)、[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)、[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
