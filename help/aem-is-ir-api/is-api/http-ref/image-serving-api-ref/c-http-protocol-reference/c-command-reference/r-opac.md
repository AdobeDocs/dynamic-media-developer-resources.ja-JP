---
title: opac
description: 画像の不透明度を調整する 画像、テキスト、ソリッドカラーまたはエフェクトレイヤーの前景の不透明度を下げることができます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# opac{#opac}

画像の不透明度を調整する 画像、テキスト、ソリッドカラーまたはエフェクトレイヤーの前景の不透明度を下げることができます。

`opac= *`opacity`*[, *`fillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> の不透明度 </span> </p> </td> 
  <td class="stentry"> <p>プライマリの不透明度（0...100 int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>fillOpacity<span class="varname"> 指定 </span> </p></td> 
  <td class="stentry"> <p>塗りつぶしの不透明度（0...100 int） </p></td> 
 </tr> 
</table>

イメージレイヤのフォアグラウンドの不透明度は、レイヤーマスクまたはイメージのアルファチャンネルによって決まります。どちらも存在しない場合は 100% になります。 テキストレイヤーの前景の不透明度は 100% で、ソリッドカラーレイヤーの前景の不透明度は `color=` で設定されます。

`opac=` では、`color=` または `bgColor=` で塗りつぶされた領域の不透明度は変更されません。ただし、単色レイヤーとエフェクトレイヤー（`color=` で設定）の前景領域は変更されません。

画像、テキスト、または単色のレイヤーで指定した場合、*`opacity`* は関連するすべてのエフェクトレイヤーを含むレイヤー全体を適用し、*`fillOpacity`* はプライマリレイヤーのコンテンツにのみ適用します。 エフェクトレイヤーで指定した場合、*`opacity`* はエフェクトレイヤーに適用されますが、*`fillOpacity`* は無視されます。

メインレイヤーコンテンツの有効な不透明度は（*`opacity`* &#42; *`fillOpacity`* / 100）です。 エフェクトレイヤーの有効な不透明度は（メイン *`opacity`* &#42; エフェクト *`opacity`* / 100）です。

## プロパティ {#section-ac3f136ff1584a2eab87500b7164f7fa}

レイヤー属性。 現在のレイヤーまたは合成イメージ（`layer=comp` の場合）に適用されます。

## 初期設定 {#section-abba67ed028049048ae43405ea69b164}

レイヤーの不透明度を変更せずに `opac=100,100` きます。

## 例 {#section-9710810e96af40538652e8ae4aadd3be}

...`&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`...

この例では、テキストの不透明度は 90&#42;70/100=63%、エフェクトレイヤーの不透明度は 90&#42;50/100=45% です。

## 関連項目 {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
