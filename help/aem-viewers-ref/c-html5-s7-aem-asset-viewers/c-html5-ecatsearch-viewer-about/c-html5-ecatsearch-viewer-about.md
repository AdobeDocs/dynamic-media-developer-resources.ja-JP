---
description: eCatalog Search Viewerは、電子パンフレットをスプレッド別またはページ別に表示するカタログビューアです。 eCatalogでは、追加のユーザーインターフェイス要素または専用のサムネールモードを使用して、カタログ内を移動できます。 利用者は、各ページをズームインして詳細を確認することもできます。
keywords: responsive
solution: Experience Manager
title: e カタログ検索
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 915e628e-65e7-44c6-a2aa-d4ae7ed03b8e
TQID: 'https://experienceleague.adobe.com/rQEr1uCyFrCErLcSvoOTvolSJID0D-sHYYSTDMc-pPQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 2191
ht-degree: 0%

---

# e カタログ検索{#ecatalog-search}

eCatalog Search Viewerは、電子パンフレットをスプレッド別またはページ別に表示するカタログビューアです。 eCatalogでは、追加のユーザーインターフェイス要素または専用のサムネールモードを使用して、カタログ内を移動できます。 利用者は、各ページをズームインして詳細を確認することもできます。

このビューアはecatalogsで動作し、オプションの画像マップとソーシャル共有ツールをサポートしています。 ズームツール、カタログナビゲーションツール、フルスクリーンサポート、サムネール、オプションの閉じるボタンがあります。 ビューアは、ソーシャル共有ツール、印刷、ダウンロード、お気に入りもサポートしています。 デスクトップやモバイルデバイスで動作するように設計されています。

ユーザは、カタログのコンテンツに対してキーワードベースまたはフレーズに基づく検索を行うこともできる。

>[!NOTE]
>
>IR （画像レンダリング）またはUGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアータイプ 513。

[必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/)


## eCatalog Viewerの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalog Search Viewerは、メインのJavaScript ファイルと一連のヘルパーファイルを表します（1つのJavaScriptには、この特定のビューア、アセット、CSSで使用されるすべてのビューア SDK コンポーネントが含まれています）。実行時にビューアがダウンロードします

ECatalog Search Viewerは、IS-Viewersを備えた実稼動対応のHTML ページを使用してポップアップモードで使用したり、埋め込みモードで使用したりできます。このページは、文書化されたAPIを使用してターゲット web ページに統合されます。

設定とスキニングは、他のビューアと同様です。 すべてのスキニングは、カスタム CSSを使用して実行できます。

すべてのビューアに共通する[&#x200B; コマンド参照 – 構成属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通するコマンド参照 – URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください

## eCatalog Search Viewerの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

eCatalog Search Viewerは、他のモバイルアプリケーションで一般的な次のタッチジェスチャーをサポートしています。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ジェスチャ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>シングルタップ </p> </td> 
   <td colname="col2"> <p> スウォッチで新しいサムネールを選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ダブルタップ </p> </td> 
   <td colname="col2"> <p> 最大の倍率に達するまで1 レベルでズームします。 次のダブルタップジェスチャーは、ビューアを初期表示状態にリセットします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ピンチ </p> </td> 
   <td colname="col2"> <p>ズームインまたはズームアウト </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p>スライドフレームの切り替えが使用されている場合は、カタログページのリストをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p>画像がリセット状態の場合、ネイティブページスクロールが実行されます。 </p> <p>サムネールがアクティブな場合、サムネールのリストがスクロールされます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

カタログページ間を移動する際に、リアルなページ反転アニメーション効果を有効にすることができます。 この場合、ユーザーはページの角を保持してドラッグし、ページを反転させることができます。

このビューアは、タッチスクリーンとマウスを使用したWindows デバイスでのタッチ入力とマウス入力の両方をサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11、およびEdgeのweb ブラウザーのみに限定されます。

## e カタログ検索ビューアを使用したソーシャルメディア共有ツール {#section-eb575084a99647c3a9591f439f40b412}

eCatalog Search Viewerは、ソーシャル共有ツールをサポートしています。 これらは、ユーザーが共有ツールバーをクリックまたはタップしたときに共有ツールバーに展開されるメインコントロールバーのボタンとして使用できます。

共有ツールバーには、Facebook、Twitter、メール共有、埋め込みコード共有、リンク共有など、サポートされている共有チャネルのタイプごとにアイコンが含まれています。 メール共有、埋め込み共有またはリンク共有ツールがアクティブ化されると、対応するデータ入力フォームを含むモーダルダイアログボックスがビューアに表示されます。 FacebookまたはTwitterが呼び出されると、ビューアはソーシャルサービスから標準の共有ダイアログにユーザーをリダイレクトします。 Web ブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは利用できません。

ビューアの検索機能は、メインツールバーのルックグラスアイコンとして使用できます。 アイコンをクリックまたはタップすると、入力フィールドを含む検索パネルがアクティブになります。 キーワードまたはフレーズを入力してEnter キーを押すと、ビューアは検索結果をパネルにレンダリングし、見つかった単語をメインビューにハイライト表示します。

## eCatalog Search Viewerの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

web ページごとに、閲覧者の行動に対するニーズは異なります。 Web ページでリンクが提供される場合があります。このリンクを選択すると、別のブラウザーウィンドウでビューアが開きます。 それ以外の場合は、ビューアをホスティングページに直接埋め込む必要があります。 後者の場合、web ページは静的なページレイアウトを使用するか、異なるデバイスまたは異なるブラウザーウィンドウのサイズに対して異なる表示を行うレスポンシブデザインを使用します。 これらのニーズに対応するために、ビューアでは、ポップアップ、固定サイズの埋め込み、レスポンシブデザインの埋め込みという3つの主要な操作モードをサポートしています。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別のweb ブラウザーウィンドウまたはタブで開きます。 ブラウザーのサイズが変更されたり、モバイルデバイスの向きが変更されたりすると、ブラウザーのウィンドウ領域全体が調整されます。

ポップアップモードは、モバイルデバイスで最も一般的です。 Web ページは、`window.open()` JavaScript呼び出し、`A` HTML要素の適切な設定、またはその他の適切なメソッドを使用してビューアを読み込みます。

ポップアップ操作モードには、標準のHTML ページを使用することをお勧めします。 この場合は[!DNL eCatalogSearchViewer.html]と呼ばれ、標準のIS-Viewers デプロイメントの[!DNL html5/] サブフォルダー内にあります。

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

カスタム CSSを適用すると、視覚的なカスタマイズを実現できます。

次に、新しいウィンドウでビューアを開くHTML コードの例を示します。

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアが既存のweb ページに追加されます。このweb ページには、ビューアに関連しない顧客コンテンツが既に含まれている可能性があります。 通常、閲覧者はweb ページの不動産の一部しか占めていません。

主なユースケースは、デスクトップ PCやタブレットデバイス向けのweb ページです。デバイスの種類に応じてレイアウトを自動的に調整する、レスポンシブデザインのページも使用できます。

初期読み込み後にビューアのサイズが変更されない場合は、固定サイズ埋め込みが使用されます。 これは、静的レイアウトを使用するweb ページに最適です。

レスポンシブデザイン埋め込みは、コンテナ `DIV`のサイズ変更に応じて、実行時にビューアのサイズ変更が必要になる場合があることを前提としています。 最も一般的なユースケースは、柔軟性の高いページレイアウトを使用するweb ページにビューアを追加することです。

レスポンシブデザイン埋め込みモードでは、web ページのサイズとコンテナ `DIV`のサイズによって、ビューアの動作が異なります。 Web ページがコンテナ `DIV`の幅のみを設定し、高さを制限しない場合、ビューアは使用されるアセットの縦横比に応じて自動的に高さを選択します。 この機能により、側面にパディングすることなく、アセットをビューに完全に収めることができます。 このユースケースは、BootstrapやFoundationなどのレスポンシブレイアウトフレームワークを使用するweb ページで最も一般的です。

それ以外の場合、web ページがビューアのコンテナ `DIV`の幅と高さの両方を設定すると、ビューアはその領域だけを塗りつぶし、web ページレイアウトが提供するサイズに従います。 良い例は、ビューアをモーダルオーバーレイに埋め込むことです。このオーバーレイは、web ブラウザーのウィンドウサイズに応じてサイズが調整されます。

**固定サイズ埋め込み**

次の操作を実行して、ビューアをweb ページに追加します。

1. ビューアのJavaScript ファイルをweb ページに追加します。
1. コンテナ DIVの定義。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. ビューアのJavaScript ファイルをweb ページに追加します。

   ビューアを作成するには、HTML ヘッドにスクリプトタグを追加する必要があります。 ビューアーAPIを使用する前に、[!DNL eCatalogSearchViewer.js]を含めることを確認してください。 [!DNL eCatalogSearchViewer.js] ファイルは、標準のIS-Viewers デプロイメントの[!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

ビューアがAdobe Dynamic Media サーバーのいずれかにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-ViewersがインストールされているAdobe Dynamic Media サーバーの1つにフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
```

1. コンテナ DIVの定義。

   ビューアを表示するページに、空のDIV エレメントを追加します。 このIDは後でビューア APIに渡されるので、DIV要素にはIDが定義されている必要があります。

   プレースホルダーDIVは配置された要素です。`position` CSS プロパティが`relative`または`absolute`に設定されていることを意味します。

   次に、定義済みのプレースホルダーDIV要素の例を示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアサイズの設定

   ビューアの静的サイズは、`.s7ecatalogsearchviewer` トップレベル CSS クラスを絶対単位で宣言するか、`stagesize`修飾子を使用することで設定できます。

   CSSでは、HTML ページに直接、またはカスタムビューア CSS ファイルにサイズを設定できます。このファイルは、後でDynamic Media Classicのビューアプリセットレコードに割り当てられるか、スタイルコマンドを使用して明示的に渡されます。

   CSSを使用したビューアのスタイル設定について詳しくは、[eCatalog ビューアのカスタマイズ &#x200B;](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)を参照してください。

   次に、HTML ページの静的ビューアサイズを定義する例を示します。

   ```html {.line-numbers}
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   `stagesize`修飾子は、Dynamic Media Classicのビューアプリセットレコードで設定するか、`params` コレクションを使用してビューアの初期化コードで明示的に渡すか、コマンドリファレンスの節で説明されているように、次のようにAPI呼び出しとして渡すことができます。

   ```html {.line-numbers}
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. ビューアの初期化。

   上記の手順を完了したら、`s7viewers.eCatalogSearchViewer` クラスのインスタンスを作成し、すべての構成情報をそのコンストラクターに渡し、ビューアーインスタンスで`init()` メソッドを呼び出します。 構成情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアコンテナ IDの名前を保持する`containerId` フィールドと、ビューアがサポートする設定パラメーターを含むネストされた`params` JSON オブジェクトがあります。 この場合、`params` オブジェクトには、少なくとも`serverUrl` プロパティとして渡された画像サービング URLと、`asset` パラメーターとして最初のアセットが必要です。 JSON ベースの初期化APIを使用すると、1行のコードでビューアを作成および開始できます。

   ビューアコードがIDでコンテナ要素を見つけられるように、ビューアコンテナをDOMに追加することが重要です。 一部のブラウザーは、Web ページの最後までDOMの構築を遅らせます。 ただし、互換性を最大限に高めるには、終了`BODY` タグの直前または本文`onload()` イベントで`init()` メソッドを呼び出します。

   同時に、コンテナ要素はまだ必ずしもweb ページレイアウトの一部である必要はありません。 例えば、割り当てられた`display:none` スタイルを使用して非表示にすることができます。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで初期化プロセスを遅らせます。 これが発生すると、ビューアの読み込みが自動的に再開されます。

   次に、ビューアーインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡し、`init()` メソッドを呼び出す例を示します。 この例では、`eCatalogSearchViewer`がビューアインスタンスであると仮定します。`s7viewer`はプレースホルダー`DIV`の名前、`https://s7d1.scene7.com/is/image/`は画像サービング URL、`Viewers/Pluralist`はアセットです。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、eCatalog Search Viewerを固定サイズで埋め込む面倒なweb ページの完全な例です。

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高さの制限のないレスポンシブデザイン埋め込み**

レスポンシブデザインの埋め込みでは、通常、web ページには、ビューアのコンテナ `DIV`のランタイムサイズを決定する、ある種の柔軟なレイアウトが配置されています。 この例では、web ページでビューアのコンテナ `DIV`がweb ブラウザーのウィンドウ サイズの40%を使用でき、高さは制限されないと仮定します。 結果のweb ページのHTML コードは次のようになります。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

このようなページにビューアを追加することは、固定サイズの埋め込みと似ていますが、唯一の違いは、ビューアサイズを明示的に定義する必要がないことです。

1. ビューアのJavaScript ファイルをweb ページに追加します。
1. コンテナ DIVの定義。
1. ビューアの作成と初期化。

上記のすべての手順は、固定サイズ埋め込みと同じです。 コンテナ `DIV`を既存の「ホルダー」 `DIV`に追加します。 次のコードは、完全な例です。 ブラウザーのサイズを変更するとビューアサイズがどのように変化するか、およびビューアの縦横比がアセットとどのように一致するかを確認できます。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

次のサンプルページでは、高さに制限のないレスポンシブデザイン埋め込みをより実際に使用する例を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**幅と高さが定義された柔軟なサイズ埋め込み**

幅と高さが定義された柔軟なサイズの埋め込みの場合、web ページのスタイル設定は異なります。 つまり、「ホルダー」に両方のサイズを提供し、ブラウザーウィンドウに中央に配置します。 `DIV`また、web ページでは、`HTML`要素と`BODY`要素のサイズを100%に設定しています。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

残りの埋め込み手順は、高さの制限のないレスポンシブデザイン埋め込みと同じです。 結果として得られる例は次のとおりです。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Setter ベースのAPIを使用した埋め込み**

JSON ベースの初期化を使用する代わりに、セッターベースのAPIとno-args コンストラクターを使用できます。 このAPI コンストラクターではパラメーターを使用せず、設定パラメーターは`setContainerId()`、`setParam()`、`setAsset()`のAPI メソッドを使用して指定され、別々のJavaScript呼び出しが行われます。

次の例は、setter ベースのAPIを使用した固定サイズの埋め込みを示しています。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogsearchviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer(); 
eCatalogSearchViewer.setContainerId("s7viewer"); 
eCatalogSearchViewer.setParam("serverurl", "https://s7d1.scene7.com/is/image/"); 
eCatalogSearchViewer.setParam("searchserverurl", "https://s7search1.scene7.com/s7search/"); 
eCatalogSearchViewer.setAsset("Viewers/Pluralist"); 
eCatalogSearchViewer.init(); 
</script> 
</body> 
</html>
```

