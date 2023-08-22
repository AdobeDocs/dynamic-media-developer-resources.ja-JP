---
title: op_colorize
description: 画像の色彩の統一。 シャドウとハイライトを保持しながら、イメージデータに色を付けます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 4%

---

# op_colorize{#op-colorize}

画像の色彩の統一。 シャドウとハイライトを保持しながら、イメージデータに色を付けます。

` op_colorize= *`カラー`*[,off|norm[, *`対照`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>置換RGBの色。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> オフ </span> </p> </td> 
  <td class="stentry"> <p>明るさの自動補正を無効にします。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norm </span> </p> </td> 
  <td class="stentry"> <p>明るさの自動補正を有効にします（デフォルト）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 比較対照 </span> </p> </td> 
  <td class="stentry"> <p>コントラスト範囲（実数 0 ～ 100）。入力コントラストを保持するには、0 に設定します。 </p> </td> 
 </tr> 
</table>

2 番目の引数は、色付けする前にソース画像の明るさを調整するかどうかを指定します。 指定 `off` 自動明るさ補正を無効にするか、 `norm` 中央値が 50 %の強度になるように明るさを自動的に調整するには

を設定します。 *`contrast`* 値を 0 に設定すると、入力画像のコントラスト範囲が保持されます。または、0 より大きい値を持つ目的のコントラスト範囲を指定します。 値を 100 に設定すると、コントラストが最大になります。一般的な値は 30 ～ 70 です。

組み込みの明るさとコントラストの調整に加えて、 `op_brightness=` および `op_contrast=` は、色彩の影響をさらに微調整するために使用できます。

>[!NOTE]
>
>色彩化アルゴリズムは、画像データの輝度情報のみを用いる。 このグレースケールへの変換は簡単で、カラーマネジメントはおこなわれません。 `op_colorize` 入力がグレースケールまたは CMYK の場合でも、常にRGBデータを出力します。

## プロパティ {#section-c0f8bd424b864153a1108f384939f55b}

[ 画層 ] コマンド 現在の画層または合成画像に適用されます ( `layer=comp`. 効果画層で無視されます。

*`color`* は、RGB値（グレーまたは CMYK）である必要があります *`color`* の値はサポートされていません。

The *`contrast`* 明るさの補正がオフの場合、値は無視されます。

*`color`* は、 *`color`*. *`color`* 結合時にレイヤー画像のピクセルタイプが異なる場合、は正確に変換されます。

CMYK 画像は、操作が適用される前にRGBに変換されます。

## 初期設定 {#section-0c3ea13efbac432c8970862d223e39b3}

`None`（カラー化なし）。 2 番目と 3 番目の引数のデフォルト値はです。 `norm,0`（明るさの自動補正とコントラストの変更なし）。

## 例 {#section-4c418d7b5e97409d9a448b8f08a1eab3}

画像レイヤーに色を付ける前に、明るさとコントラストを動的に調整します。

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

代わりに、自動明るさとコントラストの調整を使用します。

… `&op_colorize=a0b0c0,norm,50&`…

## 関連項目 {#section-5581eb0e03014fa795e8f078c60e6c8d}

[カラー](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [カラーマネジメント](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
