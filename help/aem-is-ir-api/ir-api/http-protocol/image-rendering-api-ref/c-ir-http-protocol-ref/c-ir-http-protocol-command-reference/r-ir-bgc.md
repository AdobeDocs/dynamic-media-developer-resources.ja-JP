---
title: bgc
description: 背景色。 色付け可能なテクスチャとデカールの減算色を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# bgc {#bgc}

背景色。 色付け可能なテクスチャとデカールの減算色を指定します。

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> 色 </span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGBまたはグレーのカラー値。 </p></td> 
 </tr> 
</table>

画像レンダリングのテクスチャの色付けアルゴリズムは簡単です。`bgc=` のコンポーネント値がテクスチャピクセルの値から減算され、`color=` が追加されて、最終的に結果が `0,0,0` にクリップされて `255,255,255` になります。

テクスチャのカラー化を一般的に使用する場合、`bgc=` の値はテクスチャ イメージの中で最も重要または支配的なカラーになります。 Dynamic Media画像オーサリングには、テクスチャ画像から適切な `bgc=` 色の値を抽出する半自動ツールが用意されています。

テクスチャ マテリアルをテクスチャ化できないビネット オブジェクトに適用すると、`bgc=` が指定されていない場合、前景色として適用さ `color=` ます。

## プロパティ {#section-b2db6f147d7f443ba9f671de04c2ef19}

マテリアル アトリビュート。 単色およびキャビネット材料では無視されます。

## 初期設定 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` 材料がカタログエントリに基づいている場合、それ以外の場合は `bgc=808080` （ニュートラルグレー）。

## 例 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

生地のRGBの色が支配的なアパレル生地に 120,34,193 色を付けます。

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 関連項目 {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
