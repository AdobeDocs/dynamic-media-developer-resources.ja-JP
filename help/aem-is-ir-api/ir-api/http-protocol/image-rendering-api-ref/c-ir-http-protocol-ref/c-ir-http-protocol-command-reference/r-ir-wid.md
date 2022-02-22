---
title: wid
description: 返信画像の幅。 返信画像の縦横比を維持しながら、指定した値以上の高さが返信画像になるように、レンダリング画像の拡大/縮小を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a77b71c3-8600-4d7a-ba52-e158cf9668eb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 2%

---

# wid{#wid}

返信画像の幅。 返信画像の縦横比を維持しながら、指定した値以上の高さが返信画像になるように、レンダリング画像の拡大/縮小を指定します。

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>画像の幅（0 より大きい整数） </p></td> 
 </tr> 
</table>

両方の `wid=` および `hei=` が指定され、 `wid`/ `hei` は、画像の縦横比とは異なります。

`wid=` および `hei=` は連携して、サーバーから返される画像のサイズを定義します。 If `scl=` 次の値より後 `wid=` または `hei=` URL 内で、これらのコマンドと `scl=` は、サーバーから返される画像のサイズを定義します。

ただし、 `wid=` または `hei=` 次の値より後 `scl=` URL 内で、訪問者はキャンセルします。 `scl=` および `wid=`/ `hei=` サーバーから返される画像のサイズを定義します。

>[!NOTE]
>
>返信画像のサイズが計算済みまたはデフォルトより大きい場合は、エラーが返されます `attribute::MaxPix`.

## プロパティ {#section-2d067c6d371748e19cb157684700a49d}

リクエスト内の任意の場所で発生する場合があります。 を使用した画像のサイズ変更 `wid=`, `hei=`または `scl=` 応答画像に埋め込まれた印刷解像度の値は変更されません。 次の場合は無視 `scl=` 次の後に発生 `wid=` または `hei=` を指定します。

## 初期設定 {#section-c7c6efa03d864592a3398b6f1de5a0b0}

If `wid=`, `hei=`または `scl=` が指定されていない場合、返信画像は `attribute::DefaultPix`. If `attribute::DefaultPix` が空の場合、返信画像はビネットの表示画像と同じサイズになります。

## 関連項目 {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
