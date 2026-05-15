---
title: op_colorize
description: 画像を色付け： シャドウとハイライトを保持しながら、画像データを色付けします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
TQID: 'https://experienceleague.adobe.com/vvDUoUKtzbNV64wfOq3gzJ1KnDb49-kDYUzDwF5A4Q0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 315
ht-degree: 3%

---

# op_colorize{#op-colorize}

画像を色付け： シャドウとハイライトを保持しながら、画像データを色付けします。

` op_colorize= *` カラー`*[,off|norm[, *` コントラスト `*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> カラー</span> </p> </td> 
  <td class="stentry"> <p>RGB カラーの置き換え。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span>から<span class="codeph"> </p> </td> 
  <td class="stentry"> <p>自動輝度補正を無効にします。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ノルム </span> </p> </td> 
  <td class="stentry"> <p>自動輝度補正を有効にします（デフォルト）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> コントラスト </span> </p> </td> 
  <td class="stentry"> <p>コントラスト範囲（実数0..100）。入力コントラストを維持するには0に設定します。 </p> </td> 
 </tr> 
</table>

2番目の引数は、カラーを適用する前にソース画像の明るさを調整するかどうかを指定します。 自動輝度補正を無効にするには`off`を指定し、中央値が50%の強度になるように自動的に輝度を調整するには`norm`を指定します。

入力画像のコントラスト範囲を保持するには、*`contrast`*&#x200B;値を0に設定するか、0より大きい値で目的のコントラスト範囲を指定します。 値を 100 に設定すると、コントラストが最大になります。 一般的な値は30 ～ 70です。

組み込みの明るさとコントラストの調整に加えて、`op_brightness=`と`op_contrast=`を使用して、着色効果をさらに微調整することもできます。

>[!NOTE]
>
>色付けアルゴリズムは、画像データ内の輝度情報のみを使用します。 このグレースケールへの変換はシンプルで、カラーマネジメントは行われません。 入力がグレースケールまたはCMYKの場合でも、`op_colorize`は常にRGB データを出力します。

## プロパティ {#section-c0f8bd424b864153a1108f384939f55b}

Layer コマンド。 現在のレイヤーまたは`layer=comp`の場合はコンポジット画像に適用されます。 エフェクトレイヤーでは無視されます。

*`color`*&#x200B;はRGB値である必要があります。グレーまたはCMYK *`color`*&#x200B;値はサポートされていません。

輝度補正がオフになっている場合、*`contrast`*&#x200B;値は無視されます。

*`color`*&#x200B;は、*`color`*&#x200B;のピクセルタイプに対応する作業用カラースペースに存在すると想定されます。 レイヤー画像が結合時に異なるピクセルタイプを持つ場合、*`color`*&#x200B;は正確に変換されます。

CMYK画像は、操作が適用される前にRGBに変換されます。

## 初期設定 {#section-0c3ea13efbac432c8970862d223e39b3}

`None`、色付けなし。 2番目と3番目の引数は、自動輝度補正とコントラストの変更がないために、デフォルトで`norm,0`に設定されています。

## 例 {#section-4c418d7b5e97409d9a448b8f08a1eab3}

画像レイヤーに色を付ける前に、明るさとコントラストを動的に調整します。

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

代わりに自動明るさとコントラスト調整を使用：

... `&op_colorize=a0b0c0,norm,50&`...

## 関連項目 {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)、[op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a)、[op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d)、[&#x200B; カラーマネジメント &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
