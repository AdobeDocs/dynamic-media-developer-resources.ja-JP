---
title: wid
description: 返信画像の幅。 画像の縦横比を維持しながら、返信画像の高さが指定された値より大きくならないように、レンダリングされた画像の拡大・縮小を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a77b71c3-8600-4d7a-ba52-e158cf9668eb
TQID: 'https://experienceleague.adobe.com/9pR44QWe8G9qjTzNukUN0hEitEoGA47T3gbRUA6-Kpg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 1%

---

# wid{#wid}

返信画像の幅。 画像の縦横比を維持しながら、返信画像の高さが指定された値より大きくならないように、レンダリングされた画像の拡大・縮小を指定します。

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>画像の幅（0より大きい整数）。 </p></td> 
 </tr> 
</table>

`wid=`と`hei=`の両方が指定され、`wid`/`hei`が画像の縦横比と異なる場合、画像はパディングされません。

`wid=`と`hei=`は連携して、サーバーから返される画像のサイズを定義します。 `scl=`がURLの`wid=`または`hei=`の後に来る場合、これらのコマンドはキャンセルされ、`scl=`はサーバーから返される画像のサイズを定義します。

ただし、`wid=`または`hei=`がURLの`scl=`の後に来る場合は、`scl=`と`wid=`/`hei=`をキャンセルして、サーバーから返される画像のサイズを定義します。

>[!NOTE]
>
>計算された返信画像サイズまたはデフォルトの返信画像サイズが`attribute::MaxPix`を超える場合は、エラーが返されます。

## プロパティ {#section-2d067c6d371748e19cb157684700a49d}

リクエスト内のどこでも発生する可能性があります。 `wid=`、`hei=`または`scl=`を使用して画像のサイズを変更しても、応答画像に埋め込まれている印刷解像度の値は変更されません。 `scl=`がコマンドシーケンスの`wid=`または`hei=`の後に発生する場合は無視されます。

## 初期設定 {#section-c7c6efa03d864592a3398b6f1de5a0b0}

`wid=`、`hei=`、または`scl=`が指定されていない場合、返信画像は`attribute::DefaultPix`で定義されたサイズ内に収まるように拡大・縮小されます。 `attribute::DefaultPix`が空の場合、返信画像は周辺光量補正の表示画像と同じサイズになります。

## 関連項目 {#section-450dfc12b1d440e2a3172a69d91db51f}

[属性：:DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)、[属性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)、[hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)、[scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)、[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
