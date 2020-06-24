---
description: インタラクティブビデオビューアは、H.264形式でエンコードされたストリーミングビデオおよびプログレッシブビデオを再生するビデオプレーヤーです。
seo-description: インタラクティブビデオビューアは、H.264形式でエンコードされたストリーミングビデオおよびプログレッシブビデオを再生するビデオプレーヤーです。
seo-title: インタラクティブビデオ
solution: Experience Manager
title: インタラクティブビデオ
topic: Dynamic media
uuid: 116c6b40-2490-4f1a-9c76-e06082069cc8
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2243'
ht-degree: 0%

---


# インタラクティブビデオ{#interactive-video}

インタラクティブビデオビューアは、H.264形式でエンコードされたストリーミングビデオおよびプログレッシブビデオを再生するビデオプレーヤーです。

ビューアは、ビデオコンテンツの横にインタラクティブな製品スウォッチも表示します。 単一のビデオとアダプティブビデオセットの両方がサポートされています。 HTML5ビデオをサポートするデスクトップとモバイルの両方のWebブラウザーで機能するように設計されています。 ビューアでは、ビデオコンテンツの上部に表示されるオプションのクローズドキャプション、ビデオチャプターナビゲーションおよびソーシャル共有ツールがサポートされています。 このビューアの目的は、「買い物かご可能なビデオ」エクスペリエンスの実装を支援することです。 つまり、特定のビデオ時間領域に関連付けられたスウォッチを選択して、クイック表示または顧客のWebサイトの製品の詳細ページにリダイレクトできます。

ビューアタイプ510

## デモURL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

と

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html)

## システム要件 {#section-b7270cc4290043399681dc504f043609}

必要 [システム構成を参照してください](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## インタラクティブビデオビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

インタラクティブビデオビューアは、メインのJavaScriptファイルと、ビューアによって実行時にダウンロードされるヘルパーファイルのセット（このビューア、アセットおよびCSSで使用されるすべてのビューアSDKコンポーネントを含む1つのJavaScriptインクルード）です。

インタラクティブビデオビューアは、画像サービングビューアに付属の、運用に対応しているHTMLページを使用して、ポップアップモードで使用できます。 また、ドキュメントに記載されているAPIを使用してターゲットのWebページに統合される埋め込みモードでも使用できます。

設定とスキン表示は、このガイドで説明する他のビューアと同様です。 スキン表示はすべて、カスタム(CSS)カスケーディングスタイルシートを使用して適用されます。

すべてのビューアに共通の [コマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 、およびすべてのビューアに共通の [コマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## インタラクティブビデオビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

インタラクティブビデオビューアには、再生/一時停止ボタン、ビデオスクラバー、ビデオ時間の吹き出し、再生時間/合計時間インジケーター、ボリュームコントロール、フルスクリーンボタン、クローズドキャプションの切り替えなど、ビデオ再生用の一連の標準ユーザインターフェイスコントロールがあります。 これらのコントロールはすべて、メイン表示のすぐ下にあるコントロールバーにグループ化されています。

タッチデバイスでは、ボリュームコントロールはユーザーインターフェイスに表示されません。デバイスのハードウェアボタンを使用してのみボリュームを制御できるからです。

ビューアがポップアップモードで動作している場合は、ユーザインターフェイスのフルスクリーンボタンは使用できません。

ビューアでは、ビデオ表示領域の右側に、インタラクティブスウォッチが含まれたパネルが表示されます。 ビデオの再生時にスウォッチのリストが自動的に進み、現在のビデオ領域に対応するスウォッチが表示されます。 スウォッチをクリックまたはタップすると、オーサリング時にそのスウォッチに関連付けられたアクションがトリガーされます。 設定に応じて、トリガーは、Webサイトの別のページにリダイレクトされたり、製品情報をWebページのロジックに渡して戻すことができ、その結果、関連する製品のコンテンツを示すクイック表示が開くトリガーとなります。

ビデオチャプター機能をアクティブにすると、ビデオコンテンツ間をすばやく移動できます。 ビデオチャプターはビデオスクラバートラックにマーカーとして表示され、ロールオーバー時（タッチシステムでは1回タップした場合）にチャプタータイトルと説明が表示されます。 顧客は、チャプターマーカーをクリックするか、チャプター説明の吹き出しをタップすることで、特定のチャプターを「シーク」できます。

Viewerは、様々なソーシャルメディア共有ツールもサポートしています。 これらのボタンは、ユーザーインターフェイスの1つのボタンとして使用でき、ユーザーがクリックまたはタップしたときに共有ツールバーに展開されます。 共有ツールバーには、Facebook、Twitter、電子メール共有、埋め込みコード共有、リンク共有など、サポートされる共有チャネルの種類別アイコンが表示されます。 電子メール共有、埋め込み共有またはリンク共有のツールをアクティブにすると、ビューアにモーダルダイアログボックスが開き、対応するデータ入力フォームが表示されます。 FacebookまたはTwitterを呼び出すと、ソーシャルメディアサービスの標準の共有ダイアログボックスにリダイレクトされます。 また、共有ツールがアクティブになると、ビデオ再生は自動的に一時停止します。 Webブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは使用できません。

ビューアは完全にキーボードでアクセスできます。 詳しくは、 [キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## インタラクティブビデオビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

インタラクティブビデオビューアは、ホスティングページに埋め込まれるように設計されています。 このようなWebページは静的レイアウトである場合や、「レスポンシブ」で、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わる場合があります。

これらのニーズに対応するために、ビューアでは、主に次の2つの操作モードがサポートされています。 固定サイズ埋め込みとレスポンシブ埋め込み

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存のWebページに追加されます。このWebページには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 ビューアは通常、Webページの一部のスペースのみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、また、デバイスの種類に従ってレイアウトを自動調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 静的レイアウトのWebページには、これが最適です。

レスポンシブデザイン埋め込みは、コンテナのサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定してい `DIV`ます。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナのサイズ変更の方法に応じて、ビューアの動作が異なり `DIV`ます。 Webページでコンテナの幅のみが設定され、高さは無制限のままの場合 `DIV`、ビューアでは、使用するアセットの縦横比に従って高さが自動的に選択されます。 この機能により、両側のパディングなしで、アセットは表示にぴったりと収まります。 この使用例は、Bootstrap、FoundationなどのレスポンシブWebデザインレイアウトフレームワークを使用するWebページで最も一般的です。

また、Webページでビューアのコンテナの幅と高さの両方が設定されている場合 `DIV`、ビューアはその領域全体を占め、Webページのレイアウトと同じサイズに従います。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合があります。

**固定サイズ埋め込み**

ビューアは、次の操作を行ってWebページに追加します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナの定義を参照して `DIV`ください。
1. ビューアのサイズを設定する。
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにスクリプトタグを追加する必要があります。 ビューアのAPIを使用するには、を必ず含め [!DNL InterativeVideoViewer.js]ます。 この [!DNL InteractiveVideoViewer.js] ファイルは、次に示すように、ISビューアの標準のデプロイ先の [!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

ビューアがAdobeDynamic MediaClassicサーバーの1つにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobeDynamic MediaClassicサーバーの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScript `include` ファイルのみを参照する必要があります。 Webページコード内で、ビューアのロジックによって実行時にダウンロードされる可能性のある追加のJavaScriptファイルは、参照しないでください。 特に、ビューアによって読み込まれたHTML5 SDK `Utils.js` ライブラリを、 `/s7viewers` コンテキストパスから直接参照しないでください(いわゆる統合SDK `include`)。 これは、実行時のViewerライブラリの場所がビューアのロジックで完全に管理され `Utils.js` 、ビューアのリリース間で場所が変わるためです。 アドビでは、古いバージョンのセカンダリViewerをサーバーに保持 `includes` しません。
>
>
>その結果、新しいバージョンの製品がデプロイされる際に、ビューアが `include` 使用するセカンダリJavaScriptへの直接参照をページに配置すると、将来、ビューアの機能が壊れる可能性があります。

1. コンテナの定義を参照して `DIV`ください。

   ビューアを追加表示するページの空の要素。 `DIV` この `DIV` IDは後でビューアのAPIに渡されるので、要素でIDを定義する必要があります。 DIVのサイズはCSSで指定します。

   プレースホルダ `DIV` ーは位置固定要素で、 `position` CSSプロパティが `relative` またはに設定されてい `absolute`ます。

   Internet Explorerでフルスクリーン機能を正しく機能させるには、DOM内に、プレースホルダーよりも重ね順の高い要素がないことを確認してくだ `DIV`さい。

   プレースホルダー `DIV` 要素の定義例を次に示します。

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアのサイズの設定

   ビューアの静的サイズを設定するには、最上位CSSクラスに対して絶対単位で宣言するか、 `.s7interactivevideoviewer``stagesize` 修飾子を使用します。

   サイズ調整は、CSS内で直接HTMLページまたはカスタムビューアのCSSファイルに配置できます。このCSSファイルは、後でオンデマンドのビューアプリセットレコードに割り当てるか、 `style` コマンドを使用して明示的に渡します。

   CSSでのビューアのスタイル設定について詳しくは、インタラクティブビデオビューアの [カスタマイズを参照してください](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 。

   以下は、HTMLページで静的ビューアサイズを定義する例です。

   ```
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   修飾子は、ビューアプリセットレコードのAEM Assets（オンデマンド）に設定でき `stagesize` ます。 または、次のように、ビューア初期化コードを `params` コレクションと共に明示的に渡すか、コマンドリファレンスの節で説明するAPI呼び出しとして渡すことができます。

   ```
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   CSSベースのアプローチを推奨し、この例では使用します。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報をコンストラクターに渡して、ビューアインスタンスで `s7viewers.InteractiveVideoViewer``init()` メソッドを呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 最低でも、このオブジェクトには、ビューアのコンテナIDの名前と、ビューアでサポートされている設定パラメーターを含むネストされた `containerId` JSONオブジェクトを保持する `params` フィールドが存在する必要があります。

   この場合、 `params` オブジェクトには、プ `serverUrl` ロパティとして渡された画像サービングURLが最低限必要で、また、初期アセットが `asset` パラメーターとして含まれている必要があります。 JSONベースの初期化APIを使用すると、1行のコード、プロパティとして渡されたビデオサーバのURL、初期アセットをパラメーターとして、インタラクティブデータをプ `videoserverurl``asset``interactivedata` ロパティとして、ビューアを作成および開始できます。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、開始できます。

   ビューアのコンテナをDOMに追加して、ビューアのコードがIDでコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Webページが終わるまでDOMの構築が遅れます。 互換性を最大にするには、終了タグの直前、またはbody `init()` イベントでメソッドを呼び出し `BODY``onload()` ます。

   同時に、コンテナ要素がまだWebページレイアウトの一部である必要はありません。 例えば、割り当てられた `display:none` スタイルを使用して非表示にすることができます。 この場合、Webページからコンテナ要素がレイアウトに戻る瞬間まで、ビューアは初期化プロセスを遅延します。 その結果、ビューアの読み込みが自動的に再開されます。

   以下の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、 `init()` メソッドを呼び出します。 この例では、次のことを前提としています。

   * ビューアインスタンスはで `interactiveVideoViewer`す。
   * プレースホルダーの名前 `DIV` はで `s7viewer`す。
   * 画像サービングのURLはで `https://aodmarketingna.assetsadobe.com/is/image/`す。
   * ビデオサーバーのURLはで `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`す。
   * コンテンツURLはで `https://aodmarketingna.assetsadobe.com/`す。
   * アセットはで `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`す。
   * インタラクティブデータはで `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`す。

   ```
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、固定サイズのインタラクティブビデオビューアを埋め込んだ簡単なWebページの例です。

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;"></div> 
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高さ無制限のレスポンシブデザイン埋め込み**

レスポンシブデザイン埋め込みでは、Webページには通常、ビューアのコンテナの実行時のサイズを指示する柔軟なレイアウトが指定されてい `DIV`ます。 次の例では、WebページでビューアのコンテナがWebブラウザーのウィンドウサイズの40%を占めるこ `DIV` とを許可し、高さは無制限のままにすると仮定します。 WebページのHTMLコードは次のようになります。

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

このようなページへのビューアの追加手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、ビューアサイズを明示的に定義する必要がないことです。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVを定義する。
1. ビューアを作成し、初期化する。

上記の手順はすべて、固定サイズ埋め込みの場合と同じです。 コンテナ追加DIVを既存の `"holder"` DIVに移動します。 次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化すること、ビューアの縦横比がアセットと一致することに注目してください。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用方法を説明しています。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- OLD DEMO LOCATION-KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**幅と高さが定義されたレスポンシブ埋め込み**

幅と高さが定義されたレスポンシブ埋め込みの場合、Webページのスタイルは異なります。 これは両方のサイズを `"holder"` DIVに提供し、ブラウザーウィンドウの中央に配置します。 また、Webページでは、要素 `HTML` と要素のサイズを100%に設定し `BODY` ます。

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

残りの埋め込み手順は、高さ無制限のレスポンシブ埋め込みで使用した手順と同じです。 結果の例を次に示します。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**セッターベースのAPIを使用した埋め込み**

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合、コンストラクターにパラメーターは不要です。設定パラメーターは、 `setContainerId()`、 `setParam()`および `setAsset()` APIメソッドを別々のJavaScript呼び出しで使用して指定します。

以下の例は、固定サイズ埋め込みとセッターベースのAPIを使用する場合を説明しています。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactivevideoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer(); 
interactiveVideoViewer.setContainerId("s7viewer"); 
interactiveVideoViewer.setParam("config", "/etc/dam/presets/viewer/Shoppable_Video_Dark"); 
interactiveVideoViewer.setParam("serverurl", "https://aodmarketingna.assetsadobe.com/is/image/"); 
interactiveVideoViewer.setParam("videoserverurl", "https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna"); 
interactiveVideoViewer.setParam("contenturl", "https://aodmarketingna.assetsadobe.com/"); 
interactiveVideoViewer.setParam("interactivedata", "is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt"); 
interactiveVideoViewer.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4"); 
interactiveVideoViewer.init(); 
</script> 
</body> 
</html>
```

