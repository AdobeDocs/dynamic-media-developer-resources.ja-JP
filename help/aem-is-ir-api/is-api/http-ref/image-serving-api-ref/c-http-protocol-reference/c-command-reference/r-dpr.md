---
title: dpr
description: デバイスピクセルレシオ（DPR）&mdash;CSS ピクセル比&mdashとも呼ばれます；は、デバイスの物理ピクセルと論理ピクセルの関係です。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d64ca9ed-7d8e-4a13-9c9d-acb7de3e31ed
TQID: 'https://experienceleague.adobe.com/cYp-WX-2PUiJ5sKTsxlKEXrjo6TrRegBJc6tPLbleGg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 355
ht-degree: 2%

---

# dpr{#dpr}

デバイスピクセルレシオ（DPR）とは、デバイスの物理ピクセルと論理ピクセルの関係のことです。CSS ピクセル比とも呼ばれています。 特に網膜スクリーンの登場により、現代のモバイルデバイスのピクセル解像度は急速に成長しています。

デバイスピクセルレシオの最適化を有効にすると、画像が画面のネイティブ解像度でレンダリングされ、シャープになります。

現在、ディスプレイのピクセル密度はAkamai CDN ヘッダー値に基づいています。

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> オフ </span> </span> </p> </td> 
  <td class="stentry"> <p>個々の画像URL レベルでDPR最適化をオフにします。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> （上）、dpr値</span> </span> </p> </td> 
  <td class="stentry"> <p>スマートイメージングで検出されたDPR値を、カスタム値（クライアントサイドのロジックやその他の方法で検出されたもの）で上書きします。 dprValueの許可される値は0より大きい任意の数値です。 </p> </td> 
 </tr> 
</table>


会社レベルのDPR設定がオフの場合でも、`dpr=on,dprValue`を使用できます。

DPR最適化により、結果の画像がMaxPix Dynamic Media設定よりも大きい場合、画像の縦横比を維持することでMaxPixの幅が常に認識されます。

| 要求された画像サイズ | DPR値 | 配信画像サイズ |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

DPR値は、バンドルされたCDNの検出されたクライアントサイドの値に基づいています。 これらの値は不正確な場合があります。 例えば、`dpr=2`のiPhone5とdpr=3のiPhone12は、両方とも`dpr=2`を表示します。 ただし、高解像度デバイスの場合、`dpr=2`を送信するほうが`dpr=1`を送信するよりも優れています。 しかし、この不正確さを克服する最良の方法は、クライアントサイドのDPRを使用して100%正確な値を提供することです。 Appleやリリースされたその他のデバイスを問わず、あらゆるデバイスで機能します。 「[&#x200B; クライアントサイドのデバイスピクセルレシオでスマートイメージングを使用する](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en)」を参照してください。

## プロパティ

リクエスト属性。 `dpr`がオフの場合や`dprValue=1`の場合は効果がありません。

## 初期設定

`dpr=off`


## 例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## 関連項目

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md)、[network](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md)、[&#x200B; スマートイメージング &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)
