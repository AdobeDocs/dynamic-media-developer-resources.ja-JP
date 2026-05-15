---
title: へい
description: 返信画像の高さ。 画像の縦横比を維持しながら、返信画像の高さが指定された値を超えないように、レンダリングされた画像の拡大・縮小を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
TQID: 'https://experienceleague.adobe.com/-sH3rlYycsZ36DheRgEpMUm6xSuUnY7s-3awUgdfloA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 245
ht-degree: 1%

---

# へい{#hei}

返信画像の高さ。 画像の縦横比を維持しながら、返信画像の高さが指定された値を超えないように、レンダリングされた画像の拡大・縮小を指定します。

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>画像の高さをピクセル単位で返します（0より大きい整数）。 </p></td> 
 </tr> 
</table>

`wid=`と`hei=`の両方が指定され、幅/高さが画像の縦横比と異なる場合、画像はパディングされません。

`wid=`と`hei=`は連携して、サーバーから返される画像のサイズを定義します。 `scl=`がURLの`wid=`または`hei=`の後に来る場合、これらのコマンドはキャンセルされ、`scl=`はサーバーから返される画像のサイズを定義します。

ただし、`wid=`または`hei=`がURLの`scl=`の後に来る場合は、`scl=`と`wid=`/`hei=`をキャンセルして、サーバーから返される画像のサイズを定義します。

>[!NOTE]
>
>計算された返信画像サイズまたはデフォルトの返信画像サイズが`attribute::MaxPix`を超える場合は、エラーが返されます。

## プロパティ {#section-6cbc6acd37c847beab84c896ac25280c}

リクエスト内のどこでも発生する可能性があります。 `wid=`、`hei=`または`scl=`を使用して画像のサイズを変更しても、応答画像に埋め込まれている印刷解像度の値は変更されません。 `scl=`がコマンドシーケンスの`wid=`または`hei=`の後に発生する場合は無視されます。

## 初期設定 {#section-61043f6c1f5d450883ff9e5eafd95955}

`wid=`、`hei=`、または`scl=`が指定されていない場合、返信画像は`attribute::DefaultPix`で定義されたサイズ内に収まるように拡大・縮小されます。 `attribute::DefaultPix`が空の場合、返信画像は周辺光量補正の表示画像と同じサイズになります。

## 関連項目 {#section-7ba51379f1e2421c92d3592d20a37734}

[属性：:DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)、[属性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)、[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)、[scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)、[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
