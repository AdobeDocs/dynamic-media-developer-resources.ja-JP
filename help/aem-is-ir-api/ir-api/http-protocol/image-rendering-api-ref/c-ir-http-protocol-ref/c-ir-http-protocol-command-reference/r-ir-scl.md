---
title: scl
description: ビューを拡大/縮小します。 フル解像度のビネットを基準にして、指定した尺度係数でレンダリング イメージの尺度を変更します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 1%

---

# scl{#scl}

ビューを拡大/縮小します。 フル解像度のビネットを基準にして、指定した尺度係数でレンダリング イメージの尺度を変更します。

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>逆尺度係数（実数、1.0 以上） </p></td> 
 </tr> 
</table>

URL の `wid=` または `hei=` の後に `scl=` がある場合、コマンドはキャンセルされ、`scl=` はサーバーによって返される画像のサイズが定義されます。

ただし、URL の `wid=` または `hei=` が `scl=` の後にある場合は、`scl=` および `wid=`/ `hei=` をキャンセルして、サーバーから返される画像のサイズを定義します。

>[!NOTE]
>
>計算済みまたはデフォルトの返信画像のサイズが `attribute::MaxPix` を超える場合はエラーが返されます。

## プロパティ {#section-170458cbd6984bd59a3434431258b20f}

は、リクエスト内のどこでも発生する可能性があります。 コマンド シーケンスの `scl=` の後に `wid=` または `hei=` が発生する場合、無視されます。

`scl=` を使用して画像のサイズを変更しても、応答画像に埋め込まれている印刷解像度の値は変更されません。

## 初期設定 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

`wid=`、`hei=`、`scl=` のいずれかが指定されていない場合、返信画像は `attribute::DefaultPix` で定義されたサイズに収まるように拡大縮小されます。 `attribute::DefaultPix` が空の場合、返信画像はビネットのビュー画像と同じサイズになります。

## 関連項目 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)、[hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)、[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)、[attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)、[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
