---
title: hei
description: 返信画像の高さ。 返信画像の高さが指定の値以下になるように、画像の縦横比を維持しながら、レンダリング画像の拡大/縮小を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 2%

---

# hei{#hei}

返信画像の高さ。 返信画像の高さが指定の値以下になるように、画像の縦横比を維持しながら、レンダリング画像の拡大/縮小を指定します。

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>返信画像の高さ（ピクセル単位、0 より大きい整数）。 </p></td> 
 </tr> 
</table>

両方の `wid=` および `hei=` が指定され、幅/高さが画像の縦横比と異なる。

`wid=` および `hei=` は連携して、サーバーから返される画像のサイズを定義します。 If `scl=` 次の値より後 `wid=` または `hei=` URL 内で、これらのコマンドと `scl=` は、サーバーから返される画像のサイズを定義します。

ただし、 `wid=` または `hei=` 次の値より後 `scl=` URL 内で、訪問者はキャンセルします。 `scl=` および `wid=`/ `hei=` サーバーから返される画像のサイズを定義します。

>[!NOTE]
>
>返信画像のサイズが計算済みまたはデフォルトより大きい場合は、エラーが返されます `attribute::MaxPix`.

## プロパティ {#section-6cbc6acd37c847beab84c896ac25280c}

リクエスト内の任意の場所で発生する場合があります。 を使用した画像のサイズ変更 `wid=`, `hei=`または `scl=` 応答画像に埋め込まれた印刷解像度の値は変更されません。 次の場合は無視 `scl=` 次の後に発生 `wid=` および/または `hei=` を指定します。

## 初期設定 {#section-61043f6c1f5d450883ff9e5eafd95955}

If `wid=`, `hei=`または `scl=` が指定されていない場合、返信画像は `attribute::DefaultPix`. If `attribute::DefaultPix` が空の場合、返信画像はビネットの表示画像と同じサイズになります。

## 関連項目 {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
