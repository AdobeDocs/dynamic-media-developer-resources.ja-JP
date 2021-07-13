---
description: 画像サービングは、特定のレコードのカタログImageSetに関連付けられたすべてのリソースとメタデータを表す、階層テキスト応答（xmlまたはjson）を取得するメカニズムを提供します。
solution: Experience Manager
title: メディアセットリクエスト
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# メディアセットリクエスト{#media-set-requests}

画像サービングは、特定のレコードのcatalog::ImageSetに関連付けられたすべてのリソースとメタデータを表す、階層テキスト応答（xmlまたはjson）を取得するメカニズムを提供します。

ビューアはこのメカニズムを使用して応答を生成し、単純な画像、ビデオ、ビデオセット、スウォッチセット、スピンセット、ページセット（eカタログ）、メディアセットの表示を通知できます。

## リクエスト構文 {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

`catalog::ImageSet`に対する設定応答は、`req=set`修飾子を使用して、ネットパス内のカタログレコードIDを参照することで取得できます。 または、 `imageset=`修飾子を使用して、画像セットをURL内で直接指定することもできます。 画像セットの指定に`imageset=`修飾子を使用する場合、画像セット値をエスケープし、含まれる修飾子がURLクエリ文字列の一部として解釈されないように、値全体を中括弧で囲む必要があります。

## セット応答のタイプ {#section-93eb0a1f70344da2a888e56372ad3896}

設定メカニズムでは、次のタイプの応答がサポートされます。

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>単純な画像 </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::ImageSet</span>が定義されていない画像レコード。 </p></td> 
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
  <td class="stentry"> <p>階層スウォッチセット </p></td> 
  <td class="stentry"> <p>基本的なスウォッチ項目またはスウォッチセットレコードへの参照で構成される項目のセットです。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>スピンセット </p></td> 
  <td class="stentry"> <p>画像IDのシンプルなリストで構成される一連の項目。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2次元スピンセット </p></td> 
  <td class="stentry"> <p>単純な画像または基本的なスピンセットへの参照から成る一連の項目。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ページセット </p></td> 
  <td class="stentry"> <p>最大3ページの画像のリストから成る一連の項目 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>メディアセット </p></td> 
  <td class="stentry"> <p>単純な画像、ビデオセット、スウォッチセット、階層的なスウォッチセット、スピンセット、2Dスピンセット、ページセット、ビデオアセットから成る一連の項目。 各メディアセット項目には、オプションのスウォッチを含めることもできます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ビデオセット </p></td> 
  <td class="stentry"> <p>シンプルなビデオのリストで構成される一連の項目です。 </p></td> 
 </tr> 
</table>

## 外部セット型検出 {#section-3dd6e453528d46898e559d31458a59ba}

`req=set`リクエストを受け取ると、生成する応答のタイプは`catalog::AssetType`の値によって決まります。 `catalog::AssetType`が定義されていない場合、応答タイプは次のルールに基づいて決定されます。

* レコードが画像カタログに見つかり、 `catalog::ImageSet`が定義されている場合

   * レコード内の1つ以上のエントリにコロンが含まれている場合、eカタログセットを想定する
   * レコードの画像セットフィールド内に少なくとも1つのエントリに2つのセミコロンが含まれている場合、メディアセットを想定します。
   * レコード内の1つ以上のエントリがセミコロンを1つ含む場合、画像セットを使用します。
   * コロンとセミコロンが含まれていないエントリが1つも参照先のセットまたはインラインセット（これは2Dスピンセット）を含むエントリが1つも含まれている場合に、スピンセットを使用します。
   * コロン、セミコロン、参照セット、インラインセット（画像のコンマ区切りリスト）が含まれないエントリの場合、不明なセットを想定します。

* 画像と静的コンテンツカタログの両方でレコードが見つかる場合

   * ファイル拡張子が次のセットの場合、ビデオを想定します。mp3, mp4, flv, f4v, swf, xml
   * それ以外の場合は画像を仮定

* レコードが静的コンテンツカタログに見つかったが、画像カタログに見つからなかった場合

   * ファイル拡張子が次のセットの場合、ビデオを想定します。mp3, mp4, flv, f4v, swf, xml
   * それ以外は静的と見なす

* レコードが画像カタログに見つかったが、静的コンテンツカタログに見つからなかった場合

   * 画像を仮定

* レコードが画像カタログで見つからず、静的コンテンツカタログで見つからない場合

   * ファイル拡張子が次のセットにある場合、ファイルベースのビデオと見なします。mp3, mp4, flv, f4v, swf, xml
   * それ以外の場合はファイルベースの画像を想定する

どの場合でも、結果のXML応答は、検出された型に対応するset rootノードを持つ指定されたXMLドキュメントに準拠します。

## 内部セット型検出 {#section-8f46490e467247e69ce284704def06f3}

外部セットがタイプのメディアセットとして検出された場合、応答は`catalog::ImageSet`内の各メディアセットエントリに対応するメディアセット項目のセットを含む。 特定のメディアセットエントリに対してオプションのtypeパラメーターが指定されている場合、次の表に従って出力タイプにマッピングされます。

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

特定のメディアセットエントリのオプションのタイプパラメーターが指定されていない場合、またはサポートされていないタイプに対応する場合は、外部のセットレベルで適用されたのと同じルールを使用して、メディアセット項目タイプが自動検出されます。

## XML仕様 {#section-c1bd60948ef545759a16885bb6fcc607}

返されるxml応答は、次の仕様に準拠しています。

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

`labelkey=`修飾子を`catalog::UserData`フィールドと共に使用して、画像とスウォッチのラベルを生成します。 `catalog:UserData`フィールドはキーと値のペアのセットとして解析され、このセットのラベルキーインデックスが特定のキーの値を取得します。 次に、この値が&#x200B;*`s`*&#x200B;と&#x200B;*`i`*&#x200B;の&#x200B;*`l`*&#x200B;属性に返されます。

## 強制的な制限 {#section-b9f042873bee45a5ae11b69fd42f2bca}

応答のサイズを制限し、自己参照的な問題を防ぐために、ネストの最大深度はサーバーのプロパティ`PS::fvctx.nestingLimit`で制御します。 この制限を超えると、エラーが返されます。

大きなeカタログセットに対するxml応答のサイズを制限するために、サーバのプロパティ`PS::fvctx.brochureLimit`に従って、パンフレットセット項目のプライベートメタデータを抑制する。 パンフレットの上限に達するまで、パンフレットに関連付けられているすべてのプライベートメタデータが書き出されます。 制限を超えると、プライベートマップとユーザーデータは抑制され、対応するフラグが設定され、抑制されたデータの種類が示されます。

ネストされたメディアセットはサポートされていません。 ネストされたメディアセットは、メディアセットタイプのメディアセット項目を含むメディアセットとして定義されます。 この条件が検出されると、エラーが返されます。

## 例 {#section-588c9d33aa05482c86cd2b1936887228}

`req=set`リクエストのXML応答のサンプルについては、HTMLの例ヘッダーのプロパティページを参照してください。

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 関連項目 {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) 、 [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3)、 [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)、画像カタログ [の参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
