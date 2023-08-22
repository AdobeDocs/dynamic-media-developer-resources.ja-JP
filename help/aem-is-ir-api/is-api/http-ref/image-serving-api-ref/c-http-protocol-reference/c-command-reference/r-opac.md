---
title: opac
description: 画像の不透明度を調整します。 画像、テキスト、べた塗り、効果レイヤーの前景の不透明度を下げることができます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---

# opac{#opac}

画像の不透明度を調整します。 画像、テキスト、べた塗り、効果レイヤーの前景の不透明度を下げることができます。

`opac= *`不透明度`*[, *`fillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 不透明度</span> </p> </td> 
  <td class="stentry"> <p>プライマリの不透明度 (0 ～ 100 int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>塗りの不透明度 (0 ～ 100 int)。 </p></td> 
 </tr> 
</table>

イメージレイヤーの前景の不透明度は、イメージのレイヤーマスクまたはアルファチャンネルによって決まります。不明な場合は 100 %です。 テキストレイヤーの前景の不透明度は 100%、べた塗りレイヤーの不透明度は `color=`.

`opac=` 塗りつぶされた領域の不透明度を変更しない `color=` または `bgColor=`（べた塗りレイヤーとエフェクトレイヤーの前景領域を除く） `color=`) をクリックします。

画像、テキスト、またはべた塗りのレイヤーで指定した場合、 *`opacity`* 関連するすべてのエフェクトレイヤーを含め、レイヤー全体を適用します。 *`fillOpacity`* は、プライマリレイヤコンテンツにのみ適用されます。 エフェクトレイヤーで指定した場合、 *`opacity`* エフェクトレイヤーに適用され、 *`fillOpacity`* は無視されます。

メインレイヤーのコンテンツに対して有効な不透明度は、 ( *`opacity`* &#42; *`fillOpacity`* / 100) です。 エフェクトレイヤーに対して有効な不透明度は（メイン）です。 *`opacity`* &#42; 効果 *`opacity`* / 100) です。

## プロパティ {#section-ac3f136ff1584a2eab87500b7164f7fa}

レイヤー属性。 現在の画層または合成画像に適用されます ( `layer=comp`.

## 初期設定 {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`（レイヤーの不透明度は変更されません）。

## 例 {#section-9710810e96af40538652e8ae4aadd3be}

... `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`...

この例では、テキストの不透明度は 90 です。&#42;70/100 = 63%、効果レイヤーの不透明度は 90&#42;50/100=45%。

## 関連項目 {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
