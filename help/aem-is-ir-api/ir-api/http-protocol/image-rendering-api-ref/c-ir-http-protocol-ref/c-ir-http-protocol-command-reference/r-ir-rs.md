---
title: rs
description: レンダリングの詳細設定 現在の選択をレンダリングするときに適用される高度なレンダリング設定を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# rs{#rs}

レンダリングの詳細設定 現在の選択をレンダリングするときに適用される高度なレンダリング設定を指定します。

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>レンダリング設定文字列。 </p></td> 
 </tr> 
</table>

レンダリングの外観を微調整するために使用します。 レンダリング設定文字列を作成するには、ビネットオーサリングツール（Dynamic Media画像オーサリングパッケージの一部）のレンダリング機能を使用します。

## プロパティ {#section-9a2b2228789046658cb80eddf343af75}

マテリアル アトリビュート。

## 初期設定 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings` をクリックします。

## 例 {#section-47e4811882574441a4d517e42a35f352}

画像オーサリングでいくつかの実験を行った後、アンシャープマスク （USM）により特定のアプリケーションとマテリアルに対して適切な量のシャープニングが提供されることが判明しました。 USM を構成するレンダリング設定文字列は、このマテリアルで使用する `rs=` コマンドにコピーされます。

`…&rs=U2V20W50X2&…`

## 関連項目 {#section-930116e735024a008c994547ba36ee40}

[カタログ：:RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
