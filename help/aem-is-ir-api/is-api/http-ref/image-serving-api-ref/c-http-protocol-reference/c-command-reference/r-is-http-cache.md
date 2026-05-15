---
title: キャッシュ
description: キャッシュ制御： クライアントサイドのキャッシュ （ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）および内部 [!DNL Platform Server]  キャッシュのキャッシュを選択的に無効にできます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
TQID: 'https://experienceleague.adobe.com/-52nQ085AMsFuqDNv8JdEtXjwYFtIr3aXfHlrERSDoI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 1%

---

# キャッシュ{#cache}

キャッシュ制御： クライアント側のキャッシュ （ブラウザー、プロキシ サーバー、ネットワーク キャッシュ システム）および内部[!DNL Platform Server] キャッシュのキャッシュを選択的に無効にできます。

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

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

`*`cacheControl`*`値が1つだけ指定されている場合は、クライアントとサーバーの両方のキャッシュに適用されます。

`validate` キーワードを使用すると、画像ファイルが変更された後にキャッシュエントリを更新できます。キャッシュエントリが自動的に期限切れになるまで待つ必要はありません。 クライアントのキャッシュは、このコマンドの影響を受けません。

`update` キーワードを使用すると、サーバーサイドのキャッシュエントリを強制的に更新できます。 これは、フォントファイルがファイル名や関連するフォント IDを変更せずに変更された場合など、キャッシュ検証メカニズムによって直接追跡されないリソースが変更された後に便利です。

ネストされたリクエストで指定された場合、`cache=on`は、ネストされたリクエストによって生成された画像の永続的なサーバーサイドキャッシュを有効にします。 ネストされたリクエストに対するキャッシュを有効にするには、同じネストされたリクエストが同じパラメーターで繰り返し呼び出されることを想定している場合にのみ注意する必要があります。

## プロパティ {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

リクエスト属性： 現在のレイヤー設定に関係なく適用されます。 リクエストが返信画像を返さない場合は無視されます。 *`clientControl`*は、クライアントサイドのキャッシュが画像カタログによって無効にされている場合（`catalog::Expiration`に負の値がある場合）は無視されます。

クライアント側のキャッシュ制御（`on`および`off`のみ）は、[!DNL /is/content/]の静的コンテンツ要求でも使用できます。

## 初期設定 {#section-4124b2c836e2491489b9009a92fe4f22}

HTTP リクエストの`cache=on,on`、ネストされた/埋め込みリクエストの`cache=off`、静的コンテンツリクエストの`cache=on`。

## 関連項目 {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[ カタログ：：有効期限](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a)、[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
