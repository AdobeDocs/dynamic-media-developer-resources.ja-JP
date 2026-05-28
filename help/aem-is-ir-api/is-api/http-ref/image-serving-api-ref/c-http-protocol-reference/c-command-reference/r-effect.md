---
title: エフェクト
description: エフェクトレイヤーを選択します。 エフェクトレイヤーを選択し、現在のレイヤーに関連付けられているリクエスト文字列で新しいレイヤーセグメントを開始します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
TQID: 'https://experienceleague.adobe.com/aWZh6cu9IoOFP6x5LW-Qa-Pia-uu-hQfUQJbN4FeYn0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 185
ht-degree: 2%

---

# エフェクト{#effect}

エフェクトレイヤーを選択します。 エフェクトレイヤーを選択し、現在のレイヤーに関連付けられているリクエスト文字列で新しいレイヤーセグメントを開始します。

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>エフェクトレイヤー番号（0以外の整数）。 </p></td> 
 </tr> 
</table>

新規セグメント内のすべてのコマンドは、指定したエフェクトレイヤーに適用されます。 エフェクトレイヤーセグメントは、次の`layer=`または`effect=` コマンド、またはリクエストの最後までに終了します。

値&#x200B;*`n`*&#x200B;は、外側のレイヤー効果（親レイヤーの背後にある効果）では0未満、内側のレイヤー効果（親レイヤー内の効果）では0より大きい値である必要があります。 エフェクトレイヤーの番号は連続している必要はありません。

エフェクトレイヤー番号は、同じ親レイヤーに複数のエフェクトレイヤーがある場合のZ次を指定します。 番号の高いレイヤーは、番号の低いレイヤーの上に配置されます。

エフェクトレイヤーは`layer=comp`にアタッチできます。

## プロパティ {#section-e11f795deff345779ce280a82cf221ca}

エフェクトレイヤーコマンド。 値&#x200B;*`n`*&#x200B;は0にできません。

## 初期設定 {#section-84bbe1cfe7a94040827c994323ac59d4}

なし

## 例 {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## 関連項目 {#section-573273e9e0e64103a5764075f5e50180}

[layer=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
