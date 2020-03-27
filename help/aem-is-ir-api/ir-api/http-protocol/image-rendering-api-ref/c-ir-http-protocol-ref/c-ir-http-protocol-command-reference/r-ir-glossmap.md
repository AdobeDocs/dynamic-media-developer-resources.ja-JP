---
description: 光沢マップ画像 繰り返し可能なテクスチャ、壁紙/境界、デカールの光沢をピクセル単位で制御します。
seo-description: 光沢マップ画像 繰り返し可能なテクスチャ、壁紙/境界、デカールの光沢をピクセル単位で制御します。
seo-title: 光沢マップ
solution: Experience Manager
title: 光沢マップ
topic: Scene7 Image Serving - Image Rendering API
uuid: f137d362-74a1-45b3-9274-a3a2d6cf5db0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 光沢マップ{#glossmap}

光沢マップ画像 繰り返し可能なテクスチャ、壁紙/境界、デカールの光沢をピクセル単位で制御します。

`glossmap={ *`glossMapFileembeddedReq`*| *``*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{'is{'<span class="varname"> isReq</span>'}'}|{'{'foreignReq<span class="varname"></span>'}' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> glossMapFile <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>光沢マップ画像ファイル（グレースケール） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span></span> </p></td> 
  <td class="stentry"> <p>Image Serverに対する要求。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq </span></span> </p></td> 
  <td class="stentry"> <p>外部サーバーにリクエストします。 </p></td> 
 </tr> 
</table>

金属塗装効果、ダイカットフォイルの壁紙と境界、金属糸織物などの材料に適用できます。

光沢マップ画像は、8ビットのグレースケールで、で指定したプライマリ画像と同じサイズである必要がありま `src=`す。 詳しくは、の説明を参 [ 照してく `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ださい。

## プロパティ {#section-26375672d69849be9b026cc93c3bc558}

マテリアル属性。 繰り返し可能なテクスチャ、壁紙と境界線、およびデカールでサポートされています。 べた塗り、キャビネット、窓のカバリングマテリアルでは無視されます。 See [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) for additional information.

## 初期設定 {#section-d9ac031fb2f94482ac3fe2283d7cb168}

なし

## 関連項目 {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
