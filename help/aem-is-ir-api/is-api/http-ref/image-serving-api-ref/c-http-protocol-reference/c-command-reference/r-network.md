---
title: ネットワーク
description: ネットワーク帯域幅の最適化を使用して、実際のネットワーク帯域幅に基づいて提供される画質を調整する方法について説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7df6eeed-1856-40e1-bd5d-8f06efc7f700
TQID: 'https://experienceleague.adobe.com/9odHf3s93xaQyc1WSkXGamAgoQP070p7ItB9HhyT-dQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 3%

---

# ネットワーク{#network}

「ネットワーク帯域幅」をオンにすると、実際のネットワーク帯域幅に基づいて提供される画質が自動的に調整されます。 ネットワーク帯域幅が低い場合は、[DPR （デバイス ピクセル比） ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md)最適化は、既にオンになっていても、自動的にオフになります。

必要に応じて、画像のURLに`network=off`を追加することで、個々の画像レベルでネットワーク帯域幅の最適化をオプトアウトできます。

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> on|off </span> </p> </td> 
  <td class="stentry"> <p>ネットワーク帯域幅が実際のネットワーク帯域幅（on）に基づいて提供される画質を調整するか、画質を調整しない場合にネットワーク帯域幅の最適化をオフにするかを指定します。</p> </td> 
 </tr> 
</table>

ネットワーク帯域幅の値は、バンドルされたCDNの検出されたクライアントサイドの値に基づいています。

## プロパティ

リクエスト属性。 ネットワークの状態が良好であれば効果はありません。

## 初期設定

`network=off`

## 例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## 関連項目

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md)、[drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md)、[ スマートイメージング ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)
