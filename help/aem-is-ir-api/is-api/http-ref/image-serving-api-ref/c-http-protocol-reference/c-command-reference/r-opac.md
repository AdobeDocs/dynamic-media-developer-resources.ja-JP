---
description: 画像の不透明度を調整します。 画像、テキスト、べた塗りまたはエフェクトレイヤーの前景の不透明度を下げます。
seo-description: 画像の不透明度を調整します。 画像、テキスト、べた塗りまたはエフェクトレイヤーの前景の不透明度を下げます。
seo-title: opac
solution: Experience Manager
title: opac
topic: Scene7 Image Serving - Image Rendering API
uuid: 268279bd-d777-4afe-b175-841af7e55406
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# opac{#opac}

画像の不透明度を調整します。 画像、テキスト、べた塗りまたはエフェクトレイヤーの前景の不透明度を下げます。

`opac= *`opacityfillOpacity`*[, *``*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 不透明度</span> </p> </td> 
  <td class="stentry"> <p>プライマリ不透明度(0 ～ 100 int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>塗りの不透明度（0 ～ 100整数） </p></td> 
 </tr> 
</table>

イメージレイヤの前景の不透明度は、イメージのレイヤマスクまたはアルファチャンネルによって決まります。どちらも存在しない場合は100 %です。 テキストレイヤーの前景の不透明度は100 %で、べた塗りレイヤーの不透明度はによって設定されま `color=`す。

`opac=` 塗りつぶされた領域の不透明度や、塗りつぶされた領域の不透 `color=` 明度を変更しな `bgColor=`いでください。ただし、べた塗りとエフェクトレイヤー（で設定）の前景領域は変更し `color=`ません。

画像、テキストまたはべた塗りのレイヤーで指定した場合、は関連するすべてのエフェクトレイヤーを含むレイヤー全体を適用し、 *`opacity`* 一方、プライマリレイヤーの *`fillOpacity`* コンテンツにのみ適用します。 エフェクトレイヤーで指定した場合、はエフ *`opacity`* ェクトレイヤーに適用され、は無視 *`fillOpacity`* されます。

メインレイヤーのコンテンツの有効な不透 *`opacity`* 明度は( *`fillOpacity`* * / 100)です。 エフェクトレイヤーの有効な不透明度は(メ *`opacity`* イン*エ *`opacity`* フェクト/ 100)です。

## プロパティ {#section-ac3f136ff1584a2eab87500b7164f7fa}

レイヤー属性。 現在のレイヤーまたは合成画像（の場合）に適用されま `layer=comp`す。

## 初期設定 {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`を指定します。レイヤーの不透明度は変更されません。

## 例 {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

この例のテキストの不透明度は90*70/100=63%で、効果レイヤーの不透明度は90*50/100=45%です。

## 関連項目 {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
