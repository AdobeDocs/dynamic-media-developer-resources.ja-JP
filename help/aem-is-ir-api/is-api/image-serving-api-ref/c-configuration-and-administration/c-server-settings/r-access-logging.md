---
description: これらのサーバー設定を使用して、アクセスのログを記録します。
solution: Experience Manager
title: アクセスログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e677a617-115d-4f6e-9eb5-bdc14ad7ff24
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 3%

---

# アクセスログ{#access-logging}

これらのサーバー設定を使用して、アクセスのログを記録します。

構文

## TC::directory — ログファイルフォルダ {#section-5d9e2168d4504bbe9868b7d6051c9d67}

次の場所にあるフォルダー： [!DNL Platform Server] はログファイルを書き込みます。 絶対パスまたは次の値を基準とした相対パスを指定できます。 *`install_folder`*. デフォルトはです。 [!DNL  *`install_folder`*/logs].

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダを作成する必要があります。 画像サービングがインストールされ、root 以外のユーザーアカウントで実行されるようにフォルダーに読み取り/書き込みアクセス権が設定されていることを確認します。

## TC::maxDays — ログファイルを保持する日数 {#section-45cbecffc5694c87b7d5c176a44a4885}

ログファイルを保存する日数。 新しいログファイルは、毎日午前 0 時に作成されます。 この時点で、サーバは、Image Server または Render Server が書き込んだファイルを含め、指定した日数より古いログファイルフォルダ内のすべてのファイルを削除します。 初期設定は 10 です

## TC::prefix — アクセスログファイル名 {#section-1003856323b844049632710a5a056aa7}

アクセスログデータの書き込み先のファイルの名前プレフィックス。 日付とファイルサフィックス ( [!DNL  *`yyyy`*-*`mm`*-*`dd`*.log]) を指定した文字列に追加します。 アクセスログファイルの名前は、トレースログファイルの名前とは異なる名前にする必要があります。 初期設定は &quot; `access-`&quot;.

## TC::pattern — アクセスログパターン {#section-22775ea85cee444d8a7d7336a3b1feef}

次のデータパターンを指定： [!DNL Platform Server] ログレコードにアクセスします。 パターン文字列は、対応する値で置き換えられる変数を指定します。 パターン文字列内のその他の文字はすべて、リテラルとしてログレコードに転送されます。

キャッシュウォームアップユーティリティを使用するには、フィールドの区切り文字としてスペースを使用する必要があります。 The [!DNL Platform Server] フィールド値内のすべてのスペースおよび「%」文字を `%20` および `%25`、それぞれ。

次のパターン変数がサポートされています。

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>パターン</b> </th> 
   <th class="entry"> <b>説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> %a </span> </p> </td> 
   <td> <p>リモート IP アドレス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %A </span> </p> </td> 
   <td> <p>ローカル IP アドレス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b </span> </p> </td> 
   <td> <p>HTTP ヘッダーを除く応答バイト数。0 の場合は「 」。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>HTTP ヘッダーを除く応答バイト数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>リクエストの処理時間（ミリ秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>スレッド id （デバッグ/エラーログエントリを相互参照するため）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>日付と時刻、形式 <span class="codeph"> <span class="varname"> yyyy </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span> <span class="varname"> HH </span>: <span class="varname"> mm </span>: <span class="varname"> ss </span>. <span class="varname"> SSS </span> オフセット </span> </p> <p> ( <span class="varname"> SSS </span> はミリ秒です。 <span class="varname"> オフセット </span> は GMT 時間オフセット )。応答がクライアントに送信される際に時間値が取り込まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>リクエストメソッド ( <span class="codeph"> GET </span>, <span class="codeph"> POST </span>など ) を含める必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>リクエストの重複（同時に処理されたリクエストの数）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>このリクエストが受信されたローカルポート。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>クエリ文字列（先頭に「?」が付く） （存在する場合）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>要求の最初の行（要求メソッド、URI、HTTP バージョン）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>次と同じ <span class="codeph"> %r </span>を使用しますが、ログの解析の問題を回避するために、URI に対して制限付き HTTP エンコードが適用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>HTTP 応答ステータスコード。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S </span> </p> </td> 
   <td> <p>ユーザーセッション ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>日付と時刻（共通ログ形式）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>認証されたリモートユーザー（存在する場合）、それ以外の場合は「 」。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>URI パス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v </span> </p> </td> 
   <td> <p>ローカルサーバー名。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T </span> </p> </td> 
   <td> <p>リクエストの処理時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] キャッシュキー（キャッシュファイルのフォルダー/名前）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] キャッシュ管理キーワード： <span class="codeph"> { 再利用済み |作成済み |更新済み | REMOTE | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE |検証済み |無視 | UNDEFINED } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r </span> </p> </td> 
   <td> <p>応答の MIME タイプ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>コンテキストが転送された場合の宛先コンテキスト。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r </span> </p> </td> 
   <td> <p>The <span class="codeph"> etag </span> 応答ヘッダー値（応答データの MD5 署名）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r </span> </p> </td> 
   <td> <p>エラーメッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r </span> </p> </td> 
   <td> <p>Image Server からキャッシュエントリまたはデータを取得するのにかかる時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r </span> </p> </td> 
   <td> <p>リクエストの解析および画像カタログ参照に要した時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r </span> </p> </td> 
   <td> <p>この要求がカタログシステム外でパスベースのアクセスを試みたかどうかを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r </span> </p> </td> 
   <td> <p>キャッシュエントリを配信したキャッシュクラスター内のピアサーバーの IP アドレス。 <span class="codeph"> CacheUse </span> 次のいずれでもない <span class="codeph"> REMOTE_CREATED </span> nor <span class="codeph"> REMOTE_UPDATED </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r </span> </p> </td> 
   <td> <p>エラーカテゴリ： </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0 =エラーなし。 </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1 =画像がサーバーで見つかりません。 </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=IS プロトコル使用エラー、または 1 以外のコンテンツエラー。 </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=その他のサーバーエラー。 </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=一時的なサーバー負荷が原因でリクエストが拒否されました。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r </span> </p> </td> 
   <td> <p>の大文字の値 <span class="codeph"> req= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r </span> </p> </td> 
   <td> <p>リクエストのメインカタログのルート ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r </span> </p> </td> 
   <td> <p>所要時間 [!DNL Platform Server] データを出力ストリームに書き込んだ後に応答を送信する。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r </span> </p> </td> 
   <td> <p>次に類似 <span class="codeph"> %B </span>には値が含まれますが、304（変更なし）応答の値が含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r </span> </p> </td> 
   <td> <p>すべての ruleset 変換後の最終 URL。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpRequestHeader </span>}i </span> </p> </td> 
   <td> <p>指定した HTTP リクエストヘッダーの値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpResponseHeader </span>} </span> </p> </td> 
   <td> <p>指定した HTTP 応答ヘッダーの値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

初期設定は です`"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
