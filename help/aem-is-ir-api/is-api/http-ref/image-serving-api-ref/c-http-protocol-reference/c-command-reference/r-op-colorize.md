---
title: op_colorize
description: 画像を色付けします。 シャドウとハイライトを保持しながら、画像データを色付けします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 3%

---

# op_colorize{#op-colorize}

画像を色付けします。 シャドウとハイライトを保持しながら、画像データを色付けします。

` op_colorize= *`color`*[,off|norm[, *`contrast`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>置き換えるRGBの色。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> off </span> </p> </td> 
  <td class="stentry"> <p>自動輝度補正を無効にします。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 標準 </span> </p> </td> 
  <td class="stentry"> <p>自動輝度補正を有効にします（デフォルト）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> contrast </span> </p> </td> 
  <td class="stentry"> <p>コントラスト範囲（実際の 0～100）。入力コントラストを保持するには 0 に設定します。 </p> </td> 
 </tr> 
</table>

2 番目の引数は、カラーを適用する前にソース画像の明るさを調整する必要があるかどうかを指定します。 自動輝度補正を無効にするには `off` を指定し、中央値の輝度が 50% になるように自動的に輝度を調整するには `norm` を指定します。

*`contrast`* 値を 0 に設定して入力画像のコントラスト範囲を保持するか、0 より大きい値を使用して目的のコントラスト範囲を指定します。 値を 100 に設定すると、コントラストが最大になります。一般的な値は 30 ～ 70 です。

内蔵の明るさやコントラストの調整に加えて、`op_brightness=` や `op_contrast=` を使用して着色効果をさらに微調整することもできます。

>[!NOTE]
>
>前記色付けアルゴリズムは、前記画像データの輝度情報のみを用いる。 グレースケールへの変換はシンプルで、カラーマネジメントは行われません。 入力 `op_colorize` グレースケールまたは CMYK の場合でも、常にRGBデータを出力します。

## プロパティ {#section-c0f8bd424b864153a1108f384939f55b}

[ 画層 ] コマンド： 現在のレイヤーまたは合成イメージ（`layer=comp` の場合）に適用されます。 エフェクトレイヤーで無視されます。

*`color`* はRGB値である必要があります。グレーまたは CMYK *`color`* 値はサポートされていません。

明るさの補正がオフの場合、*`contrast`* の値は無視されます。

*`color`* は、*`color`* のピクセルタイプに対応する作業用カラースペースに存在すると想定されます。 レイヤー画像のピクセルの種類がマージ時に異なる場合、*`color`* は正確に変換されます。

CMYK 画像はRGBに変換されてから処理が行われます。

## 初期設定 {#section-0c3ea13efbac432c8970862d223e39b3}

`None` （色付けなし）。 2 番目と 3 番目の引数はデフォルトで `norm,0` で、自動的な明るさの補正が行われ、コントラストは変更されません。

## 例 {#section-4c418d7b5e97409d9a448b8f08a1eab3}

画像レイヤーを色付けする前に、明るさとコントラストを動的に調整します。

...`&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

代わりに、自動的な明るさとコントラストの調整を使用します。

...`&op_colorize=a0b0c0,norm,50&`...

## 関連項目 {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [ カラーマネジメント ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
