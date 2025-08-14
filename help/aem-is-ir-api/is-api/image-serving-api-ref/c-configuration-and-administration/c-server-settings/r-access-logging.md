---
description: これらのサーバー設定を使用して、アクセスをログに記録します。
solution: Experience Manager
title: アクセスログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e677a617-115d-4f6e-9eb5-bdc14ad7ff24
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# アクセスログ{#access-logging}

これらのサーバー設定を使用して、アクセスをログに記録します。

構文

## TC::directory - ログファイルのフォルダ {#section-5d9e2168d4504bbe9868b7d6051c9d67}

[!DNL Platform Server] がログファイルを書き込むフォルダー。 絶対パスまたは *`install_folder`* に対する相対パスを指定できます。 デフォルトは [!DNL  *`install_folder`*/logs] です。

>[!NOTE]
>
>この設定を変更する前に、新規フォルダーを作成する必要があります。 root 以外のユーザー・アカウントでイメージ・サービングを実行するには、フォルダに適切な読み取り/書き込みアクセス権限があることを確認します。

## TC::maxDays - ログファイルを保存する日数 {#section-45cbecffc5694c87b7d5c176a44a4885}

日数のログファイルは保持する必要があります。 新しいログ ファイルは毎日深夜 0 時に作成されます。 このとき、Image Server または Render Server によって書き込まれたファイルを含め、ログ ファイル フォルダ内の指定された日数より古いファイルがすべて削除されます。 初期設定は 10。

## TC::prefix - アクセスログファイル名 {#section-1003856323b844049632710a5a056aa7}

アクセスログデータが書き込まれるファイルの名前プレフィックス。 日付とファイルサフィックス（[!DNL  *`yyyy`*-*`mm`*-*`dd`*.log]）が、指定された文字列に追加されます。 アクセスログファイルの名前は、トレースログファイルの名前とは異なる必要があります。 デフォルトは「`access-`」です。

## TC::pattern - アクセスログのパターン {#section-22775ea85cee444d8a7d7336a3b1feef}

アクセスログレコード [!DNL Platform Server] データパターンを指定します。 パターン文字列は、対応する値に置き換えられる変数を指定します。 パターン文字列内のその他すべての文字は、文字通りログレコードに転送されます。

キャッシュウォームアップユーティリティを使用するには、スペースをフィールドセパレーターとして使用する必要があります。 [!DNL Platform Server] は、フィールド値のすべてのスペースと「%」文字を、それぞれ `%20` と `%25` に置き換えます。

次のパターン変数がサポートされています。

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> パターン </b> </th> 
   <th class="entry"> <b> 説明 </b> </th> 
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
   <td> <p>応答バイト数から HTTP ヘッダーを除外します。ゼロの場合は「」。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>HTTP ヘッダーを除く応答バイト数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>リクエスト処理時間（ミリ秒単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>スレッド id （デバッグ/エラーログエントリの相互参照用）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>日時（<span class="codeph"> <span class="varname"> yyyy </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span> <span class="varname"> HH </span>: <span class="varname"> mm </span>: <span class="varname"> ss </span> 形式） <span class="varname"> SSS </span> オフセット </span> </p> <p> （<span class="varname"> SSS </span> はミリ秒、<span class="varname"> オフセット </span> は GMT 時間オフセット）。この時間値は、応答がクライアントに送信される際にキャプチャされます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>リクエストメソッド（<span class="codeph"> GET </span>、<span class="codeph"> POST </span> など）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>リクエストの重複（同時に処理されるリクエスト数）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>この要求を受信したローカル ポート。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>クエリ文字列（「?」が前に付く） 存在する場合）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>リクエストの最初の行（リクエストメソッド、URI、HTTP バージョン）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>%r <span class="codeph"> と同じ </span> すが、ログ解析の問題を回避するために、URI に制限付き HTTP エンコードを適用します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>HTTP 応答のステータスコード。 </p> </td> 
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
   <td> <p>認証されたリモートユーザー（存在する場合）、それ以外のユーザー''。 </p> </td> 
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
   <td> <p>リクエスト処理時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] キャッシュキー（キャッシュファイルフォルダー/名前）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] キャッシュ管理キーワード：<span class="codeph"> { 再利用済み |が作成されました |が更新されました | リモート | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE |検証済み |無視 |未定義 }</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r </span> </p> </td> 
   <td> <p>応答の MIME タイプ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>コンテキストフォワードが発生する場合の宛先コンテキスト。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r </span> </p> </td> 
   <td> <p>応答ヘッダー値（応答データ <span class="codeph">MD5 署名）の </span> の etag。 </p> </td> 
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
   <td> <p>要求の解析と画像カタログ参照に要した時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r </span> </p> </td> 
   <td> <p>このリクエストがカタログシステムの外部でパスベースのアクセスを試みたかどうかを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r </span> </p> </td> 
   <td> <p>キャッシュエントリを配信したキャッシュクラスター内のピアサーバーの IP アドレス。または <span class="codeph"> CacheUse </span> が REMOTE_CREATED<span class="codeph"> ードでも REMOTE_UPDATED </span> ードでも <span class="codeph"> い場合は「–」 </span> 指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r </span> </p> </td> 
   <td> <p>エラーカテゴリ： </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=エラーなし。 </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=個の画像がサーバーに見つかりません。 </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=IS プロトコルの使用エラーまたは 1 以外のコンテンツエラー。 </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=その他のサーバーエラー。 </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=一時的なサーバー過負荷のため、要求が拒否されました。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r </span> </p> </td> 
   <td> <p><span class="codeph"> req= </span> の大文字の値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r </span> </p> </td> 
   <td> <p>リクエストのメインカタログのルート ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r </span> </p> </td> 
   <td> <p>出力ストリーム [!DNL Platform Server] データを書き込んだ後、応答を送信するのに要する時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r </span> </p> </td> 
   <td> <p>%B <span class="codeph"></span> 似ていますが、304 （変更されていない）応答の値が含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r </span> </p> </td> 
   <td> <p>すべてのルールセット変換後の最終 URL。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpRequestHeader </span>}i </span> </p> </td> 
   <td> <p>指定された HTTP リクエストヘッダーの値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpResponseHeader </span>} </span> </p> </td> 
   <td> <p>指定された HTTP 応答ヘッダーの値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

デフォルトは `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
