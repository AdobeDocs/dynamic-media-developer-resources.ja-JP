---
description: 画像サービングは、特定のレコードのカタログ ImageSet に関連付けられたすべてのリソースとメタデータを表す階層テキスト応答（xml または json）を取得するためのメカニズムを提供します。
solution: Experience Manager
title: メディアセットリクエスト
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# メディアセットリクエスト{#media-set-requests}

画像サービングは、特定のレコードの catalog::ImageSet に関連付けられたすべてのリソースとメタデータを表す階層テキスト応答（xml または json）を取得するメカニズムを提供します。

ビューアはこのメカニズムを使用して、単純な画像、ビデオ、ビデオセット、見本セット、スピンセット、ページセット（e カタログ）、メディアセットを、プレゼンテーションに知らせる応答を生成できます。

## リクエスト構文 {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

`catalog::ImageSet` の set 応答は、`req=set` 修飾子を使用してネットパス内のカタログレコード ID を参照することで取得できます。 または、`imageset=` 修飾子を使用して、画像セットを URL 内で直接指定することもできます。 `imageset=` 修飾子を使用して画像セットを指定する場合、画像セット値をエスケープするために値全体を中括弧で囲み、含まれる修飾子が URL クエリ文字列の一部として解釈されないようにする必要があります。

## セット応答のタイプ {#section-93eb0a1f70344da2a888e56372ad3896}

セットメカニズムでは、次のタイプの応答がサポートされています。

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>シンプルな画像 </p></td> 
  <td class="stentry"> <p>カタログ：:ImageSet<span class="codeph"> が定義 </span> れていない画像レコード。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>シンプルなビデオ </p></td> 
  <td class="stentry"> <p>静的コンテンツカタログのビデオレコード。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>スウォッチセット </p></td> 
  <td class="stentry"> <p>画像レコードへの参照と、スウォッチとして使用される画像レコードへのオプションの個別参照で構成される項目セット。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>階層スウォッチセット </p></td> 
  <td class="stentry"> <p>基本スウォッチ項目またはスウォッチセットレコードへの参照で構成される項目のセット。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>スピンセット </p></td> 
  <td class="stentry"> <p>画像 ID の単純なリストで構成される項目のセット。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 次元スピンセット </p></td> 
  <td class="stentry"> <p>単純な画像または基本スピンセットへの参照で構成される項目のセット。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ページセット </p></td> 
  <td class="stentry"> <p>最大 3 つのページ画像のリストで構成される項目のセット </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>メディアセット </p></td> 
  <td class="stentry"> <p>単純な画像、ビデオセット、スウォッチセット、階層的なスウォッチセット、スピンセット、2 次元スピンセット、ページセットおよびビデオアセットで構成される項目のセットです。 各メディアセット項目には、オプションのスウォッチを含めることもできます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ビデオセット </p></td> 
  <td class="stentry"> <p>シンプルなビデオのリストで構成される項目のセット。 </p></td> 
 </tr> 
</table>

## アウターセット型検知 {#section-3dd6e453528d46898e559d31458a59ba}

`req=set` リクエストを受信した場合、生成する応答のタイプは `catalog::AssetType` の値によって決まります。 `catalog::AssetType` が定義されていない場合、応答タイプは次のルールによって決定されます。

* 画像カタログでレコードが見つかり、`catalog::ImageSet` が定義されている場合

   * レコードの画像セットフィールドの 1 つ以上のエントリにコロンが含まれている場合に電子カタログセットが使用されると想定します
   * レコードの画像セットフィールドの 1 つ以上のエントリに 2 つのセミコロンが含まれている場合にメディアセットが発生すると仮定します。
   * レコードの画像セットフィールドの 1 つ以上のエントリに 1 つのセミコロンが含まれている場合、画像セットが想定されます。
   * エントリにコロンやセミコロンが含まれておらず、1 つ以上のエントリに参照セットまたはインラインセットが含まれている場合、スピンセットを想定します（これは 2D スピンセットです）。
   * エントリにコロン、セミコロン、参照セット、インラインセットが含まれていない場合（画像のコンマ区切りリストなど）、不明なセットと見なします。

* レコードが画像と静的コンテンツカタログの両方で見つかった場合

   * ファイル拡張子のセットが mp3、mp4、flv、f4v、swf、xml の場合は、ビデオを想定します。
   * それ以外の場合は画像を使用

* 静的コンテンツカタログでレコードが見つかったが、画像カタログでレコードが見つからない場合

   * ファイル拡張子のセットが mp3、mp4、flv、f4v、swf、xml の場合は、ビデオを想定します。
   * それ以外の場合は静的と見なす

* のレコードが画像カタログで見つかったが、静的コンテンツカタログでは見つからない場合

   * イメージの仮定

* レコードが画像カタログ内に見つからず、静的コンテンツカタログ内に見つからない場合

   * ファイル拡張子のセットが mp3、mp4、flv、f4v、swf、xml の場合、ファイルベースのビデオと見なされます。
   * それ以外の場合はファイルベースのイメージを想定

どの場合でも、結果の xml 応答は、検出されたタイプに対応するルートノードが設定された、指定された XML ドキュメントに準拠します。

## インナーセット式検出 {#section-8f46490e467247e69ce284704def06f3}

外部セットがタイプのメディアセットとして検出された場合、応答は、`catalog::ImageSet` 内の各メディアセットエントリに対応する一連のメディアセット項目を含む。 オプションの type パラメータが特定のメディアセットエントリに対して指定されている場合、次の表に従って出力タイプにマッピングされます。

| 入力タイプ | 出力タイプ |
|---|---|
| `img` | `img` |
| `basic` | `img` |
| `advanced_image` | `img` |
| `img_set` | `img_set` |
| `advanced_image_set` | `img_set` |
| `advanced_swatchset` | `img_set` |
| `spin` | `spin` |
| `video` | `video` |
| `video_set` | `video_set` |
| `static` | `static` |
| `ecat` | `ecat` |

特定のメディア セット エントリのオプションのタイプ パラメータが指定されていない場合、またはサポートされていないタイプに対応する場合、メディア セット項目のタイプは、外側のセット レベルで適用されたものと同じルールを使用して自動検出されます。

## XML 仕様 {#section-c1bd60948ef545759a16885bb6fcc607}

返される xml 応答は、次の仕様に準拠しています。

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

`labelkey=` 修飾子は、`catalog::UserData` フィールドと共に使用して、画像およびスウォッチのラベルを生成します。 `catalog:UserData` フィールドはキーと値のペアのセットとして解析され、このセットの labelkey インデックスが解析されて、指定されたキーの値が取得されます。 次に、この値が *`l`* と *`s`* の *`i`* 属性で返されます。

## 適用される制限 {#section-b9f042873bee45a5ae11b69fd42f2bca}

応答のサイズを制限し、自己参照の問題を防ぐために、ネストの最大深度はサーバープロパティ `PS::fvctx.nestingLimit` によって制御されます。 この制限を超えると、エラーが返されます。

大きな電子カタログ セットに対する xml 応答のサイズを制限するために、サーバープロパティ `PS::fvctx.brochureLimit` に従って、パンフレット セット項目の非公開メタデータが抑制されます。 パンフレットに関連付けられたすべての非公開メタデータは、パンフレットの上限に達するまで書き出されます。 制限を超えると、プライベート マップとユーザ データが省略され、省略されたデータのタイプを示す対応するフラグが設定されます。

ネストされたメディアセットはサポートされていません。 ネストされたメディア セットは、メディア セット タイプのメディア セット項目を含むメディア セットとして定義されます。 この条件が検出された場合は、エラーが返されます。

## 例 {#section-588c9d33aa05482c86cd2b1936887228}

`req=set` のリクエストに対する XML 応答のサンプルについては、HTMLの例ヘッダーのプロパティ ページを参照してください。

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 関連項目 {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、[imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3)、[catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)、[ 画像カタログ参照 ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
