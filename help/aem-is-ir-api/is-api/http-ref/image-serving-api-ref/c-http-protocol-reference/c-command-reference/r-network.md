---
title: ネットワーク
description: ネットワーク帯域幅の最適化を使用して、実際のネットワーク帯域幅に基づいて提供される画質を調整する方法について説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7df6eeed-1856-40e1-bd5d-8f06efc7f700
source-git-commit: 63c0e3b494b6d583117dad01643946900855802e
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 4%

---

# ネットワーク{#network}

「ネットワーク帯域幅」をオンにすると、提供される画質が、実際のネットワーク帯域幅に基づいて自動的に調整されます。 ネットワーク帯域幅が不十分な場合は、[DPR （デバイスピクセル比） ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) 最適化がオンになっていても、自動的にオフになります。

必要に応じて、画像の URL にを付けて、個々の画像レベルでネットワーク帯域幅の最適化をオプトアウト `network=off` きます。

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> on|off </span> </p> </td> 
  <td class="stentry"> <p>実際のネットワーク帯域幅に基づいて提供される画質をネットワーク帯域幅で調整するか（オン）、画質を調整しない場合にネットワーク帯域幅の最適化をオフにするかを指定します。</p> </td> 
 </tr> 
</table>

ネットワーク帯域幅の値は、バンドルされた CDN のクライアント側の検出値に基づいています。

## プロパティ

リクエスト属性。 ネットワークの状態が良好な場合は効果はありません。

## 初期設定

`network=off`

## 例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## 関連項目

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md)、[drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md)、[ スマートイメージング ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=ja)
