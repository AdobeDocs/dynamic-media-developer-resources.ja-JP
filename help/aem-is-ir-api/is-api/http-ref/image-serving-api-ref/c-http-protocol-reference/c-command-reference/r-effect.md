---
description: 「エフェクトレイヤー」を選択します。 エフェクトレイヤーを選択し、現在のレイヤーに関連付けられている要求文字列で新しいレイヤーセグメントを開始します。
seo-description: 「エフェクトレイヤー」を選択します。 エフェクトレイヤーを選択し、現在のレイヤーに関連付けられている要求文字列で新しいレイヤーセグメントを開始します。
seo-title: 効果
solution: Experience Manager
title: 効果
topic: Scene7 Image Serving - Image Rendering API
uuid: 622dc7ca-55b8-4a82-b9a7-65588aee87d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# effect{#effect}

「エフェクトレイヤー」を選択します。 エフェクトレイヤーを選択し、現在のレイヤーに関連付けられている要求文字列で新しいレイヤーセグメントを開始します。

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>効果のレイヤー番号（整数が0ではない）。 </p></td> 
 </tr> 
</table>

新しいセグメント内のすべてのコマンドが、指定したエフェクトレイヤーに適用されます。 エフェクトレイヤーセグメントは、次のコマンドまたはコ `layer=` マンドに `effect=` よって、または要求の終わりによって終了されます。

*`n`* は、外側のレイヤー効果（親レイヤーの背後の効果）に対しては0より小さい値、内側のレイヤー効果（親レイヤー内の効果）に対しては0より大きい値に設定する必要があります。 エフェクトのレイヤー番号は連続している必要はありません。

エフェクトレイヤー番号は、同じ親レイヤーに対して複数のエフェクトレイヤーがある場合のz順序を指定します。 大きい番号のレイヤーは、小さい番号のレイヤーの上に配置されます。

エフェクトレイヤーは、にアタッチすることができま `layer=comp`す。

## プロパティ {#section-e11f795deff345779ce280a82cf221ca}

エフェクトレイヤーコマンド *`n`* は0にできません。

## 初期設定 {#section-84bbe1cfe7a94040827c994323ac59d4}

なし

## 例 {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## 関連項目 {#section-573273e9e0e64103a5764075f5e50180}

` [layer=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d)`
