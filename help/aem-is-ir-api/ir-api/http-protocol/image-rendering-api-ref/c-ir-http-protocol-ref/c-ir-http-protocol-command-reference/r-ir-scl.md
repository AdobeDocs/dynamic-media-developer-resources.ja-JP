---
description: スケール表示 最大解像度のビネットを基準にして、指定した拡大率でレンダリング画像を拡大縮小します。
seo-description: スケール表示 最大解像度のビネットを基準にして、指定した拡大率でレンダリング画像を拡大縮小します。
seo-title: scl
solution: Experience Manager
title: scl
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 04839c44-01b6-4fa2-9eda-bbb0f2822db4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---


# scl{#scl}

スケール表示 最大解像度のビネットを基準にして、指定した拡大率でレンダリング画像を拡大縮小します。

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>逆スケール係数（実数、1.0以上） </p></td> 
 </tr> 
</table>

URL内で`scl=`が`wid=`または`hei=`の後に来る場合、はこれらのコマンドをキャンセルし、`scl=`はサーバーから返される画像のサイズを定義します。

ただし、URL内で`wid=`または`hei=`が`scl=`の後に来る場合、`scl=`と`wid=`/ `hei=`はキャンセルされ、サーバから返される画像のサイズを定義します。

>[!NOTE]
>
>計算済みまたはデフォルトの返信画像のサイズが`attribute::MaxPix`より大きい場合は、エラーが返されます。

## プロパティ {#section-170458cbd6984bd59a3434431258b20f}

リクエスト内の任意の場所で発生する可能性があります。 コマンドシーケンスで`wid=`または`hei=`が`scl=`の後に発生した場合は無視されます。

`scl=`を使用して画像をサイズ変更しても、応答画像に埋め込まれている印刷解像度の値は変更されません。

## 初期設定 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

`wid=`、`hei=`、`scl=`のいずれも指定されていない場合、`attribute::DefaultPix`で定義されているサイズに合わせて返信画像のサイズが調整されます。 `attribute::DefaultPix`が空の場合、返信画像はビネットの表示画像と同じサイズになります。

## 関連項目 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3),  [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657) [, attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
