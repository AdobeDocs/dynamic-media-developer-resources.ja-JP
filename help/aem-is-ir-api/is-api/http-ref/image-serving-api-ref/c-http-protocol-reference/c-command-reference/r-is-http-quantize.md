---
title: 量子化する
description: 色量子化。 GIF出力変換のカラー量子化属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 3%

---

# 量子化する{#quantize}

色量子化。 GIF出力変換のカラー量子化属性を指定します。

` quantize= *`type`*[, *`ディザ`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>パレットの種類を指定します。 </p> <p>に設定 <span class="codeph"> アダプティブ </span> 画像に最適なパレットを計算する。 </p> <p>に設定 <span class="codeph"> web </span> または <span class="codeph"> mac </span> をクリックして、事前定義済みのパレットを選択します。 </p> <p> <p>注意：この <span class="codeph"> mac </span> パレットタイプは、GIFおよび PNG8 形式に対してのみサポートされますが、GIF — アルファおよび PNG8-Alpha 形式にはサポートされません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ディザ </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off} </span> </p> <p>ディザリングオプションを指定します。 </p> <p>に設定 <span class="codeph"> 拡散 </span> フロイド — スタインベルク誤差拡散用 </p> <p>に設定 <span class="codeph"> オフ </span> ディザリングを無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>出力色数 (2-256) </p> <p>に含まれる色の数を指定します <span class="codeph"> アダプティブ </span> パレット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>16 進数 6 形式の強制RGBの色のコンマ区切りリスト </p> <p>次に含める色を指定します： <span class="codeph"> アダプティブ </span> パレット。 指定した色数が <span class="codeph"> <span class="varname"> numColors </span> </span>の場合、画像の内容に基づいて追加の色が計算されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8ab5035055b24b858270d260912a7f3d}

要求属性。 現在の画層設定に関係なく適用されます。 次の場合にのみ使用されます。 `fmt=gif`, `fmt=gif-alpha`, `fmt=png8`または `fmt=png8-alpha`. それ以外は無視されます。

で指定された色 *`colorList`* は、16 進数 6 形式のRGB値で構成する必要があります ( [カラー](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) なし `0x` プレフィックス 他の色指定子は使用できません。 *`numColors`* は 2 ～ 256 の範囲で設定する必要があります。

## 初期設定 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 例 {#section-e34aca7587d548a7ae9d4266b80c9451}

を使用してGIFサムネールを生成 `web` パレットとディザリングなし：

` http:// *`server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

画像をキーカラー透明度でバイトーンGIFに変換し、カラーを白黒に強制的に変換します。

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 関連項目 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [カラー](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
