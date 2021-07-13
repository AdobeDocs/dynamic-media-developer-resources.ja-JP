---
description: キャッシュ制御 内部のPlatform Serverキャッシュで、クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）とキャッシュを選択的に無効にできます。
solution: Experience Manager
title: キャッシュ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---

# キャッシュ{#cache}

キャッシュ制御 内部のPlatform Serverキャッシュで、クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）とキャッシュを選択的に無効にできます。

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on | off | validate </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl  </span> </p> </td> 
  <td class="stentry"> <p>on | off </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl  </span> </p></td> 
  <td class="stentry"> <p>on | off </p></td> 
 </tr> 
</table>

*`cacheControl`*&#x200B;値を1つだけ指定した場合、クライアントキャッシュとサーバーキャッシュの両方に適用されます。

「 `validate` 」キーワードを使用すると、テクスチャやビネットファイルが変更された後にサーバーのキャッシュエントリを更新できます。キャッシュエントリが自動的に期限切れになるのを待つ必要はありません。 クライアントのキャッシュは、このコマンドの影響を受けません。

ネストされたリクエストで指定した場合、 `cache=on`は、ネストされたリクエストによって生成されたイメージのサーバー側の永続的なキャッシュを有効にします。 同じネストされたリクエストが、まったく同じパラメーターを使用して繰り返し呼び出される場合にのみ、ネストされたリクエストのキャッシュを有効にするように注意する必要があります。

## プロパティ {#section-0dcbd62e1122400e8c347f408f2d937e}

リクエストの任意の場所で発生する可能性があります。 要求が返信イメージを返さない場合は無視されます。 *`clientControl`* は、クライアント側のキャッシュがマテリアルカタログで無効になっている場合(が負の値の `attribute::Expiration` 場合)は無視されます。*`serverControl`* は、サーバーキャッシュが無効な場合(  `PlatformServer::cache.enable`)は無視されます。

## 初期設定 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` HTTPリクエスト用、ネストさ `cache=off` れた/埋め込みリクエスト用。

## 関連項目 {#section-2f5853751dab49579e97418fa766bdf9}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)、 [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
