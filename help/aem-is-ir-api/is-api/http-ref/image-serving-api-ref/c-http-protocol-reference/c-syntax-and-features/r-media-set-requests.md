---
description: Image Servingは、特定のレコードのカタログ ImageSetに関連付けられたすべてのリソースとメタデータを表す階層テキスト応答（xmlまたはjson）を取得するメカニズムを提供します。
solution: Experience Manager
title: メディアセットリクエスト
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
TQID: 'https://experienceleague.adobe.com/mcwY5R2hIttDyWKya6b3Jyvt2zwMdLyS4Xp8otY0c34'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 968
ht-degree: 0%

---

# メディアセットリクエスト{#media-set-requests}

画像サービングは、特定のレコードのcatalog::ImageSetに関連付けられたすべてのリソースとメタデータを表す階層テキスト応答（xmlまたはjson）を取得するためのメカニズムを提供します。

視聴者はこのメカニズムを使用して、シンプルな画像、ビデオ、ビデオセット、スウォッチセット、スピンセット、ページセット（電子カタログ）、およびメディアセットのプレゼンテーションに応答を生成できます。

## リクエスト構文 {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

`catalog::ImageSet`に対する設定された応答は、`req=set`修飾子を使用し、ネットパスでカタログレコード IDを参照することで取得できます。 または、`imageset=`修飾子を使用して、画像セットをURLで直接指定することもできます。 `imageset=`修飾子を使用して画像セットを指定する場合は、画像セットの値をエスケープし、含まれている修飾子がURL クエリ文字列の一部として解釈されないようにするために、値全体を中括弧で囲む必要があります。

## set応答の種類 {#section-93eb0a1f70344da2a888e56372ad3896}

set メカニズムは、次のタイプの応答をサポートしています。

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>シンプルな画像 </p></td> 
  <td class="stentry"> <p><span class="codeph"> カタログ：:ImageSet</span>が定義されていない画像レコード。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>シンプルな動画 </p></td> 
  <td class="stentry"> <p>静的コンテンツカタログのビデオレコード。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>スウォッチセット </p></td> 
  <td class="stentry"> <p>画像レコードへの参照と、スウォッチとして使用される画像レコードへのオプションの別個の参照で構成される一連のアイテム。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>階層型スウォッチセット </p></td> 
  <td class="stentry"> <p>基本的なスウォッチアイテムまたはスウォッチセットレコードへの参照で構成されるアイテムのセット。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>スピンセット </p></td> 
  <td class="stentry"> <p>画像IDの簡単なリストで構成される一連のアイテム。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2次元スピンセット </p></td> 
  <td class="stentry"> <p>単純な画像または基本的なスピンセットへの参照で構成される一連のアイテム。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ページセット </p></td> 
  <td class="stentry"> <p>最大3つのページ画像のリストで構成されるアイテムのセット </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>メディアセット </p></td> 
  <td class="stentry"> <p>シンプルな画像、ビデオセット、スウォッチセット、階層スウォッチセット、スピンセット、2次元スピンセット、ページセット、ビデオアセットで構成される一連のアイテム。 各メディアセット項目には、オプションのスウォッチを含めることもできます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ビデオセット </p></td> 
  <td class="stentry"> <p>シンプルなビデオのリストで構成される一連のアイテム。 </p></td> 
 </tr> 
</table>

## 外部設定タイプ検出 {#section-3dd6e453528d46898e559d31458a59ba}

`req=set` リクエストを受信すると、生成する応答のタイプは`catalog::AssetType`の値によって決まります。 `catalog::AssetType`が定義されていない場合、応答タイプは次のルールによって決定されます。

* 画像カタログにレコードが見つかった場合、`catalog::ImageSet`が定義されています

   * レコード画像セットフィールドの少なくとも1つのエントリにコロンが含まれている場合は、e カタログセットと仮定します
   * レコード画像セットフィールドの少なくとも1つのエントリに2つのセミコロンが含まれている場合は、メディアセットを仮定します。
   * レコードイメージセットフィールドの少なくとも1つのエントリに1つのセミコロンが含まれている場合は、画像セットを想定します。
   * 入力にコロンやセミコロンが含まれていないが、少なくとも1つの入力に参照セットまたはインラインセットが含まれている場合は、スピンセットを仮定します（これは2D スピンセットです）。
   * コロンやセミコロン、参照セットやインラインセットを含むエントリがない場合は、不明なセットを想定します（コンマ区切りの画像リストなど）。

* 画像と静的コンテンツカタログの両方にレコードが見つかった場合

   * ファイル拡張子がmp3、mp4、flv、f4v、swf、xmlのセットに含まれている場合は、ビデオを想定します。
   * それ以外の場合は画像を仮定

* 静的コンテンツカタログにレコードが見つかりますが、画像カタログには見つからない場合

   * ファイル拡張子がmp3、mp4、flv、f4v、swf、xmlのセットに含まれている場合は、ビデオを想定します。
   * それ以外の場合は静的と見なす

* のレコードが画像カタログ内に見つかりますが、静的コンテンツカタログ内に見つからない場合

   * 画像を仮定

* 画像カタログにレコードが見つからず、静的コンテンツカタログにレコードが見つからない場合

   * ファイル拡張子がmp3、mp4、flv、f4v、swf、xmlの場合は、ファイルベースのビデオを想定します。
   * それ以外の場合は、ファイルベースの画像を想定

いずれの場合も、結果のXML応答は、検出されたタイプに対応するルートノードが設定された指定のXML ドキュメントに準拠します。

## インナーセットタイプ検出 {#section-8f46490e467247e69ce284704def06f3}

外部セットがタイプ メディアセットとして検出されると、応答には、`catalog::ImageSet`の各メディアセットエントリに対応する一連のメディアセットアイテムが含まれます。 オプションのtype パラメーターが特定のメディアセットエントリに指定されている場合は、次の表に従って出力タイプにマッピングされます。

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

特定のメディアセットエントリのオプションのtype パラメーターが指定されていないか、サポートされていないタイプに対応する場合、メディアセット項目タイプは、外部セットレベルで適用されたのと同じルールを使用して自動検出されます。

## XML仕様 {#section-c1bd60948ef545759a16885bb6fcc607}

返されるxml応答は、次の仕様に準拠しています。

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

`labelkey=`修飾子は、`catalog::UserData` フィールドと共に使用して、画像およびスウォッチのラベルを生成します。 `catalog:UserData` フィールドは、キーと値のペアのセットとして解析され、このセットにlabelkey インデックスが追加されて、特定のキーの値が取得されます。 この値は、*`s`*&#x200B;および&#x200B;*`i`*&#x200B;の&#x200B;*`l`*&#x200B;属性で返されます。

## 制限の実施 {#section-b9f042873bee45a5ae11b69fd42f2bca}

応答のサイズを制限し、自己参照の問題を防ぐため、ネストの最大深度はサーバープロパティ `PS::fvctx.nestingLimit`によって制御されます。 この制限を超えると、エラーが返されます。

大規模な電子カタログセットのXML応答のサイズを制限するために、サーバープロパティ `PS::fvctx.brochureLimit`に従って、パンフレットセットアイテムのプライベートメタデータが抑制されます。 パンフレットに関連付けられたすべてのプライベートメタデータは、パンフレットの制限に達するまで書き出されます。 制限を超えた後、プライベートマップとユーザーデータが抑制され、対応するフラグが、どのタイプのデータが抑制されたかを示すように設定されます。

ネストされたメディアセットはサポートされていません。 ネストされたメディアセットは、メディアセットのタイプのメディアセットアイテムを含むメディアセットとして定義されます。 この条件が検出されると、エラーが返されます。

## 例 {#section-588c9d33aa05482c86cd2b1936887228}

`req=set` リクエストのサンプル XML応答については、「HTMLの例」ヘッダーの「プロパティ」ページを参照してください。

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 関連項目 {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、[imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3)、[ カタログ：:ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)、[画像カタログ参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
