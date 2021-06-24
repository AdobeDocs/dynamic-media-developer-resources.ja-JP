---
description: 詳細なレンダリング設定。 現在の選択範囲をレンダリングする際に適用する詳細なレンダリング設定を指定します。
solution: Experience Manager
title: rs
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# rs{#rs}

詳細なレンダリング設定。 現在の選択範囲をレンダリングする際に適用する詳細なレンダリング設定を指定します。

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>レンダリング設定文字列。 </p></td> 
 </tr> 
</table>

レンダリングの外観を微調整するために使用します。 ビネットオーサリングツール(Dynamic Media Image Authoringパッケージの一部)のレンダリング機能を使用して、レンダリング設定文字列を作成します。

## プロパティ {#section-9a2b2228789046658cb80eddf343af75}

マテリアル属性。

## 初期設定 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings` をクリックします。

## 例 {#section-47e4811882574441a4d517e42a35f352}

画像オーサリングで何らかの実験を行った後、特定のアプリケーションおよびマテリアルに対して、アンシャープマスク(USM)が正しい量のシャープを提供すると判断されます。 USMを設定するレンダリング設定文字列は、このマテリアルで使用するように`rs=`コマンドにコピーされます。

`…&rs=U2V20W50X2&…`

## 関連項目 {#section-930116e735024a008c994547ba36ee40}

[catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
