---
description: playlogユーティリティは、HTTP応答キャッシュ用のコンテンツを事前に生成するために使用できます。
seo-description: playlogユーティリティは、HTTP応答キャッシュ用のコンテンツを事前に生成するために使用できます。
seo-title: 「playlog」ユーティリティ
solution: Experience Manager
title: 「playlog」ユーティリティ
topic: Scene7 Image Serving - Image Rendering API
uuid: 9044515e-7cfb-4e86-9ac4-e071b60f38d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 「playlog」ユーティリティ{#the-playlog-utility}

playlogユーティリティは、HTTP応答キャッシュ用のコンテンツを事前に生成するために使用できます。

既存の画像サービングHTTP応答キャッシュは、メジャーバージョンのアップグレード後（バージョン番号の1桁目または2桁目が変更された場合）に使用できるとは保証されません。 アップグレード後にサーバをフルロード状態にする場合、サーバは、キャッシュが適切に入力され、キャッシュのヒット率が増加するまで、最初の数時間のキャッシュミス要求を処理して過負荷になる可能性があります。

この初期読み込みスパイクを回避するために、 `playlog` このユーティリティを使用して、HTTP応答キャッシュ用のコンテンツを事前に生成できます。 `playlog` 既存のアクセスログファイルからHTTP要求を抽出し、サーバーに送信してキャッシュエントリを生成します。 一般的な使用シナリオでは、1日分のトラフィックを含む単一のアクセスログファイルを再生すれば十分です。

アップグレードのインストール後にHTTP応答キャッシュをプライミングするほか、このユーティリティは、新しいサーバを負荷分散環境に追加する際にキャッシュの内容を事前に生成するためにも使用されます。他のサーバーの最新のログファイルを再生します。

`playlog` は、以前のバージョンの画像サービングで生成されたほとんどのアクセスログファイルをサポートするように設定できます。

## 使用方法 {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -pプレフ <span class="varname"> ィッ </span> クス </span> </p> </td> 
  <td class="stentry"> <p>ログファイルから抽出された要求の前に付加するルートURL。 </p> <p>デフォルト： <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname"> col </span></span> </p> </td> 
  <td class="stentry"> <p>ログレコード内の要求が含まれるフィールド（列）番号。1を基準とします。 </p> <p>デフォルト：16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s区 <span class="varname"> 切 </span> り </span> </p> </td> 
  <td class="stentry"> <p>フィールドの区切り文字；正規表現パターン。 </p> <p>初期設定: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -mマー <span class="varname"> カ </span> ー </span> </p> </td> 
  <td class="stentry"> <p>リクエストマーカー；再生する必要があるログファイル内の要求を識別します。正規表現パターン。 </p> <p>デフォルト： <span class="codeph"> 要求： </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -xサフィッ <span class="varname"> クス </span> - </span> </p> </td> 
  <td class="stentry"> <p>ログファイルから抽出された要求に追加するサフィックス。を使用して、再生された要求をログファイル内のライブ要求と分離できます。'?' または「&amp;」区切り文字が自動的に挿入されます。サフィックスは、中括弧内の任意のログフィールドを位置で参照できます。デフォルトはmd5署名フィールドに対応します。 </p> <p>デフォルト： <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>詳細モードでは、生成された要求URLをstdoutに出力 <span class="codeph"> します </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>標準出力に書式を <span class="codeph"> 出力す </span>る </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method — 使用するHTTPリクエストメソッ <span class="codeph"> ド( get|post|head|smart </span>)。 </p> <p>デフォルト： <span class="codeph"> スマート </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos — 元のメソッドを取得するログファイル内のpos。 </p> <p>デフォルト：15 </p> </td> 
 </tr> 
</table>

Windowsの場合、ファイル名はで [!DNL playlog.bat] 、Linuxの場合はです [!DNL playlog.sh]。

## 例 {#section-716e5c35e9fa4ee3a4b0687381fcea40}

次の例は、Linux上の画像サービングで作成されたアクセスログファイルからのすべての要求を再生します。

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

次のコマンドは、Windows上の画像サービングによって作成されたトレースログファイル内のすべての要求を再生します。

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
