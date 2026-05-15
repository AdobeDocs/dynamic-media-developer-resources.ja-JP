---
title: opac
description: 画像の不透明度を調整します。 画像、テキスト、単色、エフェクトレイヤーの前景の不透明度を下げることができます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
TQID: 'https://experienceleague.adobe.com/--AimuhKd3XDT-daEAA73WfUPmCZmaCXSrXmLVO8Y6I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 223
ht-degree: 1%

---

# opac{#opac}

画像の不透明度を調整します。 画像、テキスト、単色、エフェクトレイヤーの前景の不透明度を下げることができます。

`opac= *`不透明度`*[, *`fillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">不透明度</span> </p> </td> 
  <td class="stentry"> <p>プライマリの不透明度（0...100 int） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>塗りつぶしの不透明度（0...100 int） </p></td> 
 </tr> 
</table>

画像レイヤーの前景の不透明度は、レイヤーマスクまたは画像のアルファチャンネルによって決まります。どちらも存在しない場合は、100%になります。 テキストレイヤーの描画不透明度は100%で、単色レイヤーの描画不透明度は`color=`で設定されます。

`opac=`は、`color=`または`bgColor=`で塗りつぶされた領域の不透明度を変更しません。ただし、単色レイヤーと効果レイヤーの前景の領域（`color=`で設定）は変更されません。

画像、テキスト、または単色レイヤーで指定した場合、*`opacity`*&#x200B;は、関連するすべてのエフェクトレイヤーを含むレイヤー全体を適用し、*`fillOpacity`*&#x200B;はプライマリレイヤーのコンテンツにのみ適用されます。 エフェクトレイヤーで指定すると、*`opacity`*&#x200B;はエフェクトレイヤーに適用されますが、*`fillOpacity`*&#x200B;は無視されます。

メインレイヤーのコンテンツの効果的な不透明度は（*`opacity`* &#42; *`fillOpacity`* / 100）です。 エフェクトレイヤーの効果的な不透明度は（メイン *`opacity`* &#42; エフェクト *`opacity`* / 100）です。

## プロパティ {#section-ac3f136ff1584a2eab87500b7164f7fa}

レイヤー属性。 現在のレイヤーまたは`layer=comp`の場合はコンポジット画像に適用されます。

## 初期設定 {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100` （レイヤーの不透明度は変更されません）。

## 例 {#section-9710810e96af40538652e8ae4aadd3be}

... `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`...

この例のテキストの不透明度は90&#42;70/100=63%、エフェクトレイヤーの不透明度は90&#42;50/100=45%です。

## 関連項目 {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
