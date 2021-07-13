---
description: '[効果レイヤ]を選択します。 エフェクトレイヤを選択し、現在のレイヤに関連付けられたリクエスト文字列の新しいレイヤセグメントを開始します。'
solution: Experience Manager
title: 効果
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 3%

---

# 効果{#effect}

[効果レイヤ]を選択します。 エフェクトレイヤを選択し、現在のレイヤに関連付けられたリクエスト文字列の新しいレイヤセグメントを開始します。

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>エフェクトレイヤー番号（整数が0に等しくない）。 </p></td> 
 </tr> 
</table>

新しいセグメント内のすべてのコマンドが、指定したエフェクトレイヤに適用されます。 次の`layer=`コマンドや`effect=`コマンド、または要求の終わりによって、効果レイヤセグメントが終了します。

*`n`* は、外側のレイヤー効果（親レイヤーの背後の効果）の場合は0より小さく、内側のレイヤー効果（親レイヤー内の効果）の場合は0より大きい値にする必要があります。エフェクトレイヤ番号は、連続する必要はありません。

同じ親レイヤーに複数のエフェクトレイヤーがある場合、エフェクトレイヤー番号はz順を指定します。 番号の大きいレイヤーは、番号の小さいレイヤーの上に配置されます。

`layer=comp`にエフェクトレイヤをアタッチできます。

## プロパティ {#section-e11f795deff345779ce280a82cf221ca}

エフェクトレイヤーコマンド *`n`* は0にできません。

## 初期設定 {#section-84bbe1cfe7a94040827c994323ac59d4}

なし

## 例 {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## 関連項目 {#section-573273e9e0e64103a5764075f5e50180}

` [layer=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d)`
