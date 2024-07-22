---
title: 効果
description: 「エフェクトレイヤー」を選択します。 エフェクトレイヤーを選択し、現在のレイヤーに関連付けられているリクエスト文字列で新しいレイヤーセグメントを開始します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# 効果{#effect}

「エフェクトレイヤー」を選択します。 エフェクトレイヤーを選択し、現在のレイヤーに関連付けられているリクエスト文字列で新しいレイヤーセグメントを開始します。

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>エフェクトのレイヤー番号（整数が 0 以外）。 </p></td> 
 </tr> 
</table>

新しいセグメント内のすべてのコマンドが、指定したエフェクトレイヤーに適用されます。 エフェクトレイヤーセグメントは、次の `layer=` または `effect=` のコマンド、またはリクエストの終了によって終了します。

*`n`* の値は、外側のレイヤー効果（親レイヤーの後ろの効果）では 0 未満、内側のレイヤー効果（親レイヤー内の効果）では 0 より大きくなければなりません。 エフェクトレイヤーの番号が連続している必要はありません。

同じ親レイヤーに複数のエフェクトレイヤーがある場合、エフェクトレイヤー番号で Z オーダーを指定します。 番号の大きいレイヤーは、番号の小さいレイヤーの上に配置されます。

エフェクトレイヤーは `layer=comp` に添付できます。

## プロパティ {#section-e11f795deff345779ce280a82cf221ca}

[ 効果レイヤ ] コマンド： 値 *`n`* を 0 にすることはできません。

## 初期設定 {#section-84bbe1cfe7a94040827c994323ac59d4}

なし

## 例 {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## 関連項目 {#section-573273e9e0e64103a5764075f5e50180}

[レイヤ=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
