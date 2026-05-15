---
title: scl
description: 拡大・縮小ビュー。 フル解像度の周辺光量補正に対して、指定したスケール係数でレンダリングされた画像を拡大・縮小します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
TQID: 'https://experienceleague.adobe.com/HeszuJDuoMh-RTfrnFklpJWqT28PQ74N8GfBe0yZl7k'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 177
ht-degree: 1%

---

# scl{#scl}

拡大・縮小ビュー。 フル解像度の周辺光量補正に対して、指定したスケール係数でレンダリングされた画像を拡大・縮小します。

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>スケール因子の反転（実数、1.0以上） </p></td> 
 </tr> 
</table>

`scl=`がURLの`wid=`または`hei=`の後に来る場合、これらのコマンドはキャンセルされ、`scl=`はサーバーから返される画像のサイズを定義します。

ただし、`wid=`または`hei=`がURLの`scl=`の後に来る場合は、`scl=`と`wid=`/`hei=`をキャンセルして、サーバーから返される画像のサイズを定義します。

>[!NOTE]
>
>計算された返信画像サイズまたはデフォルトの返信画像サイズが`attribute::MaxPix`を超える場合は、エラーが返されます。

## プロパティ {#section-170458cbd6984bd59a3434431258b20f}

リクエスト内のどこでも発生する可能性があります。 `wid=`または`hei=`がコマンドシーケンスの`scl=`の後に発生する場合は無視されます。

`scl=`で画像のサイズを変更しても、応答画像に埋め込まれている印刷解像度の値は変更されません。

## 初期設定 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

`wid=`、`hei=`、または`scl=`が指定されていない場合、返信画像は`attribute::DefaultPix`で定義されたサイズ内に収まるように拡大・縮小されます。 `attribute::DefaultPix`が空の場合、返信画像は周辺光量補正の表示画像と同じサイズになります。

## 関連項目 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)、[hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)、[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)、[属性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)、[属性：:DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
