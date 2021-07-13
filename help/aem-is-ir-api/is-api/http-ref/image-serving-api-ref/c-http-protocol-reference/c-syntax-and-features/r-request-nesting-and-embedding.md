---
description: 画像サービングは、画像サービング要求の無制限のネスト、画像レンダリング要求の埋め込み、および外部サーバーから取得した画像の埋め込みをサポートします。 これらのメカニズムは、レイヤーイメージとレイヤーマスクのみでサポートされます。
solution: Experience Manager
title: リクエストのネストと埋め込み
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# リクエストのネストと埋め込み{#request-nesting-and-embedding}

画像サービングは、画像サービング要求の無制限のネスト、画像レンダリング要求の埋め込み、および外部サーバーから取得した画像の埋め込みをサポートします。 これらのメカニズムは、レイヤーイメージとレイヤーマスクのみでサポートされます。

>[!NOTE]
>
>特定の電子メールクライアントやプロキシサーバーでは、ネストや埋め込みの構文に使用する波括弧がエンコードされる場合があります。 これが問題となるアプリケーションでは、波括弧の代わりに括弧を使用する必要があります。

## ネストされた画像サービング要求 {#section-6954202119e0466f8ff27c79f4f039c8}

次の構文を使用して、 `src=` （または`mask=`）コマンドで画像サービング要求全体を指定することで、レイヤーソースとして使用できます。

`…&src=is( nestedRequest)&…`

`is`トークンでは大文字と小文字が区別されます。

ネストされたリクエストには、サーバーのルートパス（通常は` http:// *[!DNL server]*/is/image/'`）を含めないでください。

>[!NOTE]
>
>ネストされた要求の区切り文字(`'(',')'`)と、ネストされた要求内のコマンド区切り文字(`'?'`、`'&'`、`'='`)は、HTTPエンコードしないでください。 事実上、ネストされたリクエストは、外側の（ネストされた）リクエストと同じでエンコードする必要があります。

前処理ルールは、ネストされたリクエストに適用されます。

ネストされたリクエストで（リクエストURLまたは`catalog::Modifier`または`catalog::PostModifier`で）指定された場合、次のコマンドは無視されます。

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

ネストされた要求の結果イメージにマスク（アルファ）データが含まれる場合、その画像はレイヤーマスクとして埋め込みレイヤーに渡されます。

また、ネストされたリクエストに適用される画像カタログの`attribute::MaxPix`と`attribute::DefaultPix`も無視されます。

ネストされたIS要求のイメージ結果は、オプションで`cache=on`を含めることでキャッシュできます。 デフォルトでは、中間データのキャッシュは無効になっています。 キャッシュは、中間画像が適切な期間内に別のリクエストで再利用されると予想される場合にのみ有効にする必要があります。 標準のサーバー側キャッシュ管理が適用されます。 データは可逆形式でキャッシュされます。

## 埋め込み画像レンダリング要求 {#section-69c5548db930412b9b90d9b2951a6969}

Dynamic Mediaの画像レンダリングがサーバーで有効になっている場合、レンダリング要求はsrc=（またはmask=）コマンドで指定することで、レイヤーソースとして使用できます。 次の構文を使用します。

` …&src=ir( *[!DNL renderRequest]*)&…`

`ir`トークンでは大文字と小文字が区別されます。

*[!DNL renderRequest]* は、通常の画像レンダリングリクエストです（HTTPルートパスを除く） ` http:// *[!DNL server]*/ir/render/`。

>[!NOTE]
>
>ネストされた要求の区切り文字(`'(',')'`)と、ネストされた要求内のコマンド区切り文字(`'?'`、`'&'`、`'='`)は、HTTPエンコードしないでください。 実際には、埋め込みリクエストは、外部（埋め込み）リクエストと同じエンコードが必要です。

ネストされた要求で指定された場合、次の画像レンダリングコマンドは無視されます。

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

また、ネストされたレンダリング要求に適用されるマテリアルカタログの`attribute::MaxPix`と`attribute::DefaultPix`も無視されます。

ネストされたIR要求の画像結果は、オプションで`cache=on`を含めることでキャッシュできます。 デフォルトでは、中間データのキャッシュは無効になっています。 キャッシュは、中間画像が適切な期間内に別のリクエストで再利用されると予想される場合にのみ有効にする必要があります。 標準のサーバー側キャッシュ管理が適用されます。 データは可逆形式でキャッシュされます。

## 埋め込みFXGレンダリング要求 {#section-c817e4b4f7da414ea5a51252ca7e120a}

FXGグラフィックレンダラー([!DNL AGMServer])がインストールされ、画像サービングで有効になっている場合、FXG要求は`src=`（または`mask=`）コマンドで指定することで、レイヤーソースとして使用できます。 次の構文を使用します。

`…&src=fxg( renderRequest)&…`

`fxg`トークンでは大文字と小文字が区別されます。

>[!NOTE]
>
>FXGグラフィックのレンダリングは、Dynamic Mediaのホスト環境でのみ使用でき、追加のライセンスが必要な場合があります。 詳しくは、Dynamic Mediaテクニカルサポートにお問い合わせください。

*[!DNL renderRequest]* は、通常のFXGレンダリング要求です(HTTPルートパスを除きま ` http:// *[!DNL server]*/agm/render/`す)。

>[!NOTE]
>
>ネストされた要求内の区切り文字(`'(',')'`)とコマンド区切り文字(`'?'`、`'&'`、`'='`)は、HTTPエンコードしないでください。 実際には、埋め込みリクエストは、外部（埋め込み）リクエストと同じエンコードが必要です。

ネストされた要求で指定された場合、次のFXGコマンドは無視されます。

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## 外部画像ソース {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

画像サービングは、外部HTTPサーバー上のソース画像へのアクセスをサポートします。

>[!NOTE]
>
>リモートURLでは、HTTPプロトコルのみがサポートされています。

`src=`または`mask=`コマンドに外部URLを指定するには、外部URLまたはURLフラグメントを括弧で区切ります。

`…&src=( foreignUrl)&…`

重要：ネストされた要求内の区切り文字(`'(',')'`)とコマンド区切り文字(`'?'`、`'&'`、`'='`)は、HTTPエンコードしないでください。 実際には、埋め込みリクエストは、外部（埋め込み）リクエストと同じエンコードが必要です。

完全な絶対URL（`attribute::AllowDirectUrls`が設定されている場合）と`attribute::RootUrl`に対する相対URLが許可されます。 絶対URLが埋め込まれ、次の属性がある場合、エラーが発生します。`AllowDirectUrls`は0か、相対URLが指定され、`attribute::RootUrl`が空の場合。

外部URLはリクエストURLのパスコンポーネントで直接指定することはできませんが、相対パスを絶対URLに変換できるように前処理ルールを設定できます（以下の例を参照）。

外部画像は、HTTP応答に含まれるキャッシュヘッダーに従って、サーバーによってキャッシュされます。 `ETag`もLast-Modified HTTP応答ヘッダーも存在しない場合、応答はキャッシュされません。 同じ外部画像に対する繰り返しアクセスのパフォーマンスが低下する可能性があります。これは、画像サービングでは、アクセスのたびに画像を再取得して再検証する必要があるからです。

このメカニズムは、コンポーネントあたり16ビットのソース画像を除き、画像変換(IC)ユーティリティでサポートされるのと同じ画像ファイル形式をサポートします。

>[!NOTE]
>
>画像サービングは、外部画像が最初に使用されたときに検証ユーティリティを自動的に実行し、画像が有効で、送信中に破損していないことを確認します。 これにより、初回アクセスで若干の遅延が生じる場合があります。 最高のパフォーマンスを得るには、このような画像のサイズを制限するか、適切に圧縮される画像ファイル形式を使用することをお勧めします。

## 制限事項 {#section-fb68e3f0d40947feb94d7bf183b64929}

ネストされたリクエストや埋め込みリクエストによって生成される画像のサイズは、通常は自動的に最適化されます。 ネストされた要求画像のキャッシュが有効な場合、ネストされた画像の正確なサイズを指定することで、パフォーマンスの向上を実現できるので、キャッシュエントリを再利用する際に、それ以上の拡大・縮小が必要ありません。

重要な画像サービングは、ネストされた要求や埋め込み要求の二重エンコードをサポートしていません。 ネストされたリクエストと埋め込まれたリクエストは、単純なリクエストと同様にHTTPエンコードする必要があります。

## 例 {#section-d800cfc31abe46d2a964f8e7929231f1}

**キャッシュを使用したレイヤーテンプレート：**

ネストを使用して、レイヤーテンプレートにキャッシュを追加します。 限られた数の背景画像が、非常に可変なテキストでオーバーレイされます。 最初のテンプレート文字列は次のようになります。

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

少し変更を加えることで、レイヤー0の画像を事前にスケールし、持続的にキャッシュできるので、サーバーの負荷を軽減できます。

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Dynamic Media Image Renderingのリクエストの埋め込み**

[!DNL myCatalog/myTemplate]に保存されているテンプレートの使用Dynamic Media Image Renderingを使用して、テンプレートのlayer2の画像を生成します。

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

入れ子の中括弧に注意してください。 画像レンダリング要求により、画像サービングにコールバックが埋め込まれ、繰り返し可能なテクスチャが取得されます。

## 関連項目 {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) 、 [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、 [Request PreProcessing](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3)、Image Rendering Reference、 [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)、 [Image Serving Utilities](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
