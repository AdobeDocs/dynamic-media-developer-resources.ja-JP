---
description: 返信画像の高さ。 返信画像の高さが指定値を超えないように、画像の縦横比を維持したまま、レンダリング画像の拡大縮小を指定します。
seo-description: 返信画像の高さ。 返信画像の高さが指定値を超えないように、画像の縦横比を維持したまま、レンダリング画像の拡大縮小を指定します。
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 616d3306-ccbd-4400-8a94-1ff6f47b802e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# hei{#hei}

返信画像の高さ。 返信画像の高さが指定値を超えないように、画像の縦横比を維持したまま、レンダリング画像の拡大縮小を指定します。

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>返信画像の高さ（ピクセル単位、0より大きい整数）。 </p></td> 
 </tr> 
</table>

との両方を指定し、幅/高さが画 `wid=` 像の縦横比と異な `hei=` る場合、画像はパディングされません。

`wid=` サーバ `hei=` ーから返される画像のサイズを定義する作業を行います。 がURLの後に `scl=` ある `wid=` 場合、ま `hei=` たはURL内にある場合は、これらのコマンドをキャンセルし、サー `scl=` バーから返される画像のサイズを定義します。

ただし、URLの後に `wid=` ある場 `hei=` 合 `scl=` はキャンセルし、サーバーから返される画像のサ `scl=``wid=``hei=` イズを定義します。

>[!NOTE]
>
>計算された返信画像またはデフォルトの返信画像のサイズが次のサイズより大きい場合は、エラーが返されま `attribute::MaxPix`す。

## プロパティ {#section-6cbc6acd37c847beab84c896ac25280c}

リクエスト内の任意の場所で発生する可能性があります。 、、またはを使用して画 `wid=`像のサ `hei=`イズを変 `scl=` 更しても、応答画像に埋め込まれたプリント解像度の値は変更されません。 コマンドシーケ `scl=` ンスの後、ま `wid=` たはその両方で発生 `hei=` する場合は無視されます。

## 初期設定 {#section-61043f6c1f5d450883ff9e5eafd95955}

どちらも指 `wid=`定され `hei=`ていない場合、も `scl=` 指定されていない場合も、で定義されたサイズに合わせて返信画像が拡大・縮小されま `attribute::DefaultPix`す。 が空 `attribute::DefaultPix` の場合、返信画像はビネットのビュー画像と同じサイズになります。

## 関連項目 {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)[,](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)attribute::MaxPix [,](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)wid= [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
