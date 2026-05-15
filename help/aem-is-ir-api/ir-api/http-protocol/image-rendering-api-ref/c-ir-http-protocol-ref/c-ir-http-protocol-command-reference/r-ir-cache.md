---
title: キャッシュ
description: キャッシュ制御： クライアントサイドのキャッシュ （ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）および内部 [!DNL Platform Server]  キャッシュのキャッシュを選択的に無効にできます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
TQID: 'https://experienceleague.adobe.com/xq-8hE9RB7I-CMb-yguhBcEttxTv6IRRHWzh0lDvn6E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 1%

---

# キャッシュ {#cache}

キャッシュ制御： クライアント側のキャッシュ （ブラウザー、プロキシ サーバー、ネットワーク キャッシュ システム）と内部[!DNL Platform Server] キャッシュのキャッシュを選択的に無効にできます。

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>オン | オフ |検証 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>オン | オフ </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>オン | オフ </p></td> 
 </tr> 
</table>

1つの&#x200B;*`cacheControl`*&#x200B;値のみを指定した場合、クライアントとサーバーの両方のキャッシュに適用されます。

&#39;`validate`&#39; キーワードを使用すると、テクスチャ ファイルまたは周辺光量補正ファイルが変更された後、キャッシュ エントリが自動的に期限切れになるまで待たずに、サーバーのキャッシュ エントリを更新できます。 クライアントのキャッシュは、このコマンドの影響を受けません。

ネストされたリクエストで指定された場合、`cache=on`は、ネストされたリクエストによって生成された画像の永続的なサーバーサイドキャッシュを有効にします。 ネストされたリクエストのキャッシュは、同じネストされたリクエストが同じパラメーターで繰り返し呼び出される場合にのみ有効にしてください。

## プロパティ {#section-0dcbd62e1122400e8c347f408f2d937e}

リクエスト内のどこでも発生する可能性があります。 リクエストが返信画像を返さない場合は無視されます。 マテリアル カタログによってクライアント側のキャッシュが無効になっている場合、プロパティ *`clientControl`*&#x200B;は無視されます（`attribute::Expiration`に負の値がある場合）。 サーバーのキャッシュが無効になっている場合（`PlatformServer::cache.enable`）、プロパティ *`serverControl`*&#x200B;は無視されます。

## 初期設定 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

HTTP リクエストの`cache=on,on`、ネストされた/埋め込まれたリクエストの`cache=off`。

## 関連項目 {#section-2f5853751dab49579e97418fa766bdf9}

[&#x200B; カタログ：：有効期限](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)、[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
