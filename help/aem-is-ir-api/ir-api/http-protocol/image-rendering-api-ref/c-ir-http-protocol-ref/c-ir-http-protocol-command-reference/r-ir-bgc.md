---
description: 背景色. 色付け可能なテクスチャとデカルの減色カラーを指定します。
solution: Experience Manager
title: bgc
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 6%

---

# bgc{#bgc}

背景色. 色付け可能なテクスチャとデカルの減色カラーを指定します。

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGBまたはグレーのカラー値 </p></td> 
 </tr> 
</table>

Image Renderingのテクスチャの色付けアルゴリズムは非常に単純で、 `bgc=`の成分値がテクスチャピクセルの成分値から減算され、 `color=`が加算され、最後に`0,0,0`と`255,255,255`にクリップされます。

テクスチャの色付けを一般的に使用する場合、`bgc=`の値は、テクスチャイメージで最も重要または優先的なカラーになります。 Dynamic Media Image Authoringは、テクスチャイメージから適切な`bgc=`色の値を抽出する半自動ツールを提供します。

テクスチャマテリアルがテクスチャ化されないビネットオブジェクトに適用される場合、 `color=`が指定されていないと、 `bgc=`が前景色として適用されます。

## プロパティ {#section-b2db6f147d7f443ba9f671de04c2ef19}

マテリアル属性。 ソリッドカラーとキャビネットのマテリアルでは無視されます。

## 初期設定 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` マテリアルがカタログエントリに基づいている場合は、それ以外の場合は( `bgc=808080` ニュートラルグレー)。

## 例 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

120,34,193の優れたRGBカラーを持つアパレル生地をカラー化する。

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 関連項目 {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) 、 [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
