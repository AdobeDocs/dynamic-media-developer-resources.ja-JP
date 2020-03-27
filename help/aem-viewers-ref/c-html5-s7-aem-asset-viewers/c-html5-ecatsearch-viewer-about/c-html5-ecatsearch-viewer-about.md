---
description: eCatalog検索ビューアは、見開き別またはページ別の見開き別に電子パンフレットを表示するカタログビューアです。eCatalogを使用すると、追加のユーザインターフェイス要素または専用のサムネールモードを使用してカタログ内を移動できます。 また、各ページをズームインして詳細を表示することもできます。
keywords: responsive
seo-description: eCatalog検索ビューアは、見開き別またはページ別の見開き別に電子パンフレットを表示するカタログビューアです。eCatalogを使用すると、追加のユーザインターフェイス要素または専用のサムネールモードを使用してカタログ内を移動できます。 また、各ページをズームインして詳細を表示することもできます。
seo-title: eCatalog検索
solution: Experience Manager
title: eCatalog検索
topic: Dynamic media
uuid: f5ec33bf-e827-4709-9780-6f17096bf306
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# eCatalog検索{#ecatalog-search}

eCatalog検索ビューアは、見開き別またはページ別の見開き別に電子パンフレットを表示するカタログビューアです。eCatalogを使用すると、追加のユーザインターフェイス要素または専用のサムネールモードを使用してカタログ内を移動できます。 また、各ページをズームインして詳細を表示することもできます。

このビューアはeCatalogで機能し、オプションの画像マップとソーシャル共有ツールをサポートします。 ズームツール、カタログナビゲーションツール、フルスクリーンのサポート、サムネール、およびオプションの閉じるボタンがあります。 Viewerは、ソーシャル共有ツール、印刷、ダウンロードおよびお気に入りもサポートしています。 デスクトップや携帯端末で動作するように設計されています。

また、ユーザは、カタログのコンテンツに対して、キーワードベースまたはフレーズベースの検索を行うこともできます。

>[!NOTE]
>
>IR（画像レンダリング）またはUGC（ユーザ生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアタイプ513

必要システム [構成と前提条件を参照してくださ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)い。

## デモURL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/)

## eCatalogビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalog検索ビューアは、メインのJavaScriptファイルと、ビューアによって実行時にダウンロードされるヘルパーファイルのセット（この特定のビューアで使用されるすべてのビューアSDKコンポーネントを含む1つのJavaScriptが含まれる）です

eCatalog検索ビューアは、ISビューアに付属の実稼動用HTMLページを使用するか、埋め込みモードで使用できます。このモードでは、ドキュメントに記載されたAPIを使用して、eCatalog検索ビューアをターゲットWebページに統合します。

設定とスキン表示は、他のビューアと同様です。 スキン表示は、すべてカスタムCSSを使用して適用されます。

すべてのビ [ューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 、およびすべ [てのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## eCatalog検索ビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

eCatalog検索ビューアは、他のモバイルアプリケーションで一般的な次のタッチジェスチャに対応しています。

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
   <td colname="col2"> <p> スウォッチ内の新しいサムネールを選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ダブルタップ </p> </td> 
   <td colname="col2"> <p> 最大倍率に達するまで1レベルズームインします。 次のダブルタップジェスチャでは、ビューアが初期表示状態にリセットされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ピンチ </p> </td> 
   <td colname="col2"> <p>ズームインまたはズームアウトします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p>スライドフレームのトランジションが使用されている場合に、カタログページのリストをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直方向のスワイプまたはフリック </p> </td> 
   <td colname="col2"> <p>画像がリセット状態の場合、ネイティブページスクロールを実行します。 </p> <p>サムネールがアクティブな場合は、サムネールのリストをスクロールします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

カタログページ間を移動する際に、リアルなページフリップアニメーション効果を有効にすることができます。 この場合、ユーザーはページの隅を押したままドラッグし、ページをめくることができます。

このビューアは、タッチスクリーンとマウスを備えたWindowsデバイスでのタッチ入力とマウス入力の両方もサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11およびEdge Webブラウザーのみに限定されます。

## eCatalog検索ビューアを使用したソーシャルメディア共有ツール {#section-eb575084a99647c3a9591f439f40b412}

eCatalog検索ビューアでは、ソーシャルシェアツールがサポートされています。ソーシャルシェアツールは、メインコントロールバーのボタンとして使用でき、ユーザーがクリックまたはタップすると共有ツールバーに展開されます。

共有ツールバーには、Facebook、Twitter、電子メール共有、埋め込みコード共有、リンク共有など、サポートされる共有チャネルの種類別のアイコンが表示されます。 電子メール共有、埋め込み共有またはリンク共有のツールをアクティブにすると、ビューアにモーダルダイアログボックスが表示され、対応するデータ入力フォームが表示されます。 FacebookまたはTwitterを呼び出すと、ソーシャルサービスの標準の共有ダイアログにリダイレクトされます。 Webブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは使用できません。

Viewerの検索機能は、メインツールバーの鏡のアイコンとして使用できます。 アイコンをクリックまたはタップすると、入力フィールドを含む検索パネルがアクティブになります。 キーワードまたはフレーズを入力してEnterキーを押すと、検索結果がパネルにレンダリングされ、メインビューで見つかった単語がハイライトされます。

## eCatalog検索ビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

Webページが異なると、ビューアの動作に対するニーズが異なります。 Webページをクリックすると、別のブラウザーウィンドウでビューアを開くリンクが表示される場合があります。 ホストページにビューアを直接埋め込む必要がある場合もあります。 後者の場合は、Webページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するため、ビューアでは、次の3つの主要な操作モードがサポートされています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

**ポップアップモードについて**

ポップアップモードでは、ビューアはWebブラウザーの別のウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやモバイルデバイスの向きが変更された場合は調整されます。

ポップアップモードは、モバイルデバイスで最も一般的なモードです。 Webページでは、JavaScriptの呼び出し、適切に設定された `window.open()` HTML要素、またはその他の適切な方法を使用し `A` てビューアを読み込みます。

ポップアップ操作モードには、標準搭載されたHTMLページを使用することをお勧めします。 この場合、このISビューアは、とい [!DNL eCatalogSearchViewer.html] う名前で、標準のISビューアのデプ [!DNL html5/] ロイ先のサブフォルダー内にあります。

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

カスタムCSSを適用すると、視覚的なカスタマイズを行うことができます。

次の例は、ビューアを新しいウィンドウで開くHTMLコードの例です。

```
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存のWebページに追加されます。このWebページには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 ビューアは通常、Webページの一部のスペースのみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、また、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用されます。 これは、静的レイアウトのWebページに最適な選択肢です。

レスポンシブデザイン埋め込みは、コンテナのサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定していま `DIV`す。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナのサイズ変更の方法に応じて、ビューアの動作が異なりま `DIV`す。 Webページでコンテナの幅のみが設定され、高さは無制限のままの場合、 `DIV`ビューアは、使用されるアセットの縦横比に従って高さを自動的に選択します。 この機能により、両側のパディングなしで、アセットが表示範囲にぴったりと収まるようになります。 この使用例は、Bootstrap、Foundationなどのレスポンシブレイアウトフレームワークを使用するWebページで最も一般的です。

それ以外の場合は、Webページでビューアのコンテナの幅と高さの両方が設定されている場合、ビューアはその領域のみを占め、Webページのレイアウトで指定されているサイズに従います。 `DIV`良い例は、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合です。

**固定サイズ埋め込み**

ビューアをWebページに追加するには、次の手順を実行します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVの定義を参照してください。
1. ビューアのサイズの設定
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにスクリプトタグを追加する必要があります。 ビューアのAPIを使用する前に、を必ず含めてくださ [!DNL eCatalogSearchViewer.js]い。 このフ [!DNL eCatalogSearchViewer.js] ァイルは、次に示すように、 [!DNL html5/js/] 標準のISビューアのデプロイ先のサブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

ビューアがAdobe Scene7サーバの1つにデプロイされ、同じドメインから供給されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobe Scene7サーバの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
```

1. コンテナDIVの定義を参照してください。

   ビューアを表示するページに空のDIV要素を追加します。 このIDは後でビューアのAPIに渡されるので、DIV要素のIDを定義する必要があります。

   プレースホルダDIVは、位置固定要素です。つまり、 `position` CSSプロパティがまたはに設定さ `relative` れていま `absolute`す。

   プレースホルダDIV要素の定義例を次に示します。

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアのサイズの設定

   ビューアの静的サイズを設定するには、最上位CSSクラスに対して絶 `.s7ecatalogsearchviewer` 対単位で宣言するか、修飾子を使用し `stagesize` ます。

   サイズ調整は、HTMLページ上のCSS、またはカスタムビューアのCSSファイルに直接配置し、後でScene7 Publishing Systemのビューアプリセットレコードに割り当てるか、styleコマンドを使用して明示的に渡すことができます。

   CSSを使用した [ビューアのスタイル設定について詳しくは](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 、eCatalogビューアのカスタマイズを参照してください。

   HTMLページで静的ビューアサイズを定義する例を次に示します。

   ```
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   修飾子は、Scene7 Publishing Systemのビ `stagesize` ューアプリセットレコードで設定するか、ビューア初期化コードでコレクションと共に明示的に渡すか、または次のようにコマンドリファレンスの節で説明する `params` API呼び出しとして渡すことができます。

   ```
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. ビューアを初期化する。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報をコ `s7viewers.eCatalogSearchViewer` ンストラクターに渡して、ビューアインスタンスでメソッド `init()` を呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアの `containerId` コンテナIDの名前と、ビューアでサポートされている設定パラメータを含むネストされた `params` JSONオブジェクトを保持するフィールドがあります。 この場合、オブジェクトに `params` は、プロパティとして渡された画像サービングURLが少なくとも含まれて `serverUrl` おり、最初のアセットがパラメーターとして含まれている必要が `asset` あります。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、起動できます。

   ビューアのコンテナをDOMに追加し、ビューアのコードがIDでコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Webページの最後までDOMの構築が遅れます。 互換性を最大限に高めるには、終了タ `init()` グの直前、またはbodyイベ `BODY` ントでメソッドを呼び出す必要があ `onload()` ります。

   同時に、コンテナ要素は、まだWebページレイアウトの一部ではありません。 例えば、割り当てられたスタイルを使用して非表 `display:none` 示にすることができます。 この場合、Webページがコンテナ要素をレイアウトに戻す瞬間まで、ビューアは初期化処理を遅延します。 この場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、必要最小限の設定オプションをコンストラクターに渡して、メソッドを呼び出 `init()` します。 この例では、がビューアイ `eCatalogSearchViewer` ンスタンスであると仮定しています。はプレ `s7viewer` ースホルダの名前で `DIV`す。は画 `http://s7d1.scene7.com/is/image/` 像サービングのURLで、はア `Viewers/Pluralist` セットです。

   ```
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "searchserverurl":"http://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、固定サイズのeCatalog検索ビューアを埋め込んだ簡単なWebページの例です。

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "searchserverurl":"http://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高さ無制限のレスポンシブデザイン埋め込み**

レスポンシブデザイン埋め込みでは、Webページには通常、ビューアのコンテナの実行時のサイズを指示する柔軟なレイアウトが指定されていま `DIV`す。 この例では、WebページでビューアのコンテナがWebブラウザーのウィンドウサイズの40%を占めることを許可し、高さ `DIV` は無制限のままにしていると仮定します。 結果のWebページのHTMLコードは次のようになります。

```
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

このようなページへのビューアの追加方法は、固定サイズ埋め込みと似ていますが、唯一の違いは、ビューアサイズを明示的に定義する必要がない点です。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVの定義を参照してください。
1. ビューアを作成し、初期化する。

上記の手順は、固定サイズ埋め込みの場合と同じです。 コンテナを既存の「 `DIV` holder」に追加しま `DIV`す。 次のコードは完全な例です。 ブラウザのサイズが変更されたときにビューアのサイズが変化する様子、ビューアの縦横比がアセットと一致する様子を確認できます。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "searchserverurl":"http://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下のサンプルページは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用例を示しています。

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**幅と高さが定義されたフレキシブルサイズ埋め込み**

幅と高さが定義されたフレキシブルサイズ埋め込みの場合、Webページのスタイルは異なります。 つまり、「holder」に両方のサイズを提供し、ブラウザー `DIV` ウィンドウの中央に配置します。 また、Webページでは、要素と要素のサイズを100% `HTML` に設 `BODY` 定しています。

```
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

残りの埋め込み手順は、高さ無制限のレスポンシブデザイン埋め込みと同じです。 結果の例を次に示します。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "searchserverurl":"http://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**セッターベースのAPIを使用した埋め込み**

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合、コンストラクターはパラメーターを受け取らず、設定パラメーターは、、、および `setContainerId()`APIメソッド `setParam()`を別々のJavaScript呼び出しで使用 `setAsset()` して指定されます。

次の例は、セッターベースのAPIを使用した固定サイズ埋め込みを示しています。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
eCatalogSearchViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
eCatalogSearchViewer.setParam("searchserverurl", "http://s7search1.scene7.com/s7search/"); 
eCatalogSearchViewer.setAsset("Viewers/Pluralist"); 
eCatalogSearchViewer.init(); 
</script> 
</body> 
</html>
```

