---
description: 拡大・縮小ビュー 最大解像度のビネットを基準に、指定した拡大率でレンダリングイメージを拡大/縮小します。
solution: Experience Manager
title: scl
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---

# scl{#scl}

拡大・縮小ビュー 最大解像度のビネットを基準に、指定した拡大率でレンダリングイメージを拡大/縮小します。

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>逆スケール係数（実数、1.0以上） </p></td> 
 </tr> 
</table>

URL内の`scl=`の後に`wid=`または`hei=`がある場合、これらのコマンドはキャンセルされ、`scl=`はサーバーから返される画像のサイズを定義します。

ただし、URL内の`wid=`または`hei=`が`scl=`の後に来る場合は、`scl=`と`wid=`/ `hei=`をキャンセルして、サーバーから返される画像のサイズを定義します。

>[!NOTE]
>
>計算された返信画像サイズまたはデフォルトの返信画像サイズが`attribute::MaxPix`より大きい場合は、エラーが返されます。

## プロパティ {#section-170458cbd6984bd59a3434431258b20f}

リクエスト内の任意の場所で発生する可能性があります。 コマンドシーケンス内で`wid=`または`hei=`の後に`scl=`が発生した場合は無視されます。

`scl=`で画像のサイズを変更しても、応答画像に埋め込まれた印刷解像度の値は変更されません。

## 初期設定 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

`wid=`、`hei=`、`scl=`のいずれも指定されていない場合、返信画像は`attribute::DefaultPix`で定義されているサイズ内に収まるように拡大/縮小されます。 `attribute::DefaultPix`が空の場合、返信画像はビネットの表示画像と同じサイズになります。

## 関連項目 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) 、 [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)、 [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)、 [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)、 [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
