---
description: playlogユーティリティは、HTTP応答キャッシュ用のコンテンツを事前に生成するために使用できます。
solution: Experience Manager
title: 「playlog」ユーティリティ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: e0213978-3a1d-44b4-82bf-4527b980b29e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 1%

---

# 「playlog」ユーティリティ{#the-playlog-utility}

playlogユーティリティは、HTTP応答キャッシュ用のコンテンツを事前に生成するために使用できます。

既存の画像サービングHTTP応答キャッシュは、メジャーバージョンのアップグレード後（バージョン番号の1桁または2桁目が変更された場合）に使用できる保証はありません。 アップグレード後にサーバーをフル読み込み条件に移行する場合、キャッシュが合理的に入力され、キャッシュのヒット率が高くなるまで、サーバーが過負荷になり、最初の数時間のキャッシュミスリクエストの処理を引き受ける可能性があります。

この初期読み込みスパイクを回避するために、`playlog`ユーティリティを使用してHTTP応答キャッシュのコンテンツを事前に生成できます。 `playlog` は、既存のアクセスログファイルからHTTP要求を抽出し、サーバーに送信してキャッシュエントリを生成します。一般的な使用シナリオでは、1日分のトラフィックを含む1つのアクセスログファイルを再生すれば十分です。

アップグレードインストール後にHTTP応答キャッシュをプライミングする以外に、新しいサーバを負荷分散環境に追加する際にキャッシュの内容を事前に生成するユーティリティも使用されます。他のサーバーのいずれかから最新のログファイルを再生します。

`playlog` は、以前のバージョンの画像サービングで生成されたほとんどのアクセスログファイルをサポートするように設定できます。

## 使用方法 {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -pプレフィ <span class="varname"> ックス  </span> </span> </p> </td> 
  <td class="stentry"> <p>ログファイルから抽出された要求の前に付加するルートURL。 </p> <p>デフォルト：<span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n  <span class="varname"> col  </span> </span> </p> </td> 
  <td class="stentry"> <p>ログレコード内の要求を含むフィールド（列）番号。1から始まります。 </p> <p>デフォルト：16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s区切 <span class="varname"> り文字  </span> </span> </p> </td> 
  <td class="stentry"> <p>フィールド区切り文字；正規表現パターン。 </p> <p>初期設定: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -mマー <span class="varname"> カー  </span> </span> </p> </td> 
  <td class="stentry"> <p>リクエストマーカーは、再生する必要があるログファイル内の要求を識別します。正規表現パターン。 </p> <p>デフォルト：<span class="codeph">リクエスト：</span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -xサフィッ <span class="varname"> クス  </span> </span> </p> </td> 
  <td class="stentry"> <p>ログファイルから抽出された要求に付加するサフィックス。を使用して、再生されたリクエストとログファイル内のライブリクエストを分離できます。? または「&amp;」区切り文字が自動的に挿入されます。サフィックスは、中括弧内の位置で任意のログフィールドを参照できます。デフォルトはmd5署名フィールドに対応します。 </p> <p>デフォルト：<span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>詳細モード。生成されたリクエストURLを<span class="codeph"> stdout </span>に出力します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> stdout </span>に書式を出力します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method — 使用するHTTPリクエストメソッド( <span class="codeph"> get|post|head|smart </span>)。 </p> <p>デフォルト：<span class="codeph">スマート</span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos — 元のメソッドを取得するログファイル内のpos。 </p> <p>デフォルト：15 </p> </td> 
 </tr> 
</table>

Windowsの場合、ファイル名は[!DNL playlog.bat]で、Linuxの場合は[!DNL playlog.sh]です。

## 例 {#section-716e5c35e9fa4ee3a4b0687381fcea40}

次の例は、Linux上の画像サービングによって作成されたアクセスログファイルからのすべての要求を再生します。

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

次のコマンドは、Windows上の画像サービングによって作成されたトレースログファイル内のすべての要求を再生します。

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
