---
title: キャッシュ
description: キャッシュコントロール。 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と内部キャッシュのキャッシュを選択的に無効にするこ  [!DNL Platform Server]  ができます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---

# キャッシュ {#cache}

キャッシュコントロール。 クライアント側キャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と内部 [!DNL Platform Server] キャッシュのキャッシュを選択的に無効にできます。

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>日付： | オフ |検証 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>日付： | オフ </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>日付： | オフ </p></td> 
 </tr> 
</table>

*`cacheControl`* 値を 1 つだけ指定した場合は、クライアントとサーバーの両方のキャッシュに適用されます。

&#39; `validate`&#39; キーワードを使用すると、テクスチャ ファイルまたはビネット ファイルが変更された後にサーバーキャッシュ エントリを更新できます。キャッシュ エントリが自動的に期限切れになるのを待つ必要はありません。 クライアント キャッシュは、このコマンドの影響を受けません。

ネストされたリクエストで指定した場合、`cache=on` は、ネストされたリクエストによって生成された画像のサーバーサイドの永続的なキャッシュを有効にします。 ネストされたリクエストのキャッシュを有効にするのは、同じネストされたリクエストが同じパラメーターで繰り返し呼び出される場合のみにしてください。

## プロパティ {#section-0dcbd62e1122400e8c347f408f2d937e}

は、リクエスト内のどこでも発生する可能性があります。 リクエストが返信画像を返さない場合は無視されます。 材料カタログによってクライアント側のキャッシュが無効になっている場合（*`clientControl`* の値が負の場合）、プロパティ `attribute::Expiration` は無視されます。 サーバーキャッシュが無効になっている場合（*`serverControl`*）、プロパティ `PlatformServer::cache.enable` は無視されます。

## 初期設定 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` HTTP リクエストの場合は、ネストされたリクエストまたは埋め込まれたリクエストの `cache=off`。

## 関連項目 {#section-2f5853751dab49579e97418fa766bdf9}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
