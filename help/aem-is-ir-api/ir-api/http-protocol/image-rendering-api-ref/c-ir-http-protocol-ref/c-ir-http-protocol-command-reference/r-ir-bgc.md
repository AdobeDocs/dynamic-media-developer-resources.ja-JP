---
title: bgc
description: 背景色. 色付け可能なテクスチャとデカールの減算カラーを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 6%

---

# bgc {#bgc}

背景色. 色付け可能なテクスチャとデカールの減算カラーを指定します。

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGBまたはグレーのカラー値。 </p></td> 
 </tr> 
</table>

画像レンダリングのテクスチャカラー化アルゴリズムは簡単です。 `bgc=` は、テクスチャピクセルの値から減算されます。 `color=` が追加され、最後に結果が次の値にクリップされます。 `0,0,0` および `255,255,255`.

テクスチャのカラー化を一般的に使用する場合、 `bgc=` は、テクスチャイメージ内で最も重要または優れたカラーです。 Dynamic Media Image Authoring には、合理的な抽出を行う半自動ツールが用意されています `bgc=` テクスチャイメージのカラー値。

テクスチャマテリアルをテクスチャ化できないビネットオブジェクトに適用した場合、 `bgc=` が `color=` が指定されていません。

## プロパティ {#section-b2db6f147d7f443ba9f671de04c2ef19}

材料属性。 べた塗りとキャビネットのマテリアルでは無視されます。

## 初期設定 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` マテリアルがカタログエントリに基づいている場合は、それ以外の場合は `bgc=808080` （ニュートラルグレー）。

## 例 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

120,34,193 を支配するRGB色を持つアパレル生地に色彩を加える。

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 関連項目 {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
