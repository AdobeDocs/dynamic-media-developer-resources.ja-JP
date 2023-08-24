---
title: dpr
description: Device Pixel Ratio(DPR)&mdash（CSS pixel ratio&mdash とも呼ばれます）は、デバイスの物理ピクセルと論理ピクセルとの関係です。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: a6e0db8238ba5f2209089c6eda7b42c42f66b25f
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 2%

---

# dpr{#dpr}

Device Pixel Ratio(DPR)（CSS ピクセル比とも呼ばれます）は、デバイスの物理ピクセルと論理ピクセルとの関係です。 特に、Retina スクリーンの登場に伴い、最新のモバイルデバイスのピクセル解像度が急速に増加しています。

デバイスのピクセル比の最適化を有効にすると、画像が画面のネイティブ解像度でレンダリングされ、シャープになります。

現在、表示のピクセル密度は Akamai CDN ヘッダー値に基づいています。

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> オフ </span> </span> </p> </td> 
  <td class="stentry"> <p>個々の画像 URL レベルで DPR 最適化をオフにします。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> on, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>スマートイメージングで検出された DPR 値を、カスタム値（クライアント側のロジックまたは他の手段で検出された値）で上書きします。 dprValue に許可されている値は、0 より大きい任意の数です。 </p> </td> 
 </tr> 
</table>


以下を使用できます。 `dpr=on,dprValue` （会社レベルの DPR 設定がオフの場合も）。

DPR の最適化により、結果の画像が MaxPix Dynamic Mediaの設定より大きい場合、MaxPix の幅は常に画像の縦横比を維持することで認識されます。

| 要求された画像サイズ | DPR 値 | 配信された画像サイズ |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

DPR 値は、バンドルされた CDN の検出されたクライアント側の値に基づきます。 これらの値は不正確な場合があります。 例：iPhone5 と `dpr=2`、および dpr=3 のiPhone12、両方表示 `dpr=2`. 高解像度デバイスの場合は、送信 `dpr=2` 送信するよりも効果が高い `dpr=1`. ただし、この不正確さを克服する最善の方法は、クライアント側の DPR を使用して 100%の正確な値を得ることです。 また、起動された任意のデバイス (Appleかその他のデバイスかに関わらず ) で機能します。 詳しくは、 [クライアント側デバイスのピクセル比でのスマートイメージングの使用](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## プロパティ

request 属性。 次の場合には効果がありません。 `dpr` がオフの場合、または `dprValue=1`.

## 初期設定

`dpr=off`


## 例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## 関連項目

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [network](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [スマートイメージング](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)