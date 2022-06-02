---
title: 効果
description: '[ 効果レイヤ ] を選択します。 効果レイヤを選択し、現在のレイヤに関連付けられている要求文字列の新しいレイヤセグメントを開始します。'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 4%

---

# 効果{#effect}

[ 効果レイヤ ] を選択します。 効果レイヤを選択し、現在のレイヤに関連付けられている要求文字列の新しいレイヤセグメントを開始します。

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>エフェクトレイヤー番号（整数は 0 に等しくありません）。 </p></td> 
 </tr> 
</table>

新しいセグメント内のすべてのコマンドが、指定したエフェクトレイヤに適用されます。 エフェクトレイヤセグメントは次の `layer=` または `effect=` コマンドを使用するか、リクエストの最後に置き換えます。

*`n`* は、外側のレイヤー効果（親レイヤーの背後の効果）の場合は 0 より小さい値、内側のレイヤー効果（親レイヤー内の効果）の場合は 0 より大きい値にする必要があります。 エフェクトレイヤー番号は、連続する必要はありません。

同じ親レイヤーに対して複数のエフェクトレイヤーがある場合、エフェクトレイヤー番号は z オーダーを指定します。 高い番号のレイヤーは、下の番号のレイヤーの上に配置されます。

エフェクトレイヤーは `layer=comp`.

## プロパティ {#section-e11f795deff345779ce280a82cf221ca}

エフェクトレイヤーコマンド *`n`* は 0 にはできません。

## 初期設定 {#section-84bbe1cfe7a94040827c994323ac59d4}

なし

## 例 {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## 関連項目 {#section-573273e9e0e64103a5764075f5e50180}

[layer=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
