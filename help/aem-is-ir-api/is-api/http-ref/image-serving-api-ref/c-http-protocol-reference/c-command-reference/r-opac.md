---
description: 画像の不透明度を調整 画像、テキスト、べた塗り、効果レイヤーの前景の不透明度を下げます。
solution: Experience Manager
title: opac
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---

# opac{#opac}

画像の不透明度を調整 画像、テキスト、べた塗り、効果レイヤーの前景の不透明度を下げます。

`opac= *``*[, *`opacityfillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 不透明</span> </p> </td> 
  <td class="stentry"> <p>プライマリの不透明度(0 ～ 100 int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>塗りの不透明度(0 ～ 100 int)。 </p></td> 
 </tr> 
</table>

イメージレイヤの前景の不透明度は、イメージのレイヤーマスクまたはアルファチャンネルによって決まります。どちらも存在しない場合は100%になります。 テキストレイヤーの前景の不透明度は100%で、べた塗りレイヤーの前景の不透明度は`color=`で設定される。

`opac=` またはで塗りつぶされた領域の不透明度は変 `color=` 更しませ `bgColor=`ん（べた塗りレイヤーとエフェクトレイヤーの前景領域を除く）。 `color=`

画像、テキスト、またはソリッドカラーレイヤーで指定した場合、*`opacity`*&#x200B;は関連するすべてのエフェクトレイヤーを含むレイヤー全体を適用し、*`fillOpacity`*&#x200B;はプライマリレイヤーのコンテンツにのみ適用します。 エフェクトレイヤーで指定した場合、*`opacity`*&#x200B;はエフェクトレイヤーに適用され、*`fillOpacity`*&#x200B;は無視されます。

メインレイヤーコンテンツの有効な不透明度は( *`opacity`* * *`fillOpacity`* / 100)です。 効果レイヤーの有効な不透明度は（メインの&#x200B;*`opacity`* *効果&#x200B;*`opacity`* / 100）です。

## プロパティ {#section-ac3f136ff1584a2eab87500b7164f7fa}

レイヤー属性。 `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。

## 初期設定 {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`（レイヤーの不透明度は変更されません）。

## 例 {#section-9710810e96af40538652e8ae4aadd3be}

... `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`...

この例では、テキストの不透明度は90*70/100=63%、効果レイヤーの不透明度は90*50/100=45%です。

## 関連項目 {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
