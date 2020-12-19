---
description: 画像の不透明度を調整 画像、テキスト、べた塗りまたはエフェクトレイヤーの前景の不透明度を低くできます。
seo-description: 画像の不透明度を調整 画像、テキスト、べた塗りまたはエフェクトレイヤーの前景の不透明度を低くできます。
seo-title: opac
solution: Experience Manager
title: opac
topic: Scene7 Image Serving - Image Rendering API
uuid: 268279bd-d777-4afe-b175-841af7e55406
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 2%

---


# opac{#opac}

画像の不透明度を調整 画像、テキスト、べた塗りまたはエフェクトレイヤーの前景の不透明度を低くできます。

`opac= *`opacityfillOpacity`*[, *``*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> opacity</span> </p> </td> 
  <td class="stentry"> <p>プライマリの不透明度(0 ～ 100 int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>塗りの不透明度(0 ～ 100 int) </p></td> 
 </tr> 
</table>

画像レイヤーの前景の不透明度は、レイヤーマスクまたは画像のアルファチャネルによって決まります。不透明度がない場合は100 %になります。 テキストレイヤーの前景不透明度は100%で、べた塗りレイヤーの前景不透明度は`color=`で設定します。

`opac=` 塗りつぶされた領域の不透明度は変更し `color=` ません `bgColor=` `color=`。ただし、べた塗りの領域とエフェクトレイヤー（で設定）の前景領域を除きます。

画像、テキスト、またはべた塗りのレイヤーで指定した場合、*`opacity`*&#x200B;は関連するすべてのエフェクトレイヤーを含むレイヤー全体を適用し、*`fillOpacity`*&#x200B;はプライマリレイヤーのコンテンツのみに適用します。 エフェクトレイヤーで指定した場合、*`opacity`*&#x200B;はエフェクトレイヤーに適用され、*`fillOpacity`*&#x200B;は無視されます。

メインレイヤーコンテンツの有効な不透明度は(*`opacity`* * *`fillOpacity`* / 100)です。 エフェクトレイヤーの有効な不透明度は、（メイン&#x200B;*`opacity`* *エフェクト&#x200B;*`opacity`* / 100）です。

## プロパティ {#section-ac3f136ff1584a2eab87500b7164f7fa}

レイヤー属性。 `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。

## 初期設定 {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`（レイヤーの不透明度を変更しない場合）。

## 例 {#section-9710810e96af40538652e8ae4aadd3be}

... `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`...

この例のテキストの不透明度は90*70/100=63%で、効果レイヤーの不透明度は90*50/100=45%です。

## 関連項目 {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) 、 [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
