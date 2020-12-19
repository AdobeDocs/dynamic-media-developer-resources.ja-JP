---
description: 返信画像の高さ。 返信画像の高さが指定した値を超えないように、画像の縦横比を維持しながら、レンダリング画像の拡大縮小を指定します。
seo-description: 返信画像の高さ。 返信画像の高さが指定した値を超えないように、画像の縦横比を維持しながら、レンダリング画像の拡大縮小を指定します。
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 616d3306-ccbd-4400-8a94-1ff6f47b802e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---


# hei{#hei}

返信画像の高さ。 返信画像の高さが指定した値を超えないように、画像の縦横比を維持しながら、レンダリング画像の拡大縮小を指定します。

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>返信画像の高さ（ピクセル単位、0より大きい整数） </p></td> 
 </tr> 
</table>

`wid=`と`hei=`の両方を指定し、幅/高さが画像の縦横比と異なる場合、画像は埋め込まれません。

`wid=` サーバから返される画像のサイズを定義する作業を `hei=` 一緒に行います。URL内で`scl=`が`wid=`または`hei=`の後に来る場合、&lt;a0/>はこれらのコマンドをキャンセルし、`scl=`はサーバーから返される画像のサイズを定義します。

ただし、URL内で`wid=`または`hei=`が`scl=`の後に来る場合、`scl=`と`wid=`/ `hei=`はキャンセルされ、サーバから返される画像のサイズを定義します。

>[!NOTE]
>
>計算済みまたはデフォルトの返信画像のサイズが`attribute::MaxPix`より大きい場合は、エラーが返されます。

## プロパティ {#section-6cbc6acd37c847beab84c896ac25280c}

リクエスト内の任意の場所で発生する可能性があります。 `wid=`、`hei=`、または`scl=`を使用して画像のサイズを変更しても、応答画像に埋め込まれている印刷解像度の値は変更されません。 コマンドシーケンスで`scl=`や`hei=`の後に&lt;a0/>がある場合は無視されます。`wid=`

## 初期設定 {#section-61043f6c1f5d450883ff9e5eafd95955}

`wid=`、`hei=`、`scl=`のいずれも指定されていない場合、`attribute::DefaultPix`で定義されているサイズに合わせて返信画像のサイズが調整されます。 `attribute::DefaultPix`が空の場合、返信画像はビネットの表示画像と同じサイズになります。

## 関連項目 {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)scl= [, ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29) [lesMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
