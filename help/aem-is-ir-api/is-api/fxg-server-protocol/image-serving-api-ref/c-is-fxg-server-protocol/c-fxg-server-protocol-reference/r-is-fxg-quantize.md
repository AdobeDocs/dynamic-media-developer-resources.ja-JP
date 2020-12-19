---
description: 色量子化。 GIF出力変換のカラー量子化属性を指定します。
seo-description: 色量子化。 GIF出力変換のカラー量子化属性を指定します。
seo-title: 量子化する
solution: Experience Manager
title: 量子化する
topic: Scene7 Image Serving - Image Rendering API
uuid: 624cdc45-51f2-4b18-a658-311770974521
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# 量子化{#quantize}

色量子化。 GIF出力変換のカラー量子化属性を指定します。

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> パレットの種類 </p> <p>「<span class="codeph"> web </span>」または「<span class="codeph"> mac </span>」を選択して定義済みのパレットを選択するか、「<span class="codeph">アダプティブ</span>」に設定して画像の最適なパレットを計算します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> ディザ  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> ディザオプション </p> <p>フロイド — ステインバーグ誤差拡散の場合は「拡散」を、ディザリングを無効にする場合は「オフ」を選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>' <span class="codeph">アダプティブ</span>'パレットに含まれる出力色（整数）の数です。 </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> は2 ～ 256の範囲で設定する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>強制のRGBカラーを16進数6形式でコンマ区切りリストします。 「<span class="codeph">アダプティブ</span>」パレットに含める強制の色を指定できます。 指定したカラー数が<span class="codeph"> numColors </span>より少ない場合、画像の内容に基づいて追加のカラーが計算されます。 </p> <p><span class="codeph"> fmt=gif </span>または<span class="codeph"> fmt=gif-alpha </span>の場合にのみ使用されます。 それ以外の場合は無視されます。 <span class="codeph"> <span class="varname"> colorList </span> </span>で指定する色は、16進数6形式のRGB値でなければなりません（<span class="codeph"> color </span>を参照）。その他の色指定子は使用できません。 </p> </td> 
 </tr> 
</table>

## 初期設定 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 例 {#section-b3a979dc9ae3459baa093bf17310988f}

「`web`」パレットを使用し、ディザリングなしでGIFサムネールを生成します。

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

キーカラーの透明部分を持つバイトナルGIFに画像を変換し、カラーを白黒に強制的に変換します。

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
