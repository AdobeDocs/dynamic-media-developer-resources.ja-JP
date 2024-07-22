---
title: dpr
description: デバイスピクセル比（DPR）&mdash；は CSS ピクセル比とも呼ばれます&mdash；は、デバイスの物理ピクセルと論理ピクセルの関係です。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d64ca9ed-7d8e-4a13-9c9d-acb7de3e31ed
source-git-commit: 63c0e3b494b6d583117dad01643946900855802e
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 2%

---

# dpr{#dpr}

デバイスピクセル比（DPR）（CSS ピクセル比とも呼ばれます）は、デバイスの物理ピクセルと論理ピクセルの関係です。 特に、Retina 画面の出現に伴い、最新のモバイルデバイスのピクセル解像度が急速に増加しています。

デバイスピクセル比の最適化を有効にすると、画像が画面のネイティブ解像度でレンダリングされるので、画面が鮮明に見えます。

現在、ディスプレイのピクセル密度は Akamai CDN ヘッダー値から得られます。

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> off </span> </span> </p> </td> 
  <td class="stentry"> <p>個々の画像 URL レベルで DPR の最適化をオフにします。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> on, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>スマートイメージングで検出された DPR 値を、カスタム値（クライアント側のロジックまたはその他の手段で検出された値）でオーバーライドします。 dprValue に指定可能な値は、0 より大きい任意の数です。 </p> </td> 
 </tr> 
</table>


全社レベルの DPR 設定がオフの場合でも、`dpr=on,dprValue` を使用できます。

DPR の最適化により、結果の画像がDynamic Mediaの MaxPix 設定よりも大きくなる場合、画像の縦横比を保つことで MaxPix の幅が常に認識されます。

| 要求された画像サイズ | DPR 値 | 配信される画像サイズ |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

DPR 値は、バンドルされた CDN のクライアント側の検出値に基づいています。 これらの値は不正確な場合があります。 例えば、`dpr=2` を使用するiPhone5 と dpr=3 を使用するiPhone12 では、どちらも `dpr=2` と表示されます。 それでも、高解像度デバイスの場合は、`dpr=1` を送信するより `dpr=2` を送信する方が適切です。 この不正確さを克服する最善の方法は、クライアントサイドの DPR を使用して 100% 正確な値を指定することです。 また、起動されたデバイスがAppleか他のデバイスかに関わらず、任意のデバイスで機能します。 [ クライアントサイドのデバイスピクセル比（DPR）を使用したスマートイメージングについて ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en) を参照してください。

## プロパティ

リクエスト属性。 `dpr` がオフの場合や `dprValue=1` の場合は、効果はありません。

## 初期設定

`dpr=off`


## 例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## 関連項目

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md)、[ ネットワーク ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md)、[ スマートイメージング ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)
