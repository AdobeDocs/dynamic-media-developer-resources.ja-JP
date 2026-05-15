---
title: 量子化
description: カラーの量子化： GIF出力変換のカラー量子化属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
TQID: 'https://experienceleague.adobe.com/m5e14tLMY1JAdZTzlw7iUZzXzL9yylP66MYi5XAeYtg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# 量子化{#quantize}

カラーの量子化： GIF出力変換のカラー量子化属性を指定します。

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> タイプ </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> パレット タイプ </p> <p>「<span class="codeph"> web </span>」または「<span class="codeph"> mac </span>」を選択して定義済みのパレットを選択するか、「<span class="codeph"> アダプティブ </span>」に設定して画像に最適なパレットを計算します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> ディザ </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> ディザリングオプション </p> <p>Floyd-Steinbergのエラー拡散に「diffuse」を選択するか、ディザリングを無効にするには「off」を選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>'<span class="codeph"> アダプティブ </span>' パレットに含まれる出力カラー（整数）の数。 </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span>は2 ～ 256である必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>16進数6形式の強制RGB カラーのコンマ区切りリスト。 「<span class="codeph">」アダプティブ </span> パレットに含める強制カラーを指定できます。 指定されたカラー数が<span class="codeph"> numColors </span>未満の場合、追加のカラーは画像コンテンツに基づいて計算されます。 </p> <p><span class="codeph"> fmt=gif </span>または<span class="codeph"> fmt=gif-alpha </span>の場合にのみ使用されます。 それ以外は無視されます。 <span class="codeph"> <span class="varname"> colorList </span> </span>で指定されたカラーは、16進数6のRGB値である必要があります（<span class="codeph"> color </span>を参照）。他のカラー指定子は使用できません。 </p> </td> 
 </tr> 
</table>

## 初期設定 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 例 {#section-b3a979dc9ae3459baa093bf17310988f}

「`web`」パレットを使用してGIF サムネールを生成し、ディザ処理を行いません。

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

画像をキーカラーの透明度とフォース色を白黒に変換したバイトーンのGIFに変換します。

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
