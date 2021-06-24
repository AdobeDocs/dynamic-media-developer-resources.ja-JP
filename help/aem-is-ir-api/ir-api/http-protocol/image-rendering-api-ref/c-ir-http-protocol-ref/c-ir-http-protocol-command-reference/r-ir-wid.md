---
description: 返信画像の幅。 画像の縦横比を維持しながら、返信画像の高さが指定の値以下になるように、レンダリング画像の拡大/縮小を指定します。
solution: Experience Manager
title: wid
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: a77b71c3-8600-4d7a-ba52-e158cf9668eb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# wid{#wid}

返信画像の幅。 画像の縦横比を維持しながら、返信画像の高さが指定の値以下になるように、レンダリング画像の拡大/縮小を指定します。

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>画像の幅（ピクセル単位、0より大きい整数） </p></td> 
 </tr> 
</table>

`wid=`と`hei=`の両方が指定され、`wid`/`hei`が画像の縦横比と異なる場合、画像はパディングされません。

`wid=` とは `hei=` 連携して、サーバーから返される画像のサイズを定義します。URL内の`scl=`の後に`wid=`または`hei=`がある場合、これらのコマンドはキャンセルされ、`scl=`はサーバーから返される画像のサイズを定義します。

ただし、URL内の`wid=`または`hei=`が`scl=`の後に来る場合は、`scl=`と`wid=`/ `hei=`をキャンセルして、サーバーから返される画像のサイズを定義します。

>[!NOTE]
>
>計算された返信画像サイズまたはデフォルトの返信画像サイズが`attribute::MaxPix`より大きい場合は、エラーが返されます。

## プロパティ {#section-2d067c6d371748e19cb157684700a49d}

リクエスト内の任意の場所で発生する可能性があります。 `wid=`、`hei=`または`scl=`を使用して画像のサイズを変更しても、応答画像に埋め込まれた印刷解像度の値は変更されません。 コマンドシーケンス内で`wid=`または`hei=`の後に`scl=`が発生した場合は無視されます。

## 初期設定 {#section-c7c6efa03d864592a3398b6f1de5a0b0}

`wid=`、`hei=`、`scl=`のいずれも指定されていない場合、返信画像は`attribute::DefaultPix`で定義されているサイズ内に収まるように拡大/縮小されます。 `attribute::DefaultPix`が空の場合、返信画像はビネットの表示画像と同じサイズになります。

## 関連項目 {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) 、 [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)、 [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)、 [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)、 [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
