---
description: 詳細レンダリング設定 現在の選択範囲をレンダリングする際に適用される詳細レンダリング設定を指定します。
seo-description: 詳細レンダリング設定 現在の選択範囲をレンダリングする際に適用される詳細レンダリング設定を指定します。
seo-title: rs
solution: Experience Manager
title: rs
topic: Scene7 Image Serving - Image Rendering API
uuid: 4ff7fcb4-a10a-4e82-80a1-edf79ae1f717
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# rs{#rs}

詳細レンダリング設定 現在の選択範囲をレンダリングする際に適用される詳細レンダリング設定を指定します。

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>レンダリング設定文字列 </p></td> 
 </tr> 
</table>

レンダリングの外観を微調整するために使用します。 ビネットオーサリングツール（Scene7 Image Authoringパッケージの一部）のレンダリング機能を使用して、レンダリング設定文字列を作成します。

## プロパティ {#section-9a2b2228789046658cb80eddf343af75}

マテリアル属性。

## 初期設定 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings` をクリックします。

## 例 {#section-47e4811882574441a4d517e42a35f352}

画像オーサリングで実験を行った後、アンシャープマスク(USM)が、特定のアプリケーションとマテリアルに対して適切な量のシャープを適用することが判別されます。 USMを設定するレンダリング設定文字列は、次のマテリアルで使用す `rs=` るコマンドにコピーされます。

`…&rs=U2V20W50X2&…`

## 関連項目 {#section-930116e735024a008c994547ba36ee40}

[catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
