---
description: ビネットファイル この要求に使用するビネットを指定します。
seo-description: ビネットファイル この要求に使用するビネットを指定します。
seo-title: ビネット
solution: Experience Manager
title: ビネット
topic: Scene7 Image Serving - Image Rendering API
uuid: 8bba4ad4-bd55-4c55-8ebf-585371cf33f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# vignette{#vignette}

ビネットファイル この要求に使用するビネットを指定します。

`vignette=[ *`catIdrecIdfile`*/] *``*|[catId/] *``*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>マテリアルカタログID( <span class="codeph"> attribute::RootIdに一致</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>ビネットID(ビネット：:Id <span class="codeph"> に一致</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ファイル</span> </p></td> 
  <td class="stentry"> <p>ビネットの相対ファイルパスとファイル名。 </p></td> 
 </tr> 
</table>

ビネットマップエントリまたはビネットファイルを指定できます。 リモートURLは許可されません。

`vignette=` は、要求URLパスでビネットを指定する代わりに使用できます。 主に、テンプレート内の変数を使用してビネットを指定するために使用されます。

指定し *`catId`* なかった場合、セッションカタログが使用されます。

## プロパティ {#section-f58661fc78d7496e8e3d0fb98b945c4b}

リクエスト内の任意の場所で発生する可能性があります。 要求URLパスで指定されたビネットを上書きします。

## 初期設定 {#section-db0618d48bc84dc8abcc989550349ccc}

なし

## 関連項目 {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[マテリアルカタログ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)、カ [スタム変数](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
