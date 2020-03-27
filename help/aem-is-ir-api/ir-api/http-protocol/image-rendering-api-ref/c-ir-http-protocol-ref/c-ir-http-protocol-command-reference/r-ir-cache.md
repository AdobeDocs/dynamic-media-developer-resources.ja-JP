---
description: キャッシュ制御。 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と、内部のプラットフォームサーバーキャッシュのキャッシュを選択的に無効にできます。
seo-description: キャッシュ制御。 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と、内部のプラットフォームサーバーキャッシュのキャッシュを選択的に無効にできます。
seo-title: キャッシュ
solution: Experience Manager
title: キャッシュ
topic: Scene7 Image Serving - Image Rendering API
uuid: 8af89b67-39d5-43e5-a58d-2cd509a1e373
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# cache{#cache}

キャッシュ制御。 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と、内部のプラットフォームサーバーキャッシュのキャッシュを選択的に無効にできます。

`cache= *`cacheControl`*`

`cache= *`clientControlserverControl`*, *``*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on| off| validate </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>on| off </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>on| off </p></td> 
 </tr> 
</table>

値が1つだけ指定さ *`cacheControl`* れた場合、クライアントキャッシュとサーバーキャッシュの両方に適用されます。

「 `validate`」キーワードを使用すると、テクスチャまたはビネットファイルが変更された後に、キャッシュエントリが自動的に期限切れになるのを待たずに、サーバキャッシュエントリを更新できます。 クライアントのキャッシュは、このコマンドの影響を受けません。

ネストされたリクエストで指定した場合、ネ `cache=on` ストされたリクエストで生成されたイメージの永続的なサーバー側キャッシュを有効にします。 同じネストされたリクエストが同じパラメーターで繰り返し呼び出されると予想される場合にのみ、ネストされたリクエストのキャッシュを有効にするように注意する必要があります。

## プロパティ {#section-0dcbd62e1122400e8c347f408f2d937e}

リクエストの任意の場所で発生する可能性があります。 要求が返信画像を返さない場合は無視されます。 *`clientControl`* は、マテリアルカタログでクライアント側のキャッシュが無効な場合（負の値の場合） `attribute::Expiration` は無視されます。 *`serverControl`* は、サーバーキャッシュが無効な場合は無視さ `PlatformServer::cache.enable`れます()。

## 初期設定 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` (ネストされた/埋め込ま `cache=off` れたリクエストの場合)。

## 関連項目 {#section-2f5853751dab49579e97418fa766bdf9}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)、 [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
