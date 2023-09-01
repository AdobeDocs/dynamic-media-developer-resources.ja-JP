---
title: 量子化する
description: 色量子化。 GIF出力変換のカラー量子化属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---

# 量子化する{#quantize}

色量子化。 GIF出力変換のカラー量子化属性を指定します。

` quantize= *`type`*[, *`ディザ`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> パレットの種類 </p> <p>「 」を選択 <span class="codeph"> web </span>'または' <span class="codeph"> mac </span>'をクリックして定義済みのパレットを選択するか、' <span class="codeph"> アダプティブ </span>'を使用して、画像に最適なパレットを計算します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> ディザ </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> ディザリングオプション </p> <p>Floyd-Steinberg エラー拡散の場合は「拡散」を選択し、ディザリングを無効にする場合は「オフ」を選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>「 」に含まれる出力色（整数）の数 <span class="codeph"> アダプティブ </span>'パレット。 </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> は、2 ～ 256 の範囲で設定する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>強制RGBの色を 16 進数 6 形式でコンマ区切りで表示します。 強制的に「 」に含める色を指定できます <span class="codeph"> アダプティブ </span>'パレット。 指定した色の数が <span class="codeph"> numColors </span>の場合、画像の内容に基づいて追加の色が計算されます。 </p> <p>次の場合にのみ使用されます。 <span class="codeph"> fmt=gif </span> または <span class="codeph"> fmt=gif-alpha </span>. それ以外は無視されます。 で指定された色 <span class="codeph"> <span class="varname"> colorList </span> </span> は、16 進数 6 形式のRGB値である必要があります ( <span class="codeph"> カラー </span>) の代わりに使用する必要があります。他のカラー指定子は使用できません。 </p> </td> 
 </tr> 
</table>

## 初期設定 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 例 {#section-b3a979dc9ae3459baa093bf17310988f}

「 」を使用してGIFのサムネールを生成します `web`&#39;パレットとディザリングなし：

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

画像をキーカラー透明度とカラーを白黒に強制的に変換するバイトーンGIFに変換します。

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
