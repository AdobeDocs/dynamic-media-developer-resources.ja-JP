---
description: 画像サービングは、特定のレコードのカタログ画像セットに関連付けられているすべてのリソースとメタデータを表す階層テキスト応答（xml または json）を取得するメカニズムを提供します。
solution: Experience Manager
title: メディアセットリクエスト
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 0%

---

# メディアセットリクエスト{#media-set-requests}

画像サービングは、特定のレコードの catalog::ImageSet に関連付けられたすべてのリソースとメタデータを表す、階層テキスト応答（xml または json）を取得するメカニズムを提供します。

このメカニズムを使用して応答を生成し、単純な画像、ビデオ、ビデオセット、スウォッチセット、スピンセット、ページセット（e カタログ）、メディアセットに関する情報を表示できます。

## リクエスト構文 {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

に対する `catalog::ImageSet` は、 `req=set` 修飾子を使用し、ネットパス内のカタログレコード id を参照します。 または、 `imageset=` 修飾子。 この `imageset=` modifier を使用して画像セットを指定します。画像セット値をエスケープし、含まれる修飾子が URL クエリ文字列の一部として解釈されないようにするには、値全体を中括弧で囲む必要があります。

## セット応答のタイプ {#section-93eb0a1f70344da2a888e56372ad3896}

設定メカニズムでは、次の種類の応答がサポートされています。

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>単純な画像 </p></td> 
  <td class="stentry"> <p>画像レコード ( <span class="codeph"> catalog::ImageSet</span> 定義済み </p></td> 
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
  <td class="stentry"> <p>基本的なスウォッチ項目またはスウォッチセットレコードへの参照で構成される一連の項目。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>スピンセット </p></td> 
  <td class="stentry"> <p>画像 ID の単純なリストで構成される一連の項目。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 次元スピンセット </p></td> 
  <td class="stentry"> <p>単純な画像または基本的なスピンセットへの参照から成る一連の項目。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ページセット </p></td> 
  <td class="stentry"> <p>最大 3 ページの画像のリストから成る一連の項目 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>メディアセット </p></td> 
  <td class="stentry"> <p>単純な画像、ビデオセット、スウォッチセット、階層的なスウォッチセット、スピンセット、2 次元のスピンセット、ページセット、ビデオアセットから成る一連の項目です。 各メディアセット項目には、オプションのスウォッチを含めることもできます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ビデオセット </p></td> 
  <td class="stentry"> <p>シンプルなビデオのリストで構成される一連の項目です。 </p></td> 
 </tr> 
</table>

## 外部セットタイプの検出 {#section-3dd6e453528d46898e559d31458a59ba}

実行時に `req=set` リクエストを受信した場合、生成する応答のタイプは、 `catalog::AssetType`. If `catalog::AssetType` が定義されていない場合、応答タイプは次のルールによって決定されます。

* レコードが画像カタログ AND に見つかった場合 `catalog::ImageSet` が定義されている

   * レコード内の 1 つ以上のエントリにコロンが含まれている場合、e-catalog セットを想定する画像セットフィールドにコロンが含まれている
   * レコードの画像セットフィールド内の 1 つ以上のエントリに 2 つのセミコロンが含まれている場合、メディアセットを使用します。
   * レコード内の 1 つ以上のエントリにセミコロンが 1 つ以上含まれている場合、画像セットを使用します。
   * コロンやセミコロンを含むエントリがなく、少なくとも 1 つのエントリに参照セットまたはインラインセット（これは 2D スピンセット）が含まれている場合、スピンセットを想定します。
   * エントリにコロンやセミコロン、参照セット、インラインセット（画像のコンマ区切りリスト）が含まれていない場合は、不明なセットと見なします。

* 画像と静的コンテンツカタログの両方にレコードが見つかった場合

   * ファイル拡張子が次のセットにある場合は、ビデオを想定します。mp3, mp4, flv, f4v, swf, xml
   * それ以外の場合は画像を仮定

* レコードが静的コンテンツカタログに見つかったが、画像カタログに見つからなかった場合

   * ファイル拡張子が次のセットにある場合は、ビデオを想定します。mp3, mp4, flv, f4v, swf, xml
   * それ以外の場合は静的と見なす

* レコードが画像カタログに見つかったが、静的コンテンツカタログに見つからなかった場合

   * 画像を仮定

* 画像カタログでレコードが見つからず、静的コンテンツカタログでレコードが見つからない場合

   * ファイル拡張子が次のような設定になっている場合は、ファイルベースのビデオを想定します。mp3, mp4, flv, f4v, swf, xml
   * それ以外の場合はファイルベースの画像を想定する

どのような場合でも、結果の XML 応答は、検出されたタイプに対応する set root ノードを持つ指定された XML ドキュメントに準拠します。

## 内部セットタイプ検出 {#section-8f46490e467247e69ce284704def06f3}

外部セットがタイプのメディアセットとして検出された場合、応答には、 `catalog::ImageSet`. 特定のメディアセットエントリに対してオプションの type パラメーターが指定されている場合、次の表に従って出力タイプにマッピングされます。

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

特定のメディアセットエントリのオプションの type パラメーターが指定されていない場合、またはサポートされていないタイプに対応する場合、メディアセット項目タイプは、外部のセットレベルで適用されたのと同じルールを使用して自動検出されます。

## XML 仕様 {#section-c1bd60948ef545759a16885bb6fcc607}

返される xml 応答は、次の仕様に準拠しています。

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

この `labelkey=` 修飾子は、 `catalog::UserData`画像およびスウォッチのラベルを生成するためのフィールド この `catalog:UserData` フィールドはキーと値のペアのセットとして解析され、このセットの labelkey インデックスは特定のキーの値を取得します。 この値は、 *`l`* 属性 *`s`* および *`i`*.

## 強制された制限 {#section-b9f042873bee45a5ae11b69fd42f2bca}

応答のサイズを制限し、自己参照的な問題を防ぐために、ネストの最大の深さは server プロパティで制御します `PS::fvctx.nestingLimit`. この制限を超えると、エラーが返されます。

大きな e カタログセットの xml 応答のサイズを制限するために、server プロパティに従って、パンフレットセット項目のプライベートメタデータは抑制されます `PS::fvctx.brochureLimit`. パンフレットの上限に達するまで、パンフレットに関連付けられているすべてのプライベートメタデータが書き出されます。 制限を超えた後、プライベートマップとユーザデータを抑制し、対応するフラグを設定して、抑制されたデータの種類を示す。

ネストされたメディアセットはサポートされていません。 ネストされたメディアセットは、メディアセットタイプのメディアセット項目を含むメディアセットとして定義されます。 この条件が検出された場合は、エラーが返されます。

## 例 {#section-588c9d33aa05482c86cd2b1936887228}

XML 応答の例： `req=set` リクエストについては、「プロパティの例」ヘッダーの「HTML」ページ」を参照してください。

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 関連項目 {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [画像カタログ参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
