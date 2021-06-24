---
description: カラー量子化。 GIF出力変換のカラー量子化属性を指定します。
solution: Experience Manager
title: 量子化する
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# 量子化する{#quantize}

カラー量子化。 GIF出力変換のカラー量子化属性を指定します。

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac}パレッ </span> トの種類 </p> <p>「 <span class="codeph"> web </span> 」または「 <span class="codeph"> mac </span> 」を選択して事前定義済みのパレットを選択するか、「 <span class="codeph">アダプティブ</span> 」に設定して画像に最適なパレットを計算します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> ディザ  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off}ディザリン </span> グオプション </p> <p>Floyd-Steinbergエラー拡散の場合は「拡散」を選択し、ディザリングを無効にする場合は「オフ」を選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>「 <span class="codeph">アダプティブ</span> 」パレットに含まれる出力色（整数）の数。 </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> は2 ～ 256の範囲で指定する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>強制されたRGBカラーの16進数6形式のコンマ区切りリスト。 「 <span class="codeph">アダプティブ</span> 」パレットに含める強制カラーを指定できます。 指定した色数が<span class="codeph"> numColors </span>未満の場合、画像の内容に基づいて追加の色が計算されます。 </p> <p><span class="codeph"> fmt=gif </span>または<span class="codeph"> fmt=gif-alpha </span>の場合にのみ使用されます。 それ以外の場合は無視されます。 <span class="codeph"> <span class="varname"> colorList </span> </span>で指定する色は、16進数6形式のRGB値にする必要があります（<span class="codeph"> color </span>を参照）。他の色指定子は使用できません。 </p> </td> 
 </tr> 
</table>

## 初期設定 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 例 {#section-b3a979dc9ae3459baa093bf17310988f}

「`web`」パレットを使用し、ディザリングを使用せずにGIFサムネールを生成します。

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

キーカラーの透明度とカラーを白黒に強制的に設定して、画像をバイトナルGIFに変換します。

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
