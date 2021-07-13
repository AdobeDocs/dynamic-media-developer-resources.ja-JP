---
description: 光沢マップ画像。 繰り返し可能なテクスチャ、壁紙/境界線、デカールの光沢をピクセル単位で制御できます。
solution: Experience Manager
title: 用語集
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 3%

---

# 用語集{#glossmap}

光沢マップ画像。 繰り返し可能なテクスチャ、壁紙/境界線、デカールの光沢をピクセル単位で制御できます。

`glossmap={ *``*| *`glossMapFileembeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;'<span class="varname"> foreignReq</span>'&amp;rbrace;'  </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>光沢マップ画像ファイル（グレースケール） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Image Serverに対する要求。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq  </span> </span> </p></td> 
  <td class="stentry"> <p>外部サーバーにリクエストします。 </p></td> 
 </tr> 
</table>

金属塗装効果、ダイカット箔の壁紙や縁取り、金属糸織物などの材料に適用できます。

グロスマップ画像は8ビットのグレースケールで、`src=`で指定したプライマリ画像と同じサイズである必要があります。 詳しくは、 [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)の説明を参照してください。

## プロパティ {#section-26375672d69849be9b026cc93c3bc558}

マテリアル属性。 繰り返し可能なテクスチャ、壁紙と境界線、およびデカールでサポートされています。 ソリッドカラー、キャビネット、窓のカバーマテリアルでは無視されます。 詳しくは、 [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)を参照してください。

## 初期設定 {#section-d9ac031fb2f94482ac3fe2283d7cb168}

なし

## 関連項目 {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)、 [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
