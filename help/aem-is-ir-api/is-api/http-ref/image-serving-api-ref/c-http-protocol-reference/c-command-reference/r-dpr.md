---
title: dpr
description: Device Pixel Ratio(DPR)&mdash（CSS pixel ratio&mdash とも呼ばれます）は、デバイスの物理ピクセルと論理ピクセルとの関係です。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

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

## プロパティ



## 初期設定

`dpr=off`


## 例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## 関連項目

[network](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [スマートイメージング](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)