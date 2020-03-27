---
description: 色の量子化 GIF出力変換のカラー量子化属性を指定します。
seo-description: 色の量子化 GIF出力変換のカラー量子化属性を指定します。
seo-title: 量子化する
solution: Experience Manager
title: 量子化する
topic: Scene7 Image Serving - Image Rendering API
uuid: 624cdc45-51f2-4b18-a658-311770974521
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 量子化する{#quantize}

色の量子化 GIF出力変換のカラー量子化属性を指定します。

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac}パレッ </span> トタイプ </p> <p>「Web」または「 <span class="codeph"> mac」を選択して、事前定義されたパレッ </span>トを選択するか、「アダプティブ」に設定して、画 <span class="codeph"> 像の最適なパ </span><span class="codeph"></span>レットを計算します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> ディザ </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off}ディザオプシ </span> ョン </p> <p>フロイド — スタインバーグ誤差拡散の場合は「拡散」を、ディザを無効にする場合は「オフ」を選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span></span> </p> </td> 
  <td class="stentry"> <p>「アダプティブ」パレットに含まれる出力 <span class="codeph"> 色(整 </span>数)の数。 </p> <p> <span class="codeph"> numColorsは <span class="varname"> 2 ～ 256の </span></span> 範囲で設定する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span></span> </p> </td> 
  <td class="stentry"> <p>強制RGBカラーを16進数6形式で表したコンマ区切りリストです。 「アダプティブ」パレットに含める強制カラーを指 <span class="codeph"> 定で </span>きます。 指定したカラー数がnumColorsより少ない場合、 <span class="codeph"> 画像 </span>の内容に基づいて追加のカラーが計算されます。 </p> <p>fmt=gifまたは <span class="codeph"> fmt=gif-alpha </span> の <span class="codeph"> 場合にのみ使用されます </span>。 それ以外の場合は無視されます。 colorListで指定する色は、16進数6形 <span class="codeph"> 式 <span class="varname"> のRGB </span> 値である必要があります(colorを </span><span class="codeph"></span>参照)。他の色指定子は使用できません。 </p> </td> 
 </tr> 
</table>

## 初期設定 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 例 {#section-b3a979dc9ae3459baa093bf17310988f}

「」パレットを使用し、ディザなしでGIF `web`サムネールを生成します。

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

画像をキーカラーの透明部分を持つバイトナルGIFに変換し、カラーを白黒に強制的に変換します。

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
