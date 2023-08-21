---
title: ネットワーク
description: ネットワーク帯域幅の最適化を使用して、実際のネットワーク帯域幅に基づいて提供される画質を調整する方法について説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 2%

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

DPR およびネットワーク帯域幅の値は、バンドルされた CDN の検出されたクライアント側の値に基づいています。 これらの値は不正確な場合があります。 例：iPhone5 と `dpr=2`、およびiPhone12 と `dpr=3`、両方を表示 `dpr=2`. 高解像度デバイスの場合は、送信 `dpr=2` は、dpr=1 を送信するよりも適しています。 ただし、この不正確さを克服する最善の方法は、クライアント側の DPR を使用して 100%の正確な値を得ることです。 また、起動された任意のデバイス (Appleかその他のデバイスかに関わらず ) で機能します。 詳しくは、 [クライアント側デバイスのピクセル比でのスマートイメージングの使用](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## プロパティ



## 初期設定

`network=off`

## 例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## 関連項目

[drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [スマートイメージング](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)