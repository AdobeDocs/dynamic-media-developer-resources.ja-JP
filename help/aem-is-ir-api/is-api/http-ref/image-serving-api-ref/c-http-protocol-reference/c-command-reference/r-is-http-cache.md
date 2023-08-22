---
title: キャッシュ
description: キャッシュ制御。 内部で、クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）とキャッシュを選択的に無効にすることができます。 [!DNL Platform Server] キャッシュ。
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

キャッシュ制御。 内部で、クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）とキャッシュを選択的に無効にすることができます。 [!DNL Platform Server] キャッシュ。

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

1 つのみの場合 `*`cacheControl`*` 値を指定した場合、クライアントキャッシュとサーバーキャッシュの両方に適用されます。

The `validate` キーワードを使用すると、画像ファイルが変更された後にキャッシュエントリが自動的に期限切れになるのを待たずに、キャッシュエントリを更新できます。 クライアントのキャッシュは、このコマンドの影響を受けません。

The `update` キーワードを使用して、サーバー側のキャッシュエントリを強制的に更新できます。 これは、ファイル名や関連フォント ID を変更せずにフォントファイルを変更した場合など、キャッシュ検証メカニズムで直接追跡されないリソースを変更した後に役立ちます。

ネストされた要求で指定した場合、 `cache=on` ネストされた要求で生成された画像の永続的なサーバー側のキャッシュを有効にします。 同じネストされたリクエストが同じパラメーターを使用して繰り返し呼び出されると想定される場合にのみ、ネストされたリクエストのキャッシュを有効にするように注意してください。

## プロパティ {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

要求属性。 現在の画層設定に関係なく適用されます。 リクエストが返信画像を返さない場合は無視されます。 *`clientControl`クライアント側のキャッシュが画像カタログで無効になっている場合、*は無視されます ( `catalog::Expiration` は負の値です )。

クライアント側のキャッシュ制御 ( `on` および `off` ) は、静的コンテンツリクエストでも使用できます ( [!DNL /is/content/].

## 初期設定 {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` （HTTP リクエストの場合） `cache=off` ネストされた/埋め込み要求の場合 `cache=on` 静的コンテンツリクエスト用。

## 関連項目 {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
