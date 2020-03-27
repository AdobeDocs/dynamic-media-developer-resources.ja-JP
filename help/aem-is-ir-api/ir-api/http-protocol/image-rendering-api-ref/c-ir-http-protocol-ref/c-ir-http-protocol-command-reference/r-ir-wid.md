---
description: 返信画像の幅。 返信画像の縦横比を維持しながら、指定した値よりも高さが大きくならないように、レンダリング画像の拡大/縮小を指定します。
seo-description: 返信画像の幅。 返信画像の縦横比を維持しながら、指定した値よりも高さが大きくならないように、レンダリング画像の拡大/縮小を指定します。
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a58a5d2-43ac-44db-9959-ba166006b7df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# wid{#wid}

返信画像の幅。 返信画像の縦横比を維持しながら、指定した値よりも高さが大きくならないように、レンダリング画像の拡大/縮小を指定します。

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>画像の幅（ピクセル単位、整数値0より大きい）。 </p></td> 
 </tr> 
</table>

との両方を指定し、 `wid=` / `hei=` が画像の縦横比と `wid`異なる場合、画 `hei` 像はパディングされません。

`wid=` サーバ `hei=` ーから返される画像のサイズを定義する作業を行います。 がURLの後に `scl=` ある `wid=` 場合、ま `hei=` たはURL内にある場合は、これらのコマンドをキャンセルし、サー `scl=` バーから返される画像のサイズを定義します。

ただし、URLの後に `wid=` ある場 `hei=` 合 `scl=` はキャンセルし、サーバーから返される画像のサ `scl=``wid=``hei=` イズを定義します。

>[!NOTE]
>
>計算された返信画像またはデフォルトの返信画像のサイズが次のサイズより大きい場合は、エラーが返されま `attribute::MaxPix`す。

## プロパティ {#section-2d067c6d371748e19cb157684700a49d}

リクエスト内の任意の場所で発生する可能性があります。 、、またはを使用して画 `wid=`像のサ `hei=`イズを変 `scl=` 更しても、応答画像に埋め込まれたプリント解像度の値は変更されません。 コマンドシーケ `scl=` ンスの後ま `wid=` たはで `hei=` 発生した場合は無視されます。

## 初期設定 {#section-c7c6efa03d864592a3398b6f1de5a0b0}

どちらも指 `wid=`定され `hei=`ていない場合、も `scl=` 指定されていない場合も、で定義されたサイズに合わせて返信画像が拡大・縮小されま `attribute::DefaultPix`す。 が空 `attribute::DefaultPix` の場合、返信画像はビネットのビュー画像と同じサイズになります。

## 関連項目 {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)[,](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)attribute::MaxPix [,](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)hei= [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
