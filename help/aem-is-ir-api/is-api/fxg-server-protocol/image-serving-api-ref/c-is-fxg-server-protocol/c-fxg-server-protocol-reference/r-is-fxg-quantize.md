---
title: 量子化
description: カラー量子化。 GIF出力変換のカラー量子化属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# 量子化{#quantize}

カラー量子化。 GIF出力変換のカラー量子化属性を指定します。

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> パレットタイプ </p> <p>「<span class="codeph"> web </span>」または「<span class="codeph"> mac </span>」を選択して事前定義済みのパレットを選択するか、「<span class="codeph"> adaptive </span>」に設定して画像に最適なパレットを計算します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dither </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> ディザリングオプション </p> <p>Floyd-Steinberg 誤差拡散に「diffuse」を選択するか、ディザリングを無効にする「off」を選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>「<span class="codeph"> アダプティブフ </span> ーム」パレットに含まれる出力色の数（整数）。 </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> は 2 ～ 256 の値にする必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>16 進数形式の強制RGB カラーのコンマ区切りリスト。 「<span class="codeph"> アダプティブフ </span> ーム」パレットに含める強制的な色を指定できます。 指定された色の数が numColors<span class="codeph"> より少ない場合 </span>、追加の色が画像の内容に基づいて計算されます。 </p> <p>fmt=gif <span class="codeph"> または </span>=gif-alpha <span class="codeph"> の場合 </span> のみ使用されます。 それ以外の場合は無視されます。 <span class="codeph"> <span class="varname"> colorList </span> </span> で指定するカラーは、hex6 フォーマットのRGB値である必要があります（<span class="codeph"> color </span> を参照）。他のカラー指定子は使用できません。 </p> </td> 
 </tr> 
</table>

## 初期設定 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 例 {#section-b3a979dc9ae3459baa093bf17310988f}

「`web`」パレットを使用し、ディザリングを行わずにGIF サムネールを生成します。

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

キーカラーの透明度とカラーを白黒に強制するバイトーンのGIFに画像を変換します。

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
