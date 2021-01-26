---
description: 画像のカラー化 シャドウとハイライトを維持しながら、画像データに色を付けます。
seo-description: 画像のカラー化 シャドウとハイライトを維持しながら、画像データに色を付けます。
seo-title: op_colorize
solution: Experience Manager
title: op_colorize
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e74a85ca-73bf-4c69-ac77-768a58b33d0b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 4%

---


# op_colorize{#op-colorize}

画像のカラー化 シャドウとハイライトを維持しながら、画像データに色を付けます。

` op_colorize= *``*[,off|norm[, *`色対比`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>置換後のRGBカラー </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> オフ </span> </p> </td> 
  <td class="stentry"> <p>明るさの自動補正を無効にします。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norm  </span> </p> </td> 
  <td class="stentry"> <p>明るさの自動補正を有効にする（デフォルト） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 比較対照 </span> </p> </td> 
  <td class="stentry"> <p>コントラストの範囲（実数0 ～ 100）;0に設定すると、入力コントラストが保持されます。 </p> </td> 
 </tr> 
</table>

2番目の引数は、色付きを適用する前にソース画像の明るさを調整するかどうかを指定します。 明るさの自動補正を無効にするには`off`を指定し、中央値が50 %の強度になるように明るさを自動的に調整するには`norm`を指定します。

*`contrast`*&#x200B;値を0に設定して、入力画像のコントラスト範囲を維持するか、0より大きい値を指定して、目的のコントラスト範囲を指定します。 値を 100 に設定すると、コントラストが最大になります。一般的な値は、30 ～ 70の範囲です。

組み込みの明るさとコントラストの調整に加えて、`op_brightness=`と`op_contrast=`を使用して、色彩の効果をさらに微調整することができます。

>[!NOTE]
>
>色彩付けアルゴリズムは、画像データの輝度情報のみを用いる。 このグレースケールへの変換は単純で、カラーマネジメントは行われません。 `op_colorize` 常にRGBデータを出力します。入力データがグレースケールまたはCMYKであっても同様です。

## プロパティ {#section-c0f8bd424b864153a1108f384939f55b}

レイヤーコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤーでは無視されます。

*`color`* はRGB値である必要があります。グレーまたはCMYK *`color`* の値はサポートされていません。

明るさの補正がオフの場合、*`contrast`*&#x200B;値は無視されます。

*`color`* は、のピクセルタイプに対応する作業カラースペースに存在すると見なされ *`color`*&#x200B;ます。*`color`* は、結合時にレイヤー画像のピクセルタイプが異なる場合、正確に変換されます。

CMYK画像は、操作の適用前にRGBに変換されます。

## 初期設定 {#section-0c3ea13efbac432c8970862d223e39b3}

`None`を使用します。2番目と3番目の引数は、自動輝度補正とコントラストの変更を行わないため、デフォルトで`norm,0`に設定されます。

## 例 {#section-4c418d7b5e97409d9a448b8f08a1eab3}

画像レイヤーに色を付ける前に、明るさとコントラストを動的に調整します。

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

代わりに、自動明るさとコントラスト調整を使用します。

... `&op_colorize=a0b0c0,norm,50&`...

## 関連項目 {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a),  [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d),  [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
