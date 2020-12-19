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
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 1%

---


# &#39;playlog&#39;ユーティリティ{#the-playlog-utility}

playlogユーティリティは、HTTP応答キャッシュ用のコンテンツを事前に生成するために使用できます。

既存の画像サービングHTTP応答キャッシュは、メジャーバージョンのアップグレード後（バージョン番号の1桁目または2桁目が変更された場合）に使用できるとは限りません。 アップグレード後にサーバーをフルロード状態にする場合、サーバーは、キャッシュが適切に設定されキャッシュのヒット率が増加するまで、最初の数時間のキャッシュミス要求を処理して過負荷になる可能性があります。

この初期読み込みのスパイクを回避するために、`playlog`ユーティリティを使用して、HTTP応答キャッシュ用のコンテンツを事前に生成できます。 `playlog` 既存のアクセスログファイルからHTTP要求を抽出し、サーバーに送信してキャッシュエントリを生成します。一般的な使用方法のシナリオでは、1日分のトラフィックを含む単一のアクセスログファイルを再生すれば十分です。

アップグレードのインストール後にHTTP応答キャッシュをプライミングするだけでなく、新しいサーバを負荷分散環境に追加する際にキャッシュの内容を事前に生成するユーティリティも使用します。他のサーバーのいずれかから最新のログファイルを再生するだけです。

`playlog` は、画像サービングの以前のバージョンで生成されたほとんどのアクセスログファイルをサポートするように設定できます。

## 使用方法 {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p <span class="varname"> プレフィックス  </span> </span> </p> </td> 
  <td class="stentry"> <p>ログファイルから抽出された要求の前に付加するルートURL。 </p> <p>デフォルト：<span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname"> 列  </span> </span> </p> </td> 
  <td class="stentry"> <p>ログレコード内の要求が含まれるフィールド（列）番号。1を基準とします。 </p> <p>デフォルト：16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s <span class="varname"> セパレータ  </span> </span> </p> </td> 
  <td class="stentry"> <p>フィールドの区切り文字；正規式パターン。 </p> <p>初期設定: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m <span class="varname"> マーカー  </span> </span> </p> </td> 
  <td class="stentry"> <p>リクエストマーカー；再生する必要があるログファイル内の要求を識別します。正規式パターン。 </p> <p>デフォルト：<span class="codeph">リクエスト：</span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x <span class="varname"> サフィックス  </span> </span> </p> </td> 
  <td class="stentry"> <p>ログファイルから抽出された要求に追加するサフィックス；は、再生された要求をログファイル内のライブ要求から分離するために使用できます。'?' または「&amp;」区切り文字が自動的に挿入されます。サフィックスは中括弧内の任意のログフィールドを参照できます。デフォルトはmd5署名フィールドに対応します。 </p> <p>デフォルト：<span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>詳細モードでは、生成された要求URLを<span class="codeph"> stdout </span>に出力します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h  </span> </p> </td> 
  <td class="stentry"> <p>書式を<span class="codeph"> stdout </span>に出力します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method — 使用するHTTPリクエストメソッド( <span class="codeph"> get|post|head|smart </span>)。 </p> <p>デフォルト：<span class="codeph"> smart </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos — 元のメソッドを取得するログファイル内のpos。 </p> <p>デフォルト：15 </p> </td> 
 </tr> 
</table>

Windowsの場合、ファイル名は[!DNL playlog.bat]で、Linuxの場合は[!DNL playlog.sh]です。

## 例 {#section-716e5c35e9fa4ee3a4b0687381fcea40}

次の例は、Linux上の画像サービングで作成されたアクセスログファイルからのすべての要求を再生します。

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

次のコマンドは、Windowsの画像サービングによって作成されたトレースログファイルで見つかったすべての要求を再生します。

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
