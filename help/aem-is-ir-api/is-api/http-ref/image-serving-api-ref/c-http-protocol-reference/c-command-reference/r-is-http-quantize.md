---
title: 量子化
description: カラー量子化。 GIFの出力変換に使用するカラー量子化属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# 量子化{#quantize}

カラー量子化。 GIFの出力変換に使用するカラー量子化属性を指定します。

` quantize= *`タイプ`*[, *`ディザ`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> タイプ </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>パレットの種類を指定します。 </p> <p>をに設定 <span class="codeph"> 適応 </span> 画像に最適なパレットを計算する。 </p> <p>をに設定 <span class="codeph"> web </span> または <span class="codeph"> mac </span> 事前定義済みのパレットを選択します。 </p> <p> <p>メモ： <span class="codeph"> mac </span> パレットタイプは、GIF形式と PNG8 形式でのみサポートされ、GIFAlpha形式と PNG8Alpha形式ではサポートされていません。</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ディザ </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off} </span> </p> <p>ディザリングオプションを指定します。 </p> <p>をに設定 <span class="codeph"> びまん </span> フロイド – シュタインバーグ誤差拡散の場合 </p> <p>をに設定 <span class="codeph"> オフ </span> ディザリングを無効にします。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>出力色数（2～256） </p> <p>に含める色の数を指定します <span class="codeph"> 適応 </span> パレット。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>16 進数 6 形式の強制RGBカラーのコンマ区切りリスト </p> <p>に含めるカラーを指定できます <span class="codeph"> 適応 </span> パレット。 指定した色の数が未満の場合 <span class="codeph"> <span class="varname"> numColors </span> </span>を指定すると、画像の内容に基づいて追加の色が計算されます。</p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8ab5035055b24b858270d260912a7f3d}

リクエスト属性。 現在のレイヤ設定に関係なく適用されます。 次の場合にのみ使用されます `fmt=gif`, `fmt=gif-alpha`, `fmt=png8`、または `fmt=png8-alpha`. それ以外の場合は無視されます。

で指定された色 *`colorList`* 16 進数形式のRGB値で構成する必要があります（ [色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) なし `0x` プレフィックス。 他の色指定子は使用できません。 修飾子 *`numColors`* 2～256 にする必要があります。

## 初期設定 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 例 {#section-e34aca7587d548a7ae9d4266b80c9451}

を使用したGIFサムネールの生成 `web` パレットとディザリングなし：

`http:// *`*サーバー*`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

キーカラーの透明度を持つ双色調のGIFに画像を変換します。 また、カラーを白黒に強制します。

`http:// *`*サーバー*`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 関連項目 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
