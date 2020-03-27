---
description: 色の量子化 GIF出力変換のカラー量子化属性を指定します。
seo-description: 色の量子化 GIF出力変換のカラー量子化属性を指定します。
seo-title: 量子化する
solution: Experience Manager
title: 量子化する
topic: Scene7 Image Serving - Image Rendering API
uuid: 4e9c4807-59bc-4eb9-bcab-0bf0cfdf56d4
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# 量子化する{#quantize}

色の量子化 GIF出力変換のカラー量子化属性を指定します。

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>パレットの種類を指定します。 </p> <p>画像の最適な <span class="codeph"> パレ </span> ットを計算するには、adaptiveに設定します。 </p> <p>Webまたは <span class="codeph"> Macに設 </span> 定して、 <span class="codeph"> 事前定義さ </span> れたパレットを選択します。 </p> <p> <p>注意： MACパレ <span class="codeph"> ット </span> タイプは、GIFおよびPNG8形式でのみサポートされますが、GIF-AlphaおよびPNG8-Alpha形式ではサポートされません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ディザ </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off} </span> </p> <p>ディザのオプションを指定します。 </p> <p>Floyd-Steinberg誤差 <span class="codeph"> 拡散 </span> の拡散に対して拡散に設定 </p> <p>ディザを無効に <span class="codeph"> するに </span> は、offに設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span></span> </p> </td> 
   <td colname="col2"> <p>出力色の数(2 ～ 256) </p> <p>アダプティブパレットに含める色の数を指 <span class="codeph"> 定し </span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span></span> </p> </td> 
   <td colname="col2"> <p>強制RGBカラーを16進数6形式でコンマ区切りしたリスト </p> <p>アダプティブパレットに含める色を指 <span class="codeph"> 定で </span> きます。 指定した色の数が <span class="codeph"> numColorsより少ない場合、画 <span class="varname"></span></span>像の内容に基づいて追加の色が計算されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8ab5035055b24b858270d260912a7f3d}

リクエスト属性。 現在のレイヤー設定に関係なく適用されます。 、、、またはの場 `fmt=gif`合にの `fmt=gif-alpha`み使 `fmt=png8`用されま `fmt=png8-alpha`す。 それ以外の場合は無視されます。

colorListで指定する色は、 ` *`RGB値(`*` 16進数 ` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`6形式)で構成され、「 `0x`」プレフィックスは付きません。 他の色指定子は使用できません。 *`numColors`* は2 ～ 256の範囲で設定する必要があります。

## 初期設定 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 例 {#section-e34aca7587d548a7ae9d4266b80c9451}

パレットを使用し、ディザなしでGIF `web` サムネールを生成します。

` http:// *`server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

画像をキーカラーの透明部分を持つバイトナルGIFに変換し、カラーを白黒に強制的に変換します。

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 関連項目 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
