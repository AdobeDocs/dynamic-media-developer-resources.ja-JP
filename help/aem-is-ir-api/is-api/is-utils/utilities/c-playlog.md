---
description: 再生ログユーティリティを使用して、HTTP 応答キャッシュのコンテンツを事前に生成できます。
solution: Experience Manager
title: 「playlog」ユーティリティ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0213978-3a1d-44b4-82bf-4527b980b29e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# 「playlog」ユーティリティ{#the-playlog-utility}

再生ログユーティリティを使用して、HTTP 応答キャッシュのコンテンツを事前に生成できます。

既存のイメージサービング HTTP 応答キャッシュは、メジャーバージョンのアップグレード後（バージョン番号の最初または 2 番目の桁が変更された場合）、使用可能であることは保証されません。 アップグレード後にサーバーをフルロード状態にする場合は、キャッシュに適度なデータが入力され、キャッシュヒット率が増加するまで、キャッシュミスリクエストの最初の数時間を処理して、サーバーがオーバーロードされる可能性があります。

この初期負荷スパイクを回避するには、`playlog` ユーティリティを使用して HTTP 応答キャッシュのコンテンツを事前生成します。 `playlog` は、既存のアクセスログファイルから HTTP リクエストを抽出し、サーバーに送信してキャッシュエントリを生成します。 一般的な使用シナリオでは、1 日分のトラフィックを含んだ単一のアクセスログファイルを再生するだけで十分です。

このユーティリティは、アップグレードのインストール後に HTTP 応答キャッシュにデータを書き込むだけでなく、新しいサーバを負荷分散された環境に追加するときに、キャッシュの内容を事前に生成するためにも使用されます。その場合は、単に他のいずれかのサーバから最新のログ ファイルを再生します。

`playlog` は、以前のバージョンの画像サービングで生成されたほとんどのアクセスログファイルをサポートするように設定できます。

## 使用方法 {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p <span class="varname"> プレフィックス </span> </span> </p> </td> 
  <td class="stentry"> <p>ログファイルから抽出されたリクエストの先頭に追加されるルート URL。 </p> <p>デフォルト：<span class="filepath"> http://localhost:8080/is </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname"> col </span> </span> </p> </td> 
  <td class="stentry"> <p>ログレコードにリクエストを含むフィールド（列）の番号（1 から始まります）。 </p> <p>デフォルト：16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s <span class="varname"> 区切り記号 </span> </span> </p> </td> 
  <td class="stentry"> <p>フィールドの区切り記号。正規表現のパターンです。 </p> <p>デフォルト：<span class="codeph"> [ ]+ </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m <span class="varname"> マーカー </span> </span> </p> </td> 
  <td class="stentry"> <p>リクエストマーカー。ログファイル内で再生されるリクエストを識別します。正規表現パターン。 </p> <p>デフォルト：<span class="codeph"> リクエスト：</span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x <span class="varname"> サフィックス </span> </span> </p> </td> 
  <td class="stentry"> <p>ログファイルから抽出されたリクエストに追加するサフィックス。ログファイル内のライブリクエストから再生されたリクエストを分離するために使用できます。「?」 または「&amp;」区切り記号が自動的に挿入されます。サフィックスは、中括弧内の位置によって任意のログフィールドを参照できます。デフォルトは md5 署名フィールドに対応しています。 </p> <p>デフォルト：<span class="codeph"> playlog={25} </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>詳細モードで、生成されたリクエスト URL を stdout </span> に出力 <span class="codeph"> ます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>stdout </span> に書式 <span class="codeph"> 出力します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method – 使用する HTTP リクエストメソッド （<span class="codeph"> get|post|head|smart </span>）。 </p> <p>デフォルト：<span class="codeph"> smart </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos – 元のメソッドを取得するログファイル内の場所。 </p> <p>デフォルト：15 </p> </td> 
 </tr> 
</table>

Windows の場合、ファイル名は [!DNL playlog.bat] で、Linux の場合は [!DNL playlog.sh] です。

## 例 {#section-716e5c35e9fa4ee3a4b0687381fcea40}

次の例では、Linux の画像サービングで作成されたアクセスログファイルからのすべてのリクエストを再生します。

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

次のコマンドは、Windows の画像サービングによって作成されたトレースログファイルで見つかったすべてのリクエストを再生します。

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
