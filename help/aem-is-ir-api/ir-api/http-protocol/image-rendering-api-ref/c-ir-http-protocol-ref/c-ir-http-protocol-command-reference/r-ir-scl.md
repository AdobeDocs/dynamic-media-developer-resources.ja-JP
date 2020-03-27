---
description: 拡大・縮小表示 最大解像度のビネットを基準にして、指定した拡大率でレンダリングイメージを拡大・縮小します。
seo-description: 拡大・縮小表示 最大解像度のビネットを基準にして、指定した拡大率でレンダリングイメージを拡大・縮小します。
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 04839c44-01b6-4fa2-9eda-bbb0f2822db4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scl{#scl}

拡大・縮小表示 最大解像度のビネットを基準にして、指定した拡大率でレンダリングイメージを拡大・縮小します。

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span></span> </p></td> 
  <td class="stentry"> <p>逆スケール係数（実数、1.0以上） </p></td> 
 </tr> 
</table>

がURLの後に `scl=` ある `wid=` 場合、ま `hei=` たはURL内にある場合は、これらのコマンドをキャンセルし、サー `scl=` バーから返される画像のサイズを定義します。

ただし、URLの後に `wid=` ある場 `hei=` 合 `scl=` はキャンセルし、サーバーから返される画像のサ `scl=``wid=``hei=` イズを定義します。

>[!NOTE]
>
>計算された返信画像またはデフォルトの返信画像のサイズが次のサイズより大きい場合は、エラーが返されま `attribute::MaxPix`す。

## プロパティ {#section-170458cbd6984bd59a3434431258b20f}

リクエスト内の任意の場所で発生する可能性があります。 コマンドシーケ `wid=` ンスの `hei=` 後にまたはが `scl=` 発生した場合は無視されます。

で画像のサイズを変更し `scl=` ても、応答画像に埋め込まれたプリント解像度の値は変更されません。

## 初期設定 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

どちらも指 `wid=`定され `hei=` ていな `scl=` い場合、または指定されていない場合、返信画像はで定義されたサイズに合わせて拡大・縮小されま `attribute::DefaultPix`す。 が空 `attribute::DefaultPix` の場合、返信画像はビネットのビュー画像と同じサイズになります。

## 関連項目 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)[, attribute:DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
