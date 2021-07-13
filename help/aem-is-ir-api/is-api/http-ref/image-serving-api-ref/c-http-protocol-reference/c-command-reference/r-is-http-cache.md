---
description: キャッシュ制御 内部のPlatform Serverキャッシュで、クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）とキャッシュを選択的に無効にできます。
solution: Experience Manager
title: キャッシュ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# キャッシュ{#cache}

キャッシュ制御 内部のPlatform Serverキャッシュで、クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）とキャッシュを選択的に無効にできます。

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off|validate|update</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

`*`cacheControl`*`値を1つだけ指定した場合、その値はクライアントキャッシュとサーバーキャッシュの両方に適用されます。

`validate`キーワードを使用すると、画像ファイルが変更された後にキャッシュエントリを更新できます。キャッシュエントリが自動的に期限切れになるのを待つ必要はありません。 クライアントのキャッシュは、このコマンドの影響を受けません。

`update`キーワードを使用すると、サーバー側のキャッシュエントリを強制的に更新できます。 これは、ファイル名や関連フォントIDを変更せずにフォントファイルを変更した場合など、キャッシュ検証メカニズムで直接追跡されないリソースを変更した後に役立ちます。

ネストされたリクエストで指定した場合、 `cache=on`は、ネストされたリクエストによって生成されたイメージのサーバー側の永続的なキャッシュを有効にします。 同じネストされたリクエストが、まったく同じパラメーターを使用して繰り返し呼び出される場合にのみ、ネストされたリクエストのキャッシュを有効にするように注意する必要があります。

## プロパティ {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

リクエスト属性。 現在の画層設定に関係なく適用されます。 要求が返信イメージを返さない場合は無視されます。 画像カタログでクライアント側のキャッシュが無効な場合（`catalog::Expiration`の値が負の場合）、*`clientControl`*は無視されます。

クライアント側のキャッシュ制御（`on`および`off`のみ）も、[!DNL /is/content/]での静的コンテンツリクエストで使用できます。

## 初期設定 {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` HTTPリクエスト用、ネストさ `cache=off` れた/埋め込みリクエスト用、静的コンテ `cache=on` ンツリクエスト用。

## 関連項目 {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) 、 [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
