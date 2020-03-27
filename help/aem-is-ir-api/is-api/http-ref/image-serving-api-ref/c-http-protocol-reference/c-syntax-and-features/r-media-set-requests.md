---
description: 画像サービングは、特定のレコードのカタログ画像セットに関連付けられたすべてのリソースとメタデータを表す、階層テキスト応答（xmlまたはjson）を取得するメカニズムを提供します。
seo-description: 画像サービングは、特定のレコードのカタログ画像セットに関連付けられたすべてのリソースとメタデータを表す、階層テキスト応答（xmlまたはjson）を取得するメカニズムを提供します。
seo-title: メディアセットの要求
solution: Experience Manager
title: メディアセットの要求
topic: Scene7 Image Serving - Image Rendering API
uuid: af9fabcd-531d-43fb-bd97-269923bea5e8
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# メディアセットの要求{#media-set-requests}

画像サービングは、特定のレコードのcatalog::ImageSetに関連付けられたすべてのリソースとメタデータを表す、階層テキスト応答（xmlまたはjson）を取得するメカニズムを提供します。

ビューアはこのメカニズムを使用して応答を生成し、簡単な画像、ビデオ、ビデオセット、スウォッチセット、スピンセット、ページセット(e-catalog)およびメディアセットに関するプレゼンテーションを通知できます。

## リクエストの構文 {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

に対する設定応答は、修 `catalog::ImageSet` 飾子を使用し、ネットパス `req=set` のカタログレコードIDを参照することで取得できます。 または、修飾子を使用して画像セットをURL内で直接指定でき `imageset=` ます。 修飾子を使 `imageset=` 用して画像セットを指定する場合、画像セット値をエスケープし、含まれる修飾子がURLクエリ文字列の一部として解釈されないように、値全体を波括弧で囲む必要があります。

## セット応答のタイプ {#section-93eb0a1f70344da2a888e56372ad3896}

この設定メカニズムでは、次のタイプの応答がサポートされます。

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>単純な画像 </p></td> 
  <td class="stentry"> <p>catalog::ImageSetが定義されて <span class="codeph"> いない画像レコード</span> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>簡単なビデオ </p></td> 
  <td class="stentry"> <p>静的コンテンツカタログ内のビデオレコード。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>スウォッチセット </p></td> 
  <td class="stentry"> <p>画像レコードへの参照と、スウォッチとして使用される画像レコードへのオプションの個別の参照から成る一連の項目です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>階層的スウォッチセット </p></td> 
  <td class="stentry"> <p>基本的なスウォッチ項目またはスウォッチセットレコードへの参照で構成される項目のセット。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>スピンセット </p></td> 
  <td class="stentry"> <p>画像IDの単純なリストから成る一連の項目。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2次元スピンセット </p></td> 
  <td class="stentry"> <p>単純な画像または基本的なスピンセットへの参照で構成される項目のセット。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ページセット </p></td> 
  <td class="stentry"> <p>最大3つのページ画像のリストから成る一連の項目 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>メディアセット </p></td> 
  <td class="stentry"> <p>単純な画像、ビデオセット、スウォッチセット、階層的なスウォッチセット、スピンセット、2次元スピンセット、ページセットおよびビデオアセットから構成される項目のセットです。 各メディアセット項目には、オプションのスウォッチを含めることもできます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ビデオセット </p></td> 
  <td class="stentry"> <p>単純なビデオのリストで構成される一連の項目です。 </p></td> 
 </tr> 
</table>

## 外部セットの種類の検出 {#section-3dd6e453528d46898e559d31458a59ba}

リクエスト `req=set` を受け取ると、生成する応答のタイプは、の値によって決まりま `catalog::AssetType`す。 を定義 `catalog::AssetType` していない場合、応答タイプは次のルールによって決まります。

* レコードが画像カタログ内にある場合、ANDが定 `catalog::ImageSet` 義されている

   * レコード内の1つ以上のエントリが画像セットフィールドにコロンが含まれる場合、e-catalogセットを想定
   * レコードの画像セットフィールドに2つ以上のセミコロンが含まれている場合、メディアセットを想定します。
   * レコードの画像セットフィールドに1つ以上のエントリがセミコロンを1つ含む場合、画像セットを想定します。
   * エントリにコロンやセミコロンが含まれず、少なくとも1つのエントリに参照セットまたはインラインセット（2Dスピンセット）が含まれている場合、スピンセットを想定します。
   * エントリにコロン、セミコロン、参照セット、インラインセット（画像のコンマ区切りリスト）が含まれない場合、不明なセットと見なされます。

* 画像と静的コンテンツの両方のカタログでレコードが見つかった場合

   * ファイル拡張子が次のセットの場合、ビデオを想定します。mp3、mp4、flv、f4v、swf、xml
   * 画像を想定しない

* レコードが静的コンテンツカタログで見つかったが、画像カタログで見つからなかった場合

   * ファイル拡張子が次のセットの場合、ビデオを想定します。mp3、mp4、flv、f4v、swf、xml
   * それ以外は静的と見なす

* レコードが画像カタログに見つかったが、静的コンテンツカタログに見つからなかった場合

   * 画像を仮定

* レコードが画像カタログに見つからず、静的コンテンツカタログに見つからない場合

   * ファイル拡張子が次のセットの場合、ファイルベースのビデオを想定します。mp3、mp4、flv、f4v、swf、xml
   * それ以外の場合はファイルベースの画像を想定

どのような場合でも、結果のxml応答は、検出されたタイプに対応するset root nodeを持つ指定されたXMLドキュメントに準拠します。

## 内部セットタイプの検出 {#section-8f46490e467247e69ce284704def06f3}

外側のセットがメディアセットのタイプとして検出されると、応答には、内の各メディアセットエントリに対応するメディアセット項目のセットが含まれま `catalog::ImageSet`す。 特定のメディアセットエントリに対してオプションのtypeパラメータが指定されている場合、次の表に従って出力タイプにマップされます。

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

特定のメディアセットエントリのオプションのtypeパラメータが指定されていない場合、またはサポートされていないタイプに対応する場合、メディアセットの項目タイプは、外側のセットレベルで適用されたのと同じルールを使用して自動検出されます。

## XML仕様 {#section-c1bd60948ef545759a16885bb6fcc607}

返されるxml応答は、次の仕様に準拠しています。

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

修飾子は `labelkey=` フィールドと共に使用し `catalog::UserData`て、画像やスウォッチのラベルを生成します。 フィー `catalog:UserData` ルドは、キーと値のペアのセットと、このセット内のlabelkeyインデックスとして解析され、指定されたキーの値を取得します。 次に、この値がとの属性 *`l`* に返さ *`s`* れます *`i`*。

## 強制的な制限 {#section-b9f042873bee45a5ae11b69fd42f2bca}

応答のサイズを制限し、自己参照の問題を防ぐために、ネストの深さの最大値はserverプロパティで制御します `PS::fvctx.nestingLimit`。 この制限を超えると、エラーが返されます。

大きなe-catalogセットのXML応答のサイズを制限するため、サーバのプロパティに従ってパンフレットセット項目のプライベートメタデータは抑制されま `PS::fvctx.brochureLimit`す。 パンフレットの上限に達するまで、パンフレットに関連付けられたすべてのプライベートメタデータが書き出されます。 制限を超えると、プライベートマップとユーザデータは非表示になり、どのデータタイプが抑制されたかを示すフラグが設定されます。

ネストされたメディアセットはサポートされていません。 ネストされたメディアセットは、メディアセットの種類のメディアセット項目を含むメディアセットとして定義されます。 この状態が検出されると、エラーが返されます。

## 例 {#section-588c9d33aa05482c86cd2b1936887228}

リクエストのXML応答の例につ `req=set` いては、HTMLの例ヘッダーのプロパティページを参照してください。

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 関連項目 {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [Image Catalog Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)

