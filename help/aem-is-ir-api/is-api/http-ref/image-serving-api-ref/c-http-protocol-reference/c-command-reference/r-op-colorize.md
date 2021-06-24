---
description: 画像のカラー化 シャドウとハイライトを維持しながら、イメージデータをカラー化します。
solution: Experience Manager
title: op_colorize
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 4%

---

# op_colorize{#op-colorize}

画像のカラー化 シャドウとハイライトを維持しながら、イメージデータをカラー化します。

` op_colorize= *``*[,off|norm[, *`colorcontrast`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>置き換えるRGBカラー。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> オフ </span> </p> </td> 
  <td class="stentry"> <p>明るさの自動補正を無効にします。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norm  </span> </p> </td> 
  <td class="stentry"> <p>明るさの自動補正を有効にします（デフォルト）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 比較対照 </span> </p> </td> 
  <td class="stentry"> <p>コントラスト範囲（実数0 ～ 100）0に設定すると、入力コントラストが保持されます。 </p> </td> 
 </tr> 
</table>

2番目の引数は、色付けの前にソース画像の明るさを調整するかどうかを指定します。 明るさの自動補正を無効にする場合は`off`を指定し、中央値が50%になるように明るさを自動的に調整する場合は`norm`を指定します。

*`contrast`*&#x200B;の値を0に設定して、入力画像のコントラスト範囲を保持するか、0より大きい値で目的のコントラスト範囲を指定します。 値を 100 に設定すると、コントラストが最大になります。一般的な値は30 ～ 70です。

組み込みの明るさとコントラストの調整に加えて、`op_brightness=`と`op_contrast=`を使用して色付け効果をさらに微調整できます。

>[!NOTE]
>
>色付けアルゴリズムは、画像データの輝度情報のみを用いる。 このグレースケールへの変換は簡単で、カラー管理はおこなわれません。 `op_colorize` 入力がグレースケールまたはCMYKの場合でも、常にRGBデータを出力します。

## プロパティ {#section-c0f8bd424b864153a1108f384939f55b}

レイヤコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤでは無視されます。

*`color`* はRGB値である必要があります。グレーまたはCMYK *`color`* の値はサポートされていません。

明るさの補正がオフの場合、*`contrast`*&#x200B;値は無視されます。

*`color`* は、のピクセルタイプに対応する作業用カラースペースに存在すると見なされま *`color`*&#x200B;す。*`color`* は、マージ時にレイヤー画像のピクセルタイプが異なる場合、正確に変換されます。

CMYK画像は、操作が適用される前にRGBに変換されます。

## 初期設定 {#section-0c3ea13efbac432c8970862d223e39b3}

`None`（色付けなし）。2つ目と3つ目の引数は、明るさの自動補正を行い、コントラストの変化を伴わないため、デフォルトで`norm,0`に設定されます。

## 例 {#section-4c418d7b5e97409d9a448b8f08a1eab3}

画像レイヤーに色を付ける前に、明るさとコントラストを動的に調整します。

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

代わりに、自動明るさとコントラストの調整を使用します。

... `&op_colorize=a0b0c0,norm,50&`...

## 関連項目 {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)、  [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a)、  [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d)、カラ [ーマネジメント](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
