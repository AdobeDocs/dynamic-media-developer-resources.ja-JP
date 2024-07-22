---
title: キャッシュ
description: キャッシュコントロール。 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と内部キャッシュのキャッシュを選択的に無効にするこ  [!DNL Platform Server]  ができます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# キャッシュ{#cache}

キャッシュコントロール。 クライアント側キャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と内部 [!DNL Platform Server] キャッシュのキャッシュを選択的に無効にできます。

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

`*`cacheControl`*` 値が 1 つだけ指定されている場合は、クライアントとサーバーの両方のキャッシュに適用されます。

`validate` キーワードを使用すると、画像ファイルが変更された後にキャッシュエントリを更新できます。キャッシュエントリが自動的に期限切れになるのを待つ必要はありません。 クライアント キャッシュは、このコマンドの影響を受けません。

`update` キーワードを使用すると、サーバーサイドのキャッシュエントリを強制的に更新できます。 これは、ファイル名や関連するフォント ID を変更せずにフォントファイルを変更した場合など、キャッシュ検証メカニズムによって直接追跡されないリソースが変更された後に役立ちます。

ネストされたリクエストで指定した場合、`cache=on` は、ネストされたリクエストによって生成された画像のサーバーサイドの永続的なキャッシュを有効にします。 ネストされたリクエストのキャッシュを有効にする場合は、同じネストされたリクエストが、まったく同じパラメーターで繰り返し呼び出されることが想定される場合にのみ、注意してください。

## プロパティ {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

リクエスト属性。 現在のレイヤ設定に関係なく適用されます。 リクエストが返信画像を返さない場合は無視されます。 画像カタログでクライアントサイドのキャッシュが無効になっている場合（`catalog::Expiration` の値が負の値の場合）、*`clientControl`*は無視されます。

クライアントサイドのキャッシュ制御（`on` と `off` のみ）は、[!DNL /is/content/] の静的コンテンツリクエストにも使用できます。

## 初期設定 {#section-4124b2c836e2491489b9009a92fe4f22}

HTTP リクエストの場合は `cache=on,on`、ネストされたリクエストまたは埋め込まれたリクエストの場合は `cache=off`、静的コンテンツリクエストの場合は `cache=on` です。

## 関連項目 {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
