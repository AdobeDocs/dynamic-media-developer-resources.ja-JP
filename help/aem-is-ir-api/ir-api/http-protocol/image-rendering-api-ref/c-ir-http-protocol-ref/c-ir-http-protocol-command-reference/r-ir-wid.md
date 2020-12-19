---
description: 返信画像の幅。 返信画像の高さが指定値を超えないように、画像の縦横比を維持したまま、レンダリング画像の拡大縮小を指定します。
seo-description: 返信画像の幅。 返信画像の高さが指定値を超えないように、画像の縦横比を維持したまま、レンダリング画像の拡大縮小を指定します。
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a58a5d2-43ac-44db-9959-ba166006b7df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 2%

---


# wid{#wid}

返信画像の幅。 返信画像の高さが指定値を超えないように、画像の縦横比を維持したまま、レンダリング画像の拡大縮小を指定します。

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>画像の幅（ピクセル単位、0より大きい整数） </p></td> 
 </tr> 
</table>

`wid=`と`hei=`の両方を指定し、`wid`/ `hei`が画像の縦横比と異なる場合、画像は埋め込まれません。

`wid=` サーバから返される画像のサイズを定義する作業を `hei=` 一緒に行います。URL内で`scl=`が`wid=`または`hei=`の後に来る場合、&lt;a0/>はこれらのコマンドをキャンセルし、`scl=`はサーバーから返される画像のサイズを定義します。

ただし、URL内で`wid=`または`hei=`が`scl=`の後に来る場合、`scl=`と`wid=`/ `hei=`はキャンセルされ、サーバから返される画像のサイズを定義します。

>[!NOTE]
>
>計算済みまたはデフォルトの返信画像のサイズが`attribute::MaxPix`より大きい場合は、エラーが返されます。

## プロパティ {#section-2d067c6d371748e19cb157684700a49d}

リクエスト内の任意の場所で発生する可能性があります。 `wid=`、`hei=`、または`scl=`を使用して画像のサイズを変更しても、応答画像に埋め込まれている印刷解像度の値は変更されません。 コマンドシーケンスで`scl=`または`hei=`の後に&lt;a0/>がある場合は無視されます。`wid=`

## 初期設定 {#section-c7c6efa03d864592a3398b6f1de5a0b0}

`wid=`、`hei=`、`scl=`のいずれも指定されていない場合、`attribute::DefaultPix`で定義されているサイズに合わせて返信画像のサイズが調整されます。 `attribute::DefaultPix`が空の場合、返信画像はビネットの表示画像と同じサイズになります。

## 関連項目 {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)scl= [, Mode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [DefaultPix, attribute::MaxPix,](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
