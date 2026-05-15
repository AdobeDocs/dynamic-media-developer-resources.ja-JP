---
description: playlog ユーティリティを使用して、HTTP応答キャッシュのコンテンツを事前生成できます。
solution: Experience Manager
title: 「playlog」ユーティリティ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0213978-3a1d-44b4-82bf-4527b980b29e
TQID: 'https://experienceleague.adobe.com/z8SkpY0A2aAo5ULL61m5uUiesuovSrcVjhzNRGbkAUQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 437
ht-degree: 0%

---

# 「playlog」ユーティリティ{#the-playlog-utility}

playlog ユーティリティを使用して、HTTP応答キャッシュのコンテンツを事前生成できます。

既存のImage Serving HTTP応答キャッシュは、メジャーバージョンのアップグレード後（バージョン番号の1桁または2桁が変更された場合）に使用できることが保証されていません。 アップグレード後にサーバーをフルロード状態に移行する場合、キャッシュが適正に設定され、キャッシュヒット率が上がるまで、サーバーはキャッシュミス要求の最初の数時間を処理して過負荷になる可能性があります。

この最初の読み込みスパイクを回避するために、`playlog` ユーティリティを使用して、HTTP応答キャッシュのコンテンツを事前生成できます。 `playlog`は、既存のアクセス ログ ファイルからHTTP リクエストを抽出し、それをサーバーに送信してキャッシュ エントリを生成します。 一般的な使用シナリオでは、1日分のトラフィックを含む1つのアクセスログファイルを再生するだけで十分です。

アップグレードのインストール後にHTTP応答キャッシュをプライミングすることに加えて、このユーティリティは、新しいサーバーを負荷分散環境に追加する際にキャッシュ内容を事前生成するために使用されます。他のサーバーの1つから最近のログファイルを再生するだけです。

`playlog`は、以前のバージョンの画像サービングで生成されたほとんどのアクセス ログ ファイルをサポートするように設定できます。

## 使用方法 {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p <span class="varname"> プレフィックス </span> </span> </p> </td> 
  <td class="stentry"> <p>ログファイルから抽出されたリクエストの先頭に付けるルート URL。 </p> <p>デフォルト：<span class="filepath"> http://localhost:8080/is </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname"> col </span> </span> </p> </td> 
  <td class="stentry"> <p>ログレコード内のリクエストを含むフィールド（列）番号（1 ベース）。 </p> <p>デフォルト：16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s <span class="varname">区切り記号</span> </span> </p> </td> 
  <td class="stentry"> <p>フィールド区切り記号。正規表現パターン。 </p> <p>デフォルト：<span class="codeph"> [ ]+ </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m <span class="varname"> マーカー</span> </span> </p> </td> 
  <td class="stentry"> <p>リクエストマーカー。再生するログファイル内のリクエストを識別します。正規表現パターン。 </p> <p>既定：<span class="codeph"> リクエスト：</span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x <span class="varname"> サフィックス </span> </span> </p> </td> 
  <td class="stentry"> <p>ログファイルから抽出されたリクエストに追加するサフィックス。再生されたリクエストをログファイル内のライブリクエストから分離するために使用できます。「?」または「&amp;」区切り記号が自動的に挿入されます。サフィックスは、中括弧の中の位置によって任意のログフィールドを参照できます。デフォルトはmd5署名フィールドに対応します。 </p> <p>デフォルト：<span class="codeph"> playlog={25} </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>詳細モードで、生成されたリクエスト URLを<span class="codeph"> stdout </span>に出力します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> – 時間</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">標準出力</span>への書式を印刷します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method – 使用するHTTP リクエストメソッド （<span class="codeph"> get|post|head|smart </span>）。 </p> <p>デフォルト：<span class="codeph"> スマート </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - ログファイル内のposから元のメソッドを取得します。 </p> <p>デフォルト：15 </p> </td> 
 </tr> 
</table>

Windowsの場合、ファイル名は[!DNL playlog.bat]、Linuxの場合は[!DNL playlog.sh]です。

## 例 {#section-716e5c35e9fa4ee3a4b0687381fcea40}

次の例では、LinuxでImage Servingによって作成されたアクセスログファイルからのすべてのリクエストを再生します。

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

次のコマンドは、Windows上のImage Servingによって作成されたトレース ログ ファイルで見つかったすべてのリクエストを再生します。

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
