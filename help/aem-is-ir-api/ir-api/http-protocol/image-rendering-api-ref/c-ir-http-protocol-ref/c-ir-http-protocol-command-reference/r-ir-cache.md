---
title: キャッシュ
description: キャッシュ制御。 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と、内部 Platform Server キャッシュでのキャッシュを選択的に無効にすることができます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---

# キャッシュ {#cache}

キャッシュ制御。 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と、内部 Platform Server キャッシュ内のキャッシュを選択的に無効にできます。

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>オン |オフ | validate </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>オン |オフ </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>オン |オフ </p></td> 
 </tr> 
</table>

1 つのみの場合 *`cacheControl`* 値を指定した場合、クライアントキャッシュとサーバーキャッシュの両方に適用されます。

&#39; `validate`&#39;キーワードを使用すると、テクスチャまたはビネットファイルが変更された後に、キャッシュエントリが自動的に期限切れになるのを待たずに、サーバキャッシュエントリを更新できます。 クライアントのキャッシュは、このコマンドの影響を受けません。

ネストされた要求で指定した場合、 `cache=on` ネストされた要求で生成された画像の永続的なサーバー側のキャッシュを有効にします。 同じネストされたリクエストが同じパラメーターを使用して繰り返し呼び出される場合にのみ、ネストされたリクエストのキャッシュを有効にしてください。

## プロパティ {#section-0dcbd62e1122400e8c347f408f2d937e}

リクエストの任意の場所で発生する場合があります。 リクエストが返信画像を返さない場合は無視されます。 プロパティ *`clientControl`* は、クライアント側のキャッシュがマテリアルカタログで無効になっている場合は無視されます ( `attribute::Expiration` は負の値です )。 プロパティ *`serverControl`* は、サーバーキャッシュが無効な場合は無視されます ( `PlatformServer::cache.enable`) をクリックします。

## 初期設定 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` HTTP リクエストの場合、 `cache=off` ネストされた/埋め込み要求用。

## 関連項目 {#section-2f5853751dab49579e97418fa766bdf9}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
