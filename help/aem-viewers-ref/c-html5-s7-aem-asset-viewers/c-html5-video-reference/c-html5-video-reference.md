---
description: ビデオビューアは、H.264形式でエンコードされたストリーミングビデオおよびプログレッシブビデオを再生するビデオプレーヤーです。 Scene7 Publishing SystemまたはAEMダイナミックメディアから配信されます。
keywords: responsive
seo-description: ビデオビューアは、H.264形式でエンコードされたストリーミングビデオおよびプログレッシブビデオを再生するビデオプレーヤーです。 Scene7 Publishing SystemまたはAEMダイナミックメディアから配信されます。
seo-title: ビデオ
solution: Experience Manager
title: ビデオ
topic: Dynamic media
uuid: 961a9b99-5892-4ee3-a2df-13e299f5d086
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ビデオ{#video}

ビデオビューアは、H.264形式でエンコードされたストリーミングビデオおよびプログレッシブビデオを再生するビデオプレーヤーです。 Scene7 Publishing SystemまたはAEMダイナミックメディアから配信されます。

必要システム [構成と前提条件を参照してくださ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)い。

単一のビデオとアダプティブビデオセットの両方がサポートされています。 また、ビューアは、外部の場所でホストされているプログレッシブビデオおよびHLSストリームの操作をサポートしています。 HTML5ビデオをサポートするデスクトップとモバイルの両方のWebブラウザーで機能するように設計されています。 また、このビューアは、ビデオコンテンツ、ビデオチャプターナビゲーションおよびソーシャルメディア共有ツールの上に表示されるオプションのクローズドキャプションもサポートします。

ビデオビューアは、基になるシステムがHLS形式をサポートしている場合は常に、初期設定でHLS形式のHTML5ストリーミングビデオ再生を使用します。 HTML5ストリーミングをサポートしていないシステムでは、ビューアはHTML5プログレッシブビデオ配信にフォールバックします。

ビューアタイプ506

## デモURL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## ビデオビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

ビデオビューアは、メインのJavaScriptファイルとヘルパーファイルのセットを表します。1つのJavaScriptには、この特定のビューアで使用されるすべてのビューアSDKコンポーネントが含まれ、ビューアによって実行時にCSSがダウンロードされます。

ビデオビューアは、ISビューアに付属の実稼働用HTMLページを使用して、ポップアップモードで使用できます。 または、ドキュメントに記載されているAPIを使用して、ビューアを埋め込みモードで使用し、ターゲットWebページに統合することもできます。

ビューアの設定とスキン表示のタスクは、他のビューアと同様です。 スキン表示は、すべてカスタムCSSを使用して適用されます。

すべてのビ [ューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 、およびすべ [てのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## ビデオビューアの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

ビデオビューアには、再生/一時停止ボタン、ビデオスクラバのビデオ時間の吹き出し、再生時間/合計時間インジケーター、ボリュームコントロール、フルスクリーンボタン、クローズドキャプションの切り替えなど、ビデオ再生用の一連の標準ユーザインターフェイスコントロールが用意されています。 これらのコントロールはすべて、ビューアのユーザインターフェイスの下部にあるコントロールバーにグループ化されています。

タッチデバイスでは、ハードウェアボタンを使用してのみボリュームを制御できるので、ボリュームコントロールはユーザーインターフェイスに表示されません。

ビューアがポップアップモードで動作している場合、ユーザインターフェイスのフルスクリーンボタンは使用できません。

ビデオチャプタリングがアクティブな場合、ビデオのコンテンツをすばやく移動できます。 ビデオチャプターはビデオスクラバートラックにマーカーとして表示され、マウスをロールオーバーしたり、タッチシステムで1回タップしたりした場合に、チャプタータイトルと関連する説明が表示されます。 ユーザーは、チャプターマーカーをクリックするか、チャプター説明の吹き出しをタップすることで、特定のチャプターをシークできます。

ビューアは、タッチスクリーンとマウスの両方を搭載したWindowsデバイスで、タッチ入力とマウス入力の両方をサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11およびEdge Webブラウザーのみに限定されます。

このビューアは完全にキーボードでアクセスできます。

詳しくは、キーボ [ードのアクセシビリティとナビゲーションを参照してくださ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)い。

## ビデオビューアを使用したソーシャルメディア共有ツール {#section-907d316fe1da4b87abb9775f02464704}

ビデオビューアは、ソーシャルメディア共有ツールをサポートしています。ソーシャルメディア共有ツールは、ユーザーインターフェイスの単一のボタンとして使用でき、ユーザーがクリックまたはタップすると共有ツールバーに展開されます。

共有ツールバーには、Facebook、Twitter、電子メール共有、埋め込みコード共有、リンク共有など、サポートされる共有チャネルの種類別のアイコンが含まれています。 電子メール共有、埋め込み共有またはリンク共有のツールをアクティブにすると、ビューアにモーダルダイアログボックスが表示され、対応するデータ入力フォームが表示されます。 FacebookまたはTwitterを呼び出すと、ソーシャルメディアサービスの標準の共有ダイアログボックスにリダイレクトされます。 また、共有ツールがアクティブになると、ビデオ再生が自動的に一時停止されます。

Webブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは使用できません。

## ビデオビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

Webページが異なると、ビューアの動作に対するニーズが異なります。 Webページをクリックすると、別のブラウザーウィンドウでビューアが開くリンクが表示される場合があります。 ホストページに直接ビューアを埋め込む必要がある場合もあります。 後者の場合は、Webページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するため、ビューアでは、次の3つの主要な操作モードがサポートされています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

複数のビデオを同じページに埋め込む機能は、タブレットおよびモバイルデバイスでサポートされています。 ほとんどの場合、一度に1つのビデオしか再生できません。 あるビデオの再生を開始し、次に別のビデオの再生を試みると、最初のビデオは自動的に一時停止します。 自動一時停止されたビデオは、現在の再生時間を記憶するので、ユーザーはいつでもビデオに戻って再生を再開できます。 唯一の例外は、Android 4.xデバイスのChromeブラウザーでビデオを並行して再生できる点です。

**ポップアップモードについて**

ポップアップモードでは、ビューアはWebブラウザーの別のウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやデバイスの向きが変更された場合は調整されます。

このモードは、モバイルデバイスで最も一般的なモードです。 Webページでは、JavaScript呼び出し、適切に設定された `window.open()` HTML要素、またはその他の適切な方法を使用し `A` てビューアを読み込みます。

ポップアップ操作モードには、標準搭載されたHTMLページを使用することをお勧めします。 これはとい [!DNL VideoViewer.html] う名前で、標準のISビューアのデ [!DNL html5/] プロイ先のサブフォルダーにあります。

[!DNL <s7viewers_root>/html5/VideoViewer.html]

カスタムCSSを適用すると、視覚的なカスタマイズを行うことができます。

次の例は、ビューアを新しいウィンドウで開くHTMLコードの例です。

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブ埋め込みモードについて**

埋め込みモードでは、ビューアは既存のWebページに追加されます。このWebページには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 ビューアは通常、Webページの一部のスペースのみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、また、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用されます。 この選択は、静的ページレイアウトのWebページに最適です。

レスポンシブデザイン埋め込みは、コンテナのサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定していま `DIV`す。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページでのコンテナのサイズ変更の方法に応じて、ビューアの動作が異なりま `DIV`す。 Webページでコンテナの幅のみが設定され、高さは無制限のままの場合、 `DIV`ビューアは、使用されるアセットの縦横比に従って高さを自動的に選択します。 この方法を使用すると、両側のパディングなしで、アセットがビューにぴったりと収まります。 この使用例は、Bootstrap、Foundationなどのレスポンシブデザインレイアウトフレームワークを使用するWebページで最も一般的です。

それ以外の場合は、Webページでビューアのコンテナの幅と高さの両方が設定されている場合、ビューアはその領域のみを占め、Webページのレイアウトで指定されたサイズに従います。 `DIV`良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーウィンドウのサイズに従ってサイズ設定される場合があります。

**固定サイズ埋め込み**

ビューアをWebページに追加するには、次の手順を実行します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナの定義を参照してくだ `DIV`さい。
1. ビューアのサイズの設定
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにスクリプトタグを追加する必要があります。 ビューアのAPIを使用する前に、を必ず含めてくださ [!DNL FlyoutViewer.js]い。 このフ [!DNL FlyoutViewer.js] ァイルは、次に示すように、 [!DNL html5/js/] 標準のISビューアのデプロイ先のサブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

ビューアがAdobe Dynamic Media Classicサーバーの1つにデプロイされ、同じドメインから供給されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobe Dynamic Media Classicサーバーの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScriptファイルのみ `include` を参照する必要があります。 Webページコード内の追加のJavaScriptファイルを参照してはなりません。Webページコードは、ビューアのロジックによって実行時にダウンロードされる可能性があります。 特に、ビューアによって読み込まれたHTML5 SDKライブラリを、コ `Utils.js` ンテキストパス(いわゆる統合SDK `/s7viewers` ) `include`から直接参照しないでください。 この理由は、実行時のViewerライブラリの場 `Utils.js` 所がビューアのロジックで完全に管理され、ビューアのリリース間で位置が変わるからです。 アドビでは、古いバージョンのセカンダリViewerをサーバーに保 `includes` 持していません。
>
>
>その結果、新しい製品バージョンがデプロイされると、ビューアで使用さ `include` れるセカンダリJavaScriptへの直接参照をページに配置すると、将来、ビューアの機能が機能しなくなります。

1. コンテナDIVの定義を参照してください。

   ビューアを表示するページに空のDIV要素を追加します。 このIDは後でビューアのAPIに渡されるので、DIV要素のIDを定義する必要があります。 DIVのサイズはCSSで指定されます。

   プレースホルダDIVは、位置固定要素です。つまり、 `position` CSSプロパティがまたはに設定さ `relative` れていま `absolute`す。

   フルスクリーン機能がInternet Explorerで正しく機能することを確認します。 DOM内に、プレースホルダーDIVよりも重ね順の高い要素がないことを確認します。

   プレースホルダDIV要素の定義例を次に示します。

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. ビューアのサイズの設定

   ビューアの静的サイズを設定するには、最上位CSSクラスに対して絶 `.s7videoviewer` 対単位で宣言するか、修飾子を使用します `stagesize`。

   CSSのサイズ調整は、HTMLページまたはカスタムビューアのCSSファイルに適用できます。このCSSファイルは、後でScene7 Publishing Systemのビューアプリセットレコードに割り当てられるか、styleコマンドを使用して明示的に渡されます。

   CSSを使用し [たビューアのスタイル設定について詳しくは](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) 、ビデオビューアのカスタマイズを参照してください。

   HTMLページで静的ビューアサイズを定義する例を次に示します。

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   修飾子は、Scene7 Publishing System `stagesize` のビューアプリセットレコードで設定するか、ビューア初期化コードでコレクションを使用して明示的に渡すか、または次に示すコマンドリファレンスの節で説明する `params` API呼び出しとして渡すことができます。

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   CSSベースのアプローチを推奨し、この例で使用します。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報をコ `s7viewers.VideoViewer` ンストラクターに渡し、ビューアインスタンスでメソッド `init()` を呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアのコン `containerId` テナIDの名前と、ビューアでサポートされている設定パラメータを含むネストされた `params` JSONオブジェクトを保持するフィールドが必要です。 この場合、オブジェクト `params` には、プロパティとして渡された画像サービングURL、プロパティとして渡されたビデ `serverUrl` オサーバーURL、および初期アセットをパラ `videoserverurl` メーターとして持つ必要があ `asset` ります。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、起動できます。

   ビューアのコンテナをDOMに追加し、ビューアのコードがIDでコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Webページの最後までDOMの構築が遅れます。 互換性を最大にするには、終了 `init()` タグの直前、またはbodyイベ `BODY` ントでメソッドを呼び出す必要があ `onload()` ります。

   同時に、コンテナ要素は、まだWebページレイアウトの一部ではない必要があります。 例えば、割り当てられたスタイルを使用して非表 `display:none` 示にすることができます。 この場合、Webページがコンテナ要素をレイアウトに戻す瞬間まで、ビューアは初期化処理を遅延します。 この場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、メソッドを呼び出 `init()` します。 この例では、がビ `videoViewer` ューアインスタンスで、がプ `s7viewer` レースホルダー名、が画像サービ `DIV`ングURL、 [!DNL http://s7d1.scene7.com/is/image/] がビデオサーバーURL、 [!DNL http://s7d1.scene7.com/is/content/] がアセットであると [!DNL Scene7SharedAssets/Glacier_Climber_MP4] 仮定しています。

   ```
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   次のコードは、固定サイズのビデオビューアを埋め込んだ簡単なWebページの例です。

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**高さ無制限のレスポンシブデザイン埋め込み**

レスポンシブデザイン埋め込みでは、Webページには通常、ビューアのコンテナの実行時のサイズを指示する柔軟なレイアウトが指定されていま `DIV`す。 この例では、WebページでビューアのコンテナがWebブラウザーのウィンドウサイズの40%を占めることを許可し、高さ `DIV` は無制限のままにしていると仮定します。 WebページのHTMLコードは次のようになります。

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

このようなページへのビューアの追加方法は、固定サイズ埋め込みと非常に似ています。唯一の違いは、ビューアのサイズを明示的に定義する必要がないことです。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVの定義を参照してください。
1. ビューアを作成し、初期化する。

上記の手順は、固定サイズ埋め込みの場合と同じです。 既存の「ホ `DIV` ルダー」にコンテナを追加しま `DIV`す。 次のコードは完全な例です。 ブラウザのサイズが変更されたときにビューアのサイズが変化する様子、ビューアの縦横比がアセットと一致する様子を確認できます。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用方法を説明しています。

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**幅と高さが定義されたレスポンシブデザイン埋め込み**

幅と高さが定義されたレスポンシブデザイン埋め込みの場合、Webページのスタイル設定は異なります。「holder」に両方のサイズを提供し、ブラウ `DIV` ザーウィンドウの中央に配置します。 また、Webページでは、要素と要素のサイズを100% `HTML` に設 `BODY` 定しています。

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**セッターベースのAPIを使用した埋め込み**

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用すると、コンストラクターはパラメーターを受け取らず、設定パラメーターは、 `setContainerId()`、、、お `setParam()`よび `setAsset()` APIメソッドを別々のJavaScript呼び出しで使用して指定します。

次の例は、セッターベースのAPIを使用した固定サイズ埋め込みを示しています。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var videoViewer = new s7viewers.VideoViewer(); 
videoViewer.setContainerId("s7viewer"); 
videoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
videoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
videoViewer.setAsset("Scene7SharedAssets/Glacier_Climber_MP4"); 
videoViewer.init(); 
</script> 
</body> 
</html> 
```

