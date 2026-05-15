---
title: glossmap
description: 光沢マップ画像： 繰り返し可能なテクスチャ、壁紙/境界線、デカールの光沢度をピクセル単位で制御します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
TQID: 'https://experienceleague.adobe.com/H-Ip9cbtirNaAhfQwr1lj6T3hYdiD1uG-NdQvCJB1v4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 2%

---

# glossmap {#glossmap}

光沢マップ画像： 繰り返し可能なテクスチャ、壁紙/境界線、デカールの光沢度をピクセル単位で制御します。

`glossmap={ *`glossMapFile`*| *`embeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&lbrace;'is&brace;'<span class="varname"> isReq</span>'&rbrace;'&brace;'&lbrace;'<span class="varname"> foreignReq</span>'&rbrace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>光沢マップ画像ファイル（グレースケール）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">はReq</span> </span> </p></td> 
  <td class="stentry"> <p>Image Serverへのリクエスト。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq </span> </span> </p></td> 
  <td class="stentry"> <p>外部サーバーへのリクエスト。 </p></td> 
 </tr> 
</table>

メタリックペイントエフェクト、ダイカット箔の壁紙や境界線、メタリックスレッドファブリックなどの素材に適用できます。

光沢マップ画像は8 ビットのグレースケールで、`src=`で指定されたプライマリ画像と同じサイズである必要があります。 詳しくは、[`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)の説明を参照してください。

## プロパティ {#section-26375672d69849be9b026cc93c3bc558}

マテリアル属性： 繰り返し可能なテクスチャ、壁紙、境界線、デカールでサポートされています。 単色、キャビネット、および窓のカバー材料によって無視されます。 詳しくは、[`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)を参照してください。

## 初期設定 {#section-d9ac031fb2f94482ac3fe2283d7cb168}

なし

## 関連項目 {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)、[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
