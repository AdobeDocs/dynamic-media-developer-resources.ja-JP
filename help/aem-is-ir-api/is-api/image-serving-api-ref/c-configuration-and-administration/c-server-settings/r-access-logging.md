---
description: これらのサーバー設定を使用してアクセスをログに記録します。
solution: Experience Manager
title: アクセスログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e677a617-115d-4f6e-9eb5-bdc14ad7ff24
TQID: 'https://experienceleague.adobe.com/YY1vKXzVCe8TRK0lYsdkH5ds5EHCGkBOz1TaMx5IMi4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 681
ht-degree: 0%

---

# アクセスログ{#access-logging}

これらのサーバー設定を使用してアクセスをログに記録します。

構文

## TC::directory - Log File Folder {#section-5d9e2168d4504bbe9868b7d6051c9d67}

[!DNL Platform Server]がログファイルを書き込むフォルダー。 これは、*`install_folder`*&#x200B;に対する絶対パスまたは相対パスにすることができます。 デフォルトは&#x200B;[!DNL &#x200B; *`install_folder`*/logs]です。

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダーを作成する必要があります。 Image Servingがroot以外のユーザーアカウントで実行されるようにインストールされている場合は、フォルダーに正しい読み取り/書き込みアクセス権限があることを確認してください。

## TC::maxDays - ログファイルを保持する日数 {#section-45cbecffc5694c87b7d5c176a44a4885}

ログファイルの日数を保持する必要があります。 毎日、真夜中に新しいログファイルが作成されます。 この時点で、サーバーは、指定された日数より古いログファイルフォルダー内のすべてのファイルを削除します。これには、Image ServerまたはRender Serverによって書き込まれたものも含まれます。 デフォルトは10です。

## TC::prefix - Access Log File Name {#section-1003856323b844049632710a5a056aa7}

アクセス ログ データが書き込まれるファイルの名前プレフィックス。 日付とファイルのサフィックス （[!DNL &#x200B; *`yyyy`*-*`mm`*-*`dd`*.log]）が、指定された文字列に追加されます。 アクセス ログ ファイルの名前は、トレース ログ ファイルの名前とは異なる必要があります。 デフォルトは「`access-`」です。

## TC::pattern - Access Log Pattern {#section-22775ea85cee444d8a7d7336a3b1feef}

[!DNL Platform Server] アクセス ログ レコードのデータ パターンを指定します。 パターン文字列は、対応する値で置換される変数を指定します。 パターン文字列内の他のすべての文字は、ログレコードに文字通り転送されます。

キャッシュウォームアップユーティリティを使用するには、スペースをフィールド区切り文字として使用する必要があります。 [!DNL Platform Server]は、フィールド値のすべてのスペースと&#39;%&#39;文字をそれぞれ`%20`と`%25`に置き換えます。

次のパターン変数がサポートされています。

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> パターン </b> </th> 
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
   <td> <p>HTTP ヘッダーを除く応答バイト数、または0の場合は「」。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>HTTP ヘッダーを除く応答バイト数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>リクエスト処理時間（ミリ秒単位）: </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>スレッド id （相互参照デバッグ/エラーログエントリ用）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>日付と時刻。形式：<span class="codeph"> <span class="varname"> yyyy </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span> <span class="varname"> HH </span>: <span class="varname"> mm </span>: <span class="varname"> ss </span>。<span class="varname"> SSS </span> オフセット </span> </p> <p> （<span class="varname"> SSS </span>はミリ秒、<span class="varname"> オフセット </span>はGMT時間オフセット）。応答がクライアントに送信されたときに時間値が取得されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>リクエストメソッド （<span class="codeph"> GET </span>、<span class="codeph"> POST </span>など）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>リクエストの重複（同時に処理されたリクエスト数）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>この要求を受信したローカル ポート。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>クエリー文字列（存在する場合は「?」が先頭に付きます）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>リクエストの最初の行（リクエストメソッド、URI、HTTP バージョン）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p><span class="codeph"> %r </span>と同じですが、ログ解析の問題を回避するために、URIに制限されたHTTP エンコーディングを適用します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>HTTP応答ステータスコード。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S </span> </p> </td> 
   <td> <p>ユーザーセッション ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>共通ログ形式の日時。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>認証されたリモートユーザー（存在する場合）、それ以外の場合「。 </p> </td> 
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
   <td> <p>[!DNL Platform Server] キャッシュ管理キーワード：<span class="codeph"> { REUSED | CREATED | UPDATED | REMOTE | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE | VALIDATED | IGNORED | UNDEFINED } </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r </span> </p> </td> 
   <td> <p>応答のMIME タイプ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>コンテキスト転送が発生した場合の宛先コンテキスト。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r </span> </p> </td> 
   <td> <p><span class="codeph"> etag </span>応答ヘッダー値（応答データのMD5署名）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r </span> </p> </td> 
   <td> <p>エラーメッセージ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r </span> </p> </td> 
   <td> <p>Image Serverからキャッシュエントリまたはデータを取得するのにかかった時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r </span> </p> </td> 
   <td> <p>リクエストの解析と画像カタログの検索にかかる時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r </span> </p> </td> 
   <td> <p>このリクエストがカタログシステム外でのパスベースのアクセスを試みたかどうかを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r </span> </p> </td> 
   <td> <p>キャッシュエントリを配信したキャッシュクラスター内のピアサーバーのIP アドレス、または<span class="codeph"> CacheUse </span>が<span class="codeph"> REMOTE_CREATED </span>でも<span class="codeph"> REMOTE_UPDATED </span>でもない場合は「 – 」。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r </span> </p> </td> 
   <td> <p>エラーのカテゴリ： </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=エラーなし。 </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=画像がサーバー上に見つかりません。 </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=IS プロトコル使用エラーまたは1以外のコンテンツエラー。 </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=その他のサーバーエラー。 </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=一時的なサーバーの過負荷が原因でリクエストが拒否されました。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r </span> </p> </td> 
   <td> <p>大文字の値<span class="codeph"> req= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r </span> </p> </td> 
   <td> <p>リクエストのメインカタログのルート ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r </span> </p> </td> 
   <td> <p>データを出力ストリームに書き込んだ後に応答を送信するのに[!DNL Platform Server]かかる時間です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r </span> </p> </td> 
   <td> <p><span class="codeph"> %B </span>と同様ですが、304 （変更なし）応答の値が含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r </span> </p> </td> 
   <td> <p>すべてのルールセット変換の後の最終的なURL。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpRequestHeader </span>}i </span> </p> </td> 
   <td> <p>指定されたHTTP リクエストヘッダーの値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpResponseHeader </span>} </span> </p> </td> 
   <td> <p>指定されたHTTP応答ヘッダーの値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

デフォルトは`"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`です
