---
title: ビネット
description: ビネットファイル。 リクエストに使用するビネットを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8419d68d-7579-4e62-abbd-7dc0a736ae23
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# ビネット{#vignette}

ビネットファイル。 リクエストに使用するビネットを指定します。

`vignette=[ *`catId`*/] *`recId`*|[catId/] *`file`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>マテリアル カタログ ID （<span class="codeph"> 属性：:RootId</span> と一致） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>ビネット ID （ビネット：:Id<span class="codeph"></span> 一致）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ファイル </span> </p></td> 
  <td class="stentry"> <p>ビネットファイルの相対パスと名前。 </p></td> 
 </tr> 
</table>

ビネットマップエントリまたはビネットファイルを指定できます。 リモート URL は許可されていません。

`vignette=` リクエスト URL パスにビネットを指定する代わりに使用できます。 テンプレート内の変数を使用してビネットを指定する場合に使用します。

*`catId`* を指定しない場合、セッションカタログが使用されます。

## プロパティ {#section-f58661fc78d7496e8e3d0fb98b945c4b}

は、リクエスト内のどこでも発生する可能性があります。 リクエスト URL パスで指定されたビネットを上書きします。

## 初期設定 {#section-db0618d48bc84dc8abcc989550349ccc}

なし

## 関連項目 {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[ マテリアル カタログ ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)、[ カスタム変数 ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
