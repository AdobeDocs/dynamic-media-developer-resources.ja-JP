---
description: ビデオビューアは、H.264形式でエンコードされたストリーミングビデオおよびプログレッシブビデオを再生するビデオプレーヤーです。 Scene7出版システムやAEMDynamic Mediaから配信。
keywords: responsive
seo-description: ビデオビューアは、H.264形式でエンコードされたストリーミングビデオおよびプログレッシブビデオを再生するビデオプレーヤーです。 Scene7出版システムやAEMDynamic Mediaから配信。
seo-title: ビデオ
solution: Experience Manager
title: ビデオ
topic: Dynamic media
uuid: 961a9b99-5892-4ee3-a2df-13e299f5d086
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2402'
ht-degree: 0%

---


# ビデオ{#video}

ビデオビューアは、H.264形式でエンコードされたストリーミングビデオおよびプログレッシブビデオを再生するビデオプレーヤーです。 Scene7出版システムやAEMDynamic Mediaから配信。

[必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

単一のビデオとアダプティブビデオセットの両方がサポートされています。 また、ビューアでは、外部の場所でホストされているプログレッシブビデオおよびHLSストリームの操作もサポートされています。 HTML5ビデオをサポートするデスクトップとモバイルの両方のWebブラウザーで機能するように設計されています。 このビューアは、ビデオコンテンツの上部に表示されるオプションのクローズドキャプション、ビデオチャプターナビゲーションおよびソーシャルメディア共有ツールもサポートしています。

ビデオビューアは、基になるシステムでサポートされている場合は常に、初期設定でHLS形式のHTML5ストリーミングビデオ再生を使用します。 HTML5ストリーミングをサポートしていないシステムでは、ビューアはHTML5プログレッシブビデオ配信にフォールバックされます。

ビューアタイプ506

## デモURL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## ビデオビューアの使用{#section-f21ac23d3f6449ad9765588d69584772}

ビデオビューアは、メインのJavaScriptファイルとヘルパーファイルのセットです。1つのJavaScriptインクルードで、ビューアによって使用されるすべてのビューアSDKコンポーネント、アセット、CSSが実行時にダウンロードされます。

ビデオビューアは、ISビューアに付属の、運用に対応しているHTMLページを使用して、ポップアップモードで使用できます。 または、ドキュメントに記載されているAPIを使用してターゲットのWebページに統合されたビューアを埋め込みモードで使用できます。

ビューアの設定とスキン表示のタスクは、他のビューアと同様です。 スキン表示はすべて、カスタムCSSを使用して適用します。

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)と[すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください。

## ビデオビューアの操作{#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

ビデオビューアには、再生/一時停止ボタン、ビデオスクラバーのビデオ時間の吹き出し、再生時間/合計時間インジケーター、ボリュームコントロール、フルスクリーンボタン、クローズドキャプションの切り替えなど、ビデオ再生用の一連の標準ユーザインターフェイスコントロールがあります。 ビューアユーザインターフェイスの下部にあるコントロールバーに、すべてのコントロールがグループ別に表示されます。

タッチデバイスでは、ハードウェアボタンを使用したボリュームの制御のみが可能なので、ボリュームコントロールはユーザーインターフェイスに表示されません。

ビューアがポップアップモードで動作している場合は、ユーザインターフェイスのフルスクリーンボタンは使用できません。

ビデオチャプター機能がアクティブな場合は、ビデオのコンテンツ間をすばやく移動できます。 ビデオチャプターはビデオスクラバートラック内にマーカーとして表示され、マウスをロールオーバーするか、タッチシステムで1回タップすると、チャプタータイトルと関連する説明が表示されます。 ユーザーは、チャプターマーカーをクリックするか、チャプター説明の吹き出しをタップすることで、特定のチャプターにシークできます。

ビューアは、タッチスクリーンとマウスを備えたWindowsデバイスで、タッチ入力とマウス入力の両方をサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11およびEdgeのWebブラウザーにのみ制限されます。

このビューアは完全にキーボードでアクセスできます。

[キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## ビデオビューアを使用したソーシャルメディア共有ツール{#section-907d316fe1da4b87abb9775f02464704}

ビデオビューアは、ソーシャルメディア共有ツールをサポートしています。ソーシャルメディア共有ツールは、ユーザーインターフェイスの1つのボタンとして使用でき、ユーザーがクリックまたはタップすると共有ツールバーに展開されます。

共有ツールバーには、Facebook、Twitter、電子メール共有、埋め込みコード共有、リンク共有など、サポートされる共有チャネルの種類別アイコンが表示されます。 電子メール共有、埋め込み共有またはリンク共有のツールをアクティブにすると、ビューアにモーダルダイアログボックスが開き、対応するデータ入力フォームが表示されます。 FacebookまたはTwitterを呼び出すと、ソーシャルメディアサービスの標準の共有ダイアログボックスにリダイレクトされます。 また、共有ツールがアクティブになると、ビデオ再生は自動的に一時停止します。

Webブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは使用できません。

## ビデオビューアの埋め込み{#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Webページごとに異なります。 Webページにリンクが表示される場合があります。リンクをクリックすると、別のブラウザーウィンドウでビューアが開きます。 ホストページ上に直接ビューアを埋め込む必要がある場合もあります。 後者の場合は、Webページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは主に次の3つの操作モードがサポートされています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

複数のビデオを同じページに埋め込む機能は、タブレットと携帯端末でサポートされています。 ほとんどの場合、一度に1つのビデオしか再生できません。 あるビデオの再生中に開始がを行い、次に別のビデオの再生を試みると、最初のビデオが自動的に一時停止します。 自動一時停止されたビデオは、現在の再生時間を記憶するので、ユーザーはいつでもビデオに戻って再生を再開できます。 唯一の例外は、Android 4.xデバイスのChromeブラウザーでビデオを並行して再生できる点です。

**ポップアップモードについて**

ポップアップモードでは、ビューアはWebブラウザーの別のウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやデバイスの向きが変更された場合は調整されます。

このモードは、モバイルデバイスで最も一般的です。 Webページでは、`window.open()` JavaScript呼び出し、適切に設定された`A` HTML要素またはその他の適切な方法を使用してビューアを読み込みます。

ポップアップ操作モードには、標準搭載されたHTMLページを使用することをお勧めします。 このページは[!DNL VideoViewer.html]と呼ばれ、標準のIS-Viewersデプロイメントの[!DNL html5/]サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/VideoViewer.html]

カスタムCSSを適用すると、視覚的なカスタマイズを行うことができます。

次の例は、ビューアを新しいウィンドウに開くHTMLコードの例です。

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブ埋め込みモードについて**

埋め込みモードでは、ビューアは既存のWebページに追加されます。このWebページには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 ビューアは通常、Webページの一部のスペースのみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、また、デバイスの種類に従ってレイアウトを自動調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 静的ページレイアウトのWebページには、この選択肢が最適です。

レスポンシブデザイン埋め込みは、コンテナ`DIV`のサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定しています。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナのサイズ変更`DIV`によって、ビューアの動作が異なります。 Webページでコンテナ`DIV`の幅のみが設定され、高さは無制限のままの場合、ビューアでは、使用するアセットの縦横比に従って高さが自動的に選択されます。 この方法により、両側のパディングなしで、アセットは表示にぴったりと収まります。 この使用例は、Bootstrap、Foundationなどのレスポンシブデザインレイアウトフレームワークを使用するWebページで最も一般的です。

それ以外の場合は、Webページでビューアのコンテナ`DIV`の幅と高さの両方が設定されている場合、ビューアはその領域だけを占め、Webページのレイアウトで指定されているサイズに従います。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーウィンドウのサイズに従ってサイズ設定される場合があります。

**固定サイズ埋め込み**

ビューアは、次の操作を行ってWebページに追加します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナ`DIV`を定義しています。
1. ビューアのサイズを設定する。
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにスクリプトタグを追加する必要があります。 ビューアのAPIを使用するには、[!DNL FlyoutViewer.js]を必ず含めます。 [!DNL FlyoutViewer.js]ファイルは、次に示すように、IS-Viewersの標準のデプロイ先の[!DNL html5/js/]サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

ビューアがAdobeのDynamic Mediaクラシックサーバの1つにデプロイされ、同じドメインから供給されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobeDynamic Mediaクラシックサーバの1つへのフルパスを指定します。

相対パスの例を次に示します。

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScript `include`ファイルのみを参照してください。 Webページコード内で、ビューアのロジックによって実行時にダウンロードされる可能性のある追加のJavaScriptファイルは、参照しないでください。 特に、ビューアによって読み込まれたHTML5 SDK `Utils.js`ライブラリを`/s7viewers`コンテキストパスから直接参照しないでください（いわゆる統合SDK `include`）。 理由は、`Utils.js`や類似のランタイムビューアライブラリの場所がビューアのロジックで完全に管理され、ビューアのリリース間で場所が変化するからです。 Adobeでは、古いバージョンのセカンダリビューア`includes`はサーバに保持されません。
>
>
>その結果、新しい製品バージョンがデプロイされる際に、ビューアが使用する任意のセカンダリJavaScript `include`への直接参照をページ上に置くと、ビューアの機能が将来的に機能しなくなります。

1. コンテナDIVを定義する。

   ビューア追加を表示するページの空のDIV要素。 DIV要素は、IDが定義されている必要があります。このIDを、後でビューアのAPIに渡します。 DIVのサイズはCSSで指定します。

   プレースホルダDIVは位置固定要素です。つまり、`position` CSSプロパティは`relative`または`absolute`に設定されます。

   フルスクリーン機能がInternet Explorerで正しく機能することを確認します。 プレースホルダDIVよりも重ね順の高い他の要素がDOM内にないことを確認します。

   プレースホルダDIV要素の定義例を次に示します。

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. ビューアのサイズの設定

   ビューアの静的サイズを設定するには、最上位CSSクラスに対して絶対単位で`.s7videoviewer`宣言するか、修飾子`stagesize`を使用します。

   CSS内のサイズ調整は、HTMLページまたはカスタムビューアのCSSファイルに配置できます。このCSSファイルは、後でScene7パブリッシングシステムでビューアプリセットレコードに割り当てるか、styleコマンドを使用して明示的に渡します。

   CSSを使用したビューアのスタイル設定について詳しくは、[ビデオビューアのカスタマイズ](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e)を参照してください。

   以下は、HTMLページで静的ビューアサイズを定義する例です。

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   `stagesize`修飾子は、Scene7Publishing Systemのビューアプリセットレコードで設定するか、`params`コレクションでビューア初期化コードで明示的に渡すか、次のコマンドリファレンスの説明に従ってAPI呼び出しで渡すことができます。

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   CSSベースのアプローチを推奨し、この例では使用します。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、`s7viewers.VideoViewer`クラスのインスタンスを作成し、すべての設定情報をコンストラクターに渡して、ビューアインスタンスで`init()`メソッドを呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 最低でも、このオブジェクトには`containerId`フィールドが存在し、ビューアのコンテナIDの名前と、ビューアでサポートされている設定パラメーターを含むネストされた`params` JSONオブジェクトが含まれている必要があります。 この場合、`params`オブジェクトには、`serverUrl`プロパティとして渡された画像サービングURL、`videoserverurl`プロパティとして渡されたビデオサーバーURL、および`asset`パラメーターとしての初期アセットが最低限必要です。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、開始できます。

   ビューアのコンテナをDOMに追加して、ビューアのコードがIDでコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Webページが終わるまでDOMの構築が遅れます。 互換性を最大にするには、`init()`メソッドを終了`BODY`タグの直前、または本文`onload()`イベントで呼び出します。

   同時に、コンテナ要素がまだWebページレイアウトの一部である必要はありません。 例えば、`display:none`スタイルを割り当てて非表示にすることができます。 この場合、Webページからコンテナ要素がレイアウトに戻る瞬間まで、ビューアは初期化プロセスを遅延します。 この場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、`init()`メソッドを呼び出します。 この例では、`videoViewer`をビューアインスタンス、`s7viewer`をプレースホルダー`DIV`の名前、[!DNL http://s7d1.scene7.com/is/image/]を画像サービングURL、[!DNL http://s7d1.scene7.com/is/content/]をビデオサーバーURL、[!DNL Scene7SharedAssets/Glacier_Climber_MP4]をアセットと仮定しています。

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

レスポンシブデザイン埋め込みでは、Webページには通常、ビューアのコンテナ`DIV`の実行時のサイズを指示する柔軟なレイアウトが指定されています。 この例では、Webページでビューアのコンテナ`DIV`がWebブラウザーのウィンドウサイズの40%を占めることを許可し、高さは無制限のままにすると仮定します。 WebページのHTMLコードは次のようになります。

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

このようなページへのビューアの追加方法は、固定サイズ埋め込みの場合と非常に似ています。唯一の違いは、ビューアのサイズを明示的に定義する必要がないことです。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVを定義する。
1. ビューアを作成し、初期化する。

上記の手順はすべて、固定サイズ埋め込みの場合と同じです。 追加コンテナ`DIV`を既存の&quot;holder&quot; `DIV`に対して送信します。 次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化する様子、ビューアの縦横比がアセットと一致する様子を確認できます。

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

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**幅と高さが定義されたレスポンシブデザイン埋め込み**

幅と高さが定義されたレスポンシブデザイン埋め込みの場合、Webページのスタイリングは異なります。&quot;holder&quot; `DIV`に両方のサイズを提供し、ブラウザーウィンドウの中央に配置します。 また、Webページでは、`HTML`要素と`BODY`要素のサイズを100%に設定します。

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

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIでは、コンストラクターにパラメーターは不要です。設定パラメーターは、`setContainerId()`、`setParam()`および`setAsset()`の各APIメソッドを別々のJavaScript呼び出しで使用して指定します。

次の例は、セッターベースのAPIを使用する固定サイズ埋め込みを示します。

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

