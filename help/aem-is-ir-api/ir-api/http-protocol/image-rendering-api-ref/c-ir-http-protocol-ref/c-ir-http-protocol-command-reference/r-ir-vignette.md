---
title: ビネット
description: 周辺光量補正ファイル リクエストに使用する周辺光量補正を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8419d68d-7579-4e62-abbd-7dc0a736ae23
TQID: 'https://experienceleague.adobe.com/tEmCtPpiV1Y61y8R2kji-iBDwWCP3obkDR-K23AaewE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 119
ht-degree: 3%

---

# ビネット{#vignette}

周辺光量補正ファイル リクエストに使用する周辺光量補正を指定します。

`vignette=[ *`catId`*/] *`recId`*|[catId/] *` ファイル `*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>マテリアルカタログ ID （<span class="codeph">属性：:RootId</span>に一致）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>周辺光量補正ID （<span class="codeph"> ビネット：:Id</span>に一致）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ファイル </span> </p></td> 
  <td class="stentry"> <p>ビネットファイルの相対パスと名前。 </p></td> 
 </tr> 
</table>

周辺光量補正マップエントリまたは周辺光量補正ファイルを指定できます。 リモート URLは許可されていません。

`vignette=`は、リクエスト URL パスで周辺光量補正を指定する代わりに使用できます。 テンプレート内の変数を使用して周辺光量補正を指定するために使用します。

*`catId`*&#x200B;が指定されていない場合は、セッションカタログが使用されます。

## プロパティ {#section-f58661fc78d7496e8e3d0fb98b945c4b}

リクエスト内のどこでも発生する可能性があります。 リクエスト URL パスで指定された周辺光量補正を上書きします。

## 初期設定 {#section-db0618d48bc84dc8abcc989550349ccc}

なし

## 関連項目 {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[&#x200B; マテリアルカタログ &#x200B;](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)、[&#x200B; カスタム変数](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
