---
title: ネットワーク
description: ネットワーク帯域幅の最適化を使用して、実際のネットワーク帯域幅に基づいて提供される画質を調整する方法について説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: a6e0db8238ba5f2209089c6eda7b42c42f66b25f
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 3%

---

# ネットワーク{#network}

「ネットワーク帯域幅」をオンにすると、実際のネットワーク帯域幅に基づいて提供される画質が自動的に調整されます。 ネットワーク帯域幅が低い場合は、 [DPR（デバイスのピクセル比）](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) 最適化は、既にオンになっている場合でも、自動的にオフになります。

必要に応じて、個々の画像レベルでネットワーク帯域幅の最適化をオプトアウトするには、 `network=off` を画像の URL に追加します。

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> on|off </span> </p> </td> 
  <td class="stentry"> <p>実際のネットワーク帯域幅に基づいて提供される画質をネットワーク帯域幅で調整するか（オン）、画質を調整しない場合はネットワーク帯域幅の最適化をオフにするかを指定します。</p> </td> 
 </tr> 
</table>

ネットワーク帯域幅の値は、バンドルされた CDN で検出されたクライアント側の値に基づきます。

## プロパティ

request 属性。 ネットワークの状態が良好な場合は、効果はありません。

## 初期設定

`network=off`

## 例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## 関連項目

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [スマートイメージング](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)