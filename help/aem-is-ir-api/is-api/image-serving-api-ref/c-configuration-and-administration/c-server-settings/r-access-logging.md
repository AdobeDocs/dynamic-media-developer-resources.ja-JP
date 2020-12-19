---
description: アクセスのログ記録には、次のサーバー設定を使用します。
seo-description: アクセスのログ記録には、次のサーバー設定を使用します。
seo-title: アクセスログ
solution: Experience Manager
title: アクセスログ
topic: Scene7 Image Serving - Image Rendering API
uuid: ea7d5d39-3f0a-45f0-bc28-6828a9c9da50
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 4%

---


# アクセスログ{#access-logging}

アクセスのログ記録には、次のサーバー設定を使用します。

構文

## TC::directory — ログファイルフォルダ{#section-5d9e2168d4504bbe9868b7d6051c9d67}

プラットフォームサーバーがログファイルを書き込むフォルダーです。 絶対パスまたは&#x200B;*`install_folder`*&#x200B;を基準とした相対パスを指定できます。 初期設定は&#x200B;[!DNL  *`install_folder`*/logs]です。

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダーを作成する必要があります。 画像サービングがroot以外のユーザーアカウントで実行するようにインストールされている場合は、フォルダーに正しい読み取り/書き込みアクセス権限があることを確認してください。

## TC::maxDays — ログファイルを保持する日数{#section-45cbecffc5694c87b7d5c176a44a4885}

ログファイルを保持する日数。 新しいログファイルは毎日午前0時に作成されます。 この時点で、サーバは、Image ServerまたはRender Serverが書き込むファイルを含め、指定した日数より古いログファイルフォルダ内のすべてのファイルを削除します。 初期設定は 10 です

## TC::prefix — アクセスログファイル名{#section-1003856323b844049632710a5a056aa7}

アクセスログデータの書き込み先となるファイルの名前プレフィックス。 日付とファイルサフィックス([!DNL  *`yyyy`*-*`mm`*-*`dd`*.log])が指定した文字列に追加されます。 アクセスログファイルの名前は、トレースログファイルの名前とは異なる名前にする必要があります。 初期設定は &quot; `access-`&quot;.

## TC::pattern — アクセスログパターン{#section-22775ea85cee444d8a7d7336a3b1feef}

プラットフォームサーバーのアクセスログレコードのデータパターンを指定します。 パターン文字列は、対応する値で置換される変数を指定します。 パターン文字列内のその他すべての文字は、ログレコードに逐語的に転送されます。

キャッシュ・ウォームアップ・ユーティリティを使用するには、フィールドの区切り文字としてスペースを使用する必要があります。 プラットフォームサーバーでは、フィールド値内のスペースと「%」文字がすべて`%20`と`%25`に置き換えられます。

次のパターン変数がサポートされています。

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>分割測光</b> </th> 
   <th class="entry"> <b>説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> %a </span> </p> </td> 
   <td> <p>リモートIPアドレス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %A </span> </p> </td> 
   <td> <p>ローカルIPアドレス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b </span> </p> </td> 
   <td> <p>HTTPヘッダーを除く応答バイト数。0の場合は' '。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>HTTPヘッダーを除く応答バイト数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>リクエストの処理時間（ミリ秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>スレッドID（相互参照するデバッグ/エラーログエントリ用）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>日付と時刻。形式は<span class="codeph"> <span class="varname"> yyyy </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span> <span class="varname"> HH </span>:<span class="varname"> mm </span>:<span class="varname"> ss </span>. <span class="varname"> SSS </span> オフセット  </span> </p> <p> （ <span class="varname"> SSS </span> are msec, <span class="varname"> offset </span>はGMTの時間オフセット）;時間値は、応答がクライアントに送信されたときに取り込まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>リクエストメソッド(<span class="codeph">GET</span>、<span class="codeph">POST</span>など)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>リクエストの重複（同時に処理されるリクエストの数） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>この要求が受信されたローカルポート。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>クエリ文字列（「?」の前に付加） が存在する場合)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>リクエストの最初の行（リクエストメソッド、URI、HTTPバージョン）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p><span class="codeph"> %r </span>と同じですが、ログ解析の問題を回避するために、URIに限定的なHTTPエンコーディングを適用します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>HTTP応答ステータスコード。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S </span> </p> </td> 
   <td> <p>ユーザーセッションID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>日付と時刻（共通ログ形式）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>認証済みのリモートユーザー（存在する場合）、それ以外の場合は". </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>URIパス。 </p> </td> 
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
   <td> <p> <span class="codeph"> %{CacheKey}r  </span> </p> </td> 
   <td> <p>プラットフォームサーバーのキャッシュキー（キャッシュファイルのフォルダー/名前）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r  </span> </p> </td> 
   <td> <p>プラットフォームサーバーのキャッシュ管理キーワード：<span class="codeph"> { REUSED |作成済み |更新済み | REMOTE | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE |検証済み | IGNORED | UNDEFINED } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r  </span> </p> </td> 
   <td> <p>応答のMIMEタイプ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>コンテキストの転送が発生した場合の宛先コンテキスト。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r  </span> </p> </td> 
   <td> <p><span class="codeph"> etag </span>応答ヘッダー値（応答データのMD5署名）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r  </span> </p> </td> 
   <td> <p>エラーメッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r  </span> </p> </td> 
   <td> <p>Image Serverからキャッシュエントリまたはデータを取得するのにかかる時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r  </span> </p> </td> 
   <td> <p>要求の解析および画像カタログ参照に要した時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r  </span> </p> </td> 
   <td> <p>この要求がカタログシステム外でパスベースのアクセスを試みたかどうかを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r  </span> </p> </td> 
   <td> <p><span class="codeph"> CacheUse </span>が<span class="codeph"> REMOTE_CREATED </span>でも<span class="codeph"> REMOTE_UPDATED </span>でもない場合、キャッシュエントリを配信したキャッシュクラスタ内のピアサーバーのIPアドレス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r  </span> </p> </td> 
   <td> <p>エラーカテゴリ: </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=エラーなし。 </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=画像がサーバーで見つかりません。 </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=ISプロトコル使用エラーまたは1以外のコンテンツエラー。 </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=その他のサーバーエラー。 </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=一時的なサーバーの過負荷のため、要求が拒否されました。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r  </span> </p> </td> 
   <td> <p><span class="codeph"> req= </span>の大文字の値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r  </span> </p> </td> 
   <td> <p>要求のメインカタログのルートID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r  </span> </p> </td> 
   <td> <p>出力ストリームにデータを書き込んだ後、プラットフォームサーバーが応答を送信するのにかかる時間です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r  </span> </p> </td> 
   <td> <p><span class="codeph"> %B </span>のように、304（変更されていない）応答の値が含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r  </span> </p> </td> 
   <td> <p>すべてのルールセット変換の後の最終URL。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpRequestHeader  </span>}i  </span> </p> </td> 
   <td> <p>指定したHTTPリクエストヘッダーの値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpResponseHeader  </span>}  </span> </p> </td> 
   <td> <p>指定したHTTP応答ヘッダーの値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

初期設定は です`"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
