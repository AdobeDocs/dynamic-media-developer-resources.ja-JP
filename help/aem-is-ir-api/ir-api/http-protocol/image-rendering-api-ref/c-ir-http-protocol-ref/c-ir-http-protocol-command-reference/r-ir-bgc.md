---
title: bgc
description: 背景色： 色付け可能なテクスチャとデカールの減算カラーを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
TQID: 'https://experienceleague.adobe.com/0Er9kHrfQj1lt14SlNJHxqddJZOp8BaO-lLYSqc5ajU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 159
ht-degree: 2%

---

# bgc {#bgc}

背景色： 色付け可能なテクスチャとデカールの減算カラーを指定します。

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> カラー</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGBまたはグレーの値。 </p></td> 
 </tr> 
</table>

画像レンダリングのテクスチャ色付けアルゴリズムは簡単です。`bgc=`のコンポーネント値がテクスチャピクセルの値から差し引かれ、`color=`が追加され、最終的に`0,0,0`と`255,255,255`にクリップされます。

テクスチャのカラー化の一般的な用途では、`bgc=`の値は、テクスチャ画像で最も重要または支配的な色である可能性があります。 Dynamic Media画像オーサリングは、テクスチャ画像から合理的な`bgc=`色の値を抽出する半自動ツールを提供します。

テクスチャマテリアルがテクスチャリングできないビネットオブジェクトに適用される場合、`color=`が指定されていない場合、`bgc=`が描画色として適用されます。

## プロパティ {#section-b2db6f147d7f443ba9f671de04c2ef19}

マテリアル属性： 単色およびキャビネットのマテリアルでは無視されます。

## 初期設定 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` マテリアルがカタログ エントリに基づいている場合、それ以外の場合は`bgc=808080` （ニュートラル グレー）。

## 例 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

テクスチャが支配的なRGB カラーを持つアパレル生地をカラー化する120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 関連項目 {#section-de9958dd63a742b4b5d780c59a57da33}

[&#x200B; カタログ：:BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8)、[color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)

