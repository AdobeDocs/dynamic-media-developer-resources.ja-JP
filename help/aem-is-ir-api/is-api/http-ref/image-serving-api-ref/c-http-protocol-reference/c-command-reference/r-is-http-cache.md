---
description: キャッシュ制御 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と、内部のプラットフォームサーバーキャッシュのキャッシュを選択的に無効にできます。
seo-description: キャッシュ制御 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と、内部のプラットフォームサーバーキャッシュのキャッシュを選択的に無効にできます。
seo-title: キャッシュ
solution: Experience Manager
title: キャッシュ
topic: Scene7 Image Serving - Image Rendering API
uuid: 08f4e4d0-0f7d-48fe-956c-284af97c902e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# cache{#cache}

キャッシュ制御 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と、内部のプラットフォームサーバーキャッシュのキャッシュを選択的に無効にできます。

`cache= *`cacheControl`*`

`cache= *`clientControlserverControl`*, *``*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> cacheControl <span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off|validate|update</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> clientControl <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> serverControl <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

1つのcacheControl値のみが指 ` *`定された場合`*` 、その値はクライアントキャッシュとサーバーキャッシュの両方に適用されます。

このキー `validate` ワードを使用すると、画像ファイルが変更された後にキャッシュエントリを更新でき、キャッシュエントリが自動的に期限切れになるのを待つ必要はありません。 クライアントのキャッシュは、このコマンドの影響を受けません。

このキー `update` ワードを使用して、サーバー側のキャッシュエントリを強制的に更新できます。 これは、ファイル名や関連フォントIDを変更せずにフォントファイルを変更した場合など、キャッシュ検証メカニズムで直接追跡されないリソースが変更された後に役立ちます。

ネストされたリクエストで指定した場合、ネ `cache=on` ストされたリクエストで生成されたイメージの永続的なサーバー側キャッシュを有効にします。 同じネストされたリクエストが同じパラメーターで繰り返し呼び出されると予想される場合にのみ、ネストされたリクエストのキャッシュを有効にするように注意する必要があります。

## プロパティ {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

リクエスト属性。 現在のレイヤー設定に関係なく適用されます。 要求が返信画像を返さない場合は無視されます。 *`clientControl`*は、画像カタログでクライアント側のキャッシュが無効な場合（負の値の場合） `catalog::Expiration` は無視されます。

クライアント側のキャッシュ制御(お `on` よびの `off` み)は、の静的コンテンツリクエストでも使用できま [!DNL /is/content/]す。

## 初期設定 {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` (ネストされた/埋め込まれ `cache=off` たリクエストの場合)静的コン `cache=on` テンツリクエストの場合。

## 関連項目 {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) 、 [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
