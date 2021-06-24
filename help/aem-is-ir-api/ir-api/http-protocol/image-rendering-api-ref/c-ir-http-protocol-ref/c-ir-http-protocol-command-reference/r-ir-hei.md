---
description: 返信画像の高さ。 画像の縦横比を維持しながら、返信画像の高さが指定の値以下になるように、レンダリング画像の拡大/縮小を指定します。
solution: Experience Manager
title: hei
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---

# hei{#hei}

返信画像の高さ。 画像の縦横比を維持しながら、返信画像の高さが指定の値以下になるように、レンダリング画像の拡大/縮小を指定します。

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>返信画像の高さ（ピクセル単位、0より大きい整数）。 </p></td> 
 </tr> 
</table>

`wid=`と`hei=`の両方が指定され、幅/高さが画像の縦横比と異なる場合、画像はパディングされません。

`wid=` とは `hei=` 連携して、サーバーから返される画像のサイズを定義します。URL内の`scl=`の後に`wid=`または`hei=`がある場合、これらのコマンドはキャンセルされ、`scl=`はサーバーから返される画像のサイズを定義します。

ただし、URL内の`wid=`または`hei=`が`scl=`の後に来る場合は、`scl=`と`wid=`/ `hei=`をキャンセルして、サーバーから返される画像のサイズを定義します。

>[!NOTE]
>
>計算された返信画像サイズまたはデフォルトの返信画像サイズが`attribute::MaxPix`より大きい場合は、エラーが返されます。

## プロパティ {#section-6cbc6acd37c847beab84c896ac25280c}

リクエスト内の任意の場所で発生する可能性があります。 `wid=`、`hei=`または`scl=`を使用して画像のサイズを変更しても、応答画像に埋め込まれた印刷解像度の値は変更されません。 コマンドシーケンス内で`wid=`や`hei=`の後に`scl=`が発生した場合は無視されます。

## 初期設定 {#section-61043f6c1f5d450883ff9e5eafd95955}

`wid=`、`hei=`、`scl=`のいずれも指定されていない場合、返信画像は`attribute::DefaultPix`で定義されているサイズ内に収まるように拡大/縮小されます。 `attribute::DefaultPix`が空の場合、返信画像はビネットの表示画像と同じサイズになります。

## 関連項目 {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) 、 [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)、 [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)、 [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)、 [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
