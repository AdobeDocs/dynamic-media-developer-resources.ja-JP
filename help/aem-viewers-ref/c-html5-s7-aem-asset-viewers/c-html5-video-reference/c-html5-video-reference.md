---
description: ビデオビューアは、H.264形式でエンコードされたストリーミングビデオとプログレッシブビデオを再生するビデオプレーヤーです。 Dynamic Mediaと共にDynamic Media ClassicまたはAdobe Experience Managerから提供されます。
keywords: レスポンシブ
solution: Experience Manager
title: ビデオ
feature: Dynamic Media Classic，ビューア，SDK/API，ビデオ
role: Developer,User
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: f77dc0c1ac8305037bbb561451317c8e62209cec
workflow-type: tm+mt
source-wordcount: '2379'
ht-degree: 0%

---

# ビデオ{#video}

ビデオビューアは、H.264形式でエンコードされたストリーミングビデオとプログレッシブビデオを再生するビデオプレーヤーです。 これは、Dynamic Media ClassicまたはDynamic MediaとのExperience Managerから提供されます。

[必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

単一のビデオとアダプティブビデオセットの両方がサポートされています。 また、ビューアは、外部でホストされるプログレッシブビデオおよびHLSストリームの操作もサポートしています。 HTML5ビデオをサポートするデスクトップとモバイルWebブラウザーの両方で動作するように設計されています。 このビューアは、ビデオコンテンツ、ビデオチャプターナビゲーションおよびソーシャルメディア共有ツールの上に表示されるオプションのクローズドキャプションもサポートしています。

ビデオビューアは、基になるシステムがHLS形式をサポートしている場合は常に、初期設定でHTML5ストリーミングビデオ再生をHLS形式で使用します。 HTML5ストリーミングをサポートしていないシステムでは、ビューアはHTML5プログレッシブビデオ配信にフォールバックされます。

ビューアタイプ506

## デモURL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## ビデオビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

ビデオビューアは、メインのJavaScriptファイルと、ヘルパーファイルのセットです。単一のJavaScriptインクルードには、この特定のビューアで使用されるすべてのビューアSDKコンポーネント、アセット、実行時にビューアによってダウンロードされるCSSが含まれます。

ISビューアに付属する実稼動用のHTMLページを使用して、ビデオビューアをポップアップモードで使用できます。 または、ビューアを埋め込みモードで使用し、ドキュメントに記載されているAPIを使用して、ビューアをターゲットWebページに統合することもできます。

ビューアの設定とスキン表示のタスクは、他のビューアと同様です。 スキンの適用はすべて、カスタムCSSを使用して行います。

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください。

## ビデオビューアの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

ビデオビューアには、再生/一時停止ボタン、ビデオスクラバービデオ時間の吹き出し、再生時間/合計時間インジケーター、ボリューム制御、フルスクリーンボタン、クローズドキャプションの切り替えなど、ビデオ再生に関する一連の標準的なユーザーインターフェイスコントロールが用意されています。 ビューアのユーザインターフェイスの下部にあるコントロールバーに、これらのコントロールがすべてグループ化されています。

タッチデバイスでは、ハードウェアボタンを使用してのみボリュームを制御できるので、ボリューム制御はユーザーインターフェイスに表示されません。

ビューアがポップアップモードで動作している場合、ユーザーインターフェイスでフルスクリーンボタンは使用できません。

ビデオチャプターが有効になっている場合は、ビデオのコンテンツをすばやく移動できます。 ビデオチャプターは、ビデオスクラバートラックにマーカーとして表示され、マウスのロールオーバー時またはタッチシステムでの1回のタップ時に、チャプタータイトルと関連する説明が表示されます。 ユーザーは、チャプターマーカーを選択するか、チャプター説明の吹き出しを選択することで、特定のチャプターを探すことができます。

タッチスクリーンとマウスを備えたWindowsデバイスでは、タッチ入力とマウス入力の両方がサポートされます。 ただし、このサポートは、Chrome、Internet Explorer 11およびEdge Webブラウザーのみに制限されます。

このビューアは完全にキーボードでアクセス可能です。

[キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## ビデオビューアを使用したソーシャルメディア共有ツール {#section-907d316fe1da4b87abb9775f02464704}

ビデオビューアは、ソーシャルメディア共有ツールをサポートしています。 これらは、ユーザーインターフェイスの単一のボタンとして使用でき、ユーザーがクリックまたはタップすると共有ツールバーに展開されます。

共有ツールバーには、Facebook、Twitter、電子メール共有、埋め込みコード共有、リンク共有など、サポートされる共有チャネルの各タイプ用のアイコンが表示されます。 電子メール共有、埋め込み共有またはリンク共有のツールをアクティブにすると、ビューアにモーダルダイアログボックスが表示され、対応するデータ入力フォームが表示されます。 facebookまたはTwitterを呼び出すと、ソーシャルメディアサービスの標準の共有ダイアログボックスにリダイレクトされます。 また、共有ツールが有効になると、ビデオ再生が自動的に一時停止します。

Webブラウザーのセキュリティ上の制約により、共有ツールはフルスクリーンモードでは使用できません。

## ビデオビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Webページごとに異なります。 Webページにリンクが表示され、このリンクをクリックすると別のブラウザーウィンドウでビューアが開くことがあります。 ホスティングページに直接ビューアを埋め込む必要がある場合もあります。 後者の場合は、Webページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは次の3つの主要な操作モードがサポートされています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

同じページへの複数のビデオの埋め込みは、タブレットとモバイルデバイスでサポートされています。 通常、一度に1つのビデオのみ再生できます。 ユーザーが1つのビデオの再生を開始し、別のビデオの再生を試みると、最初のビデオが自動的に一時停止します。 自動一時停止になったビデオは現在の再生時間を記憶するので、ユーザーはいつでもビデオに戻って再生を再開できます。 このルールの唯一の例外は、Android™ 4.xデバイスのChromeブラウザーで、ビデオを並行して再生できる点です。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別のWebブラウザーウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやデバイスの向きが変更された場合は調整されます。

このモードは、モバイルデバイスで最も一般的なモードです。 Webページでは、`window.open()` JavaScript呼び出し、適切に設定された`A` HTML要素またはその他の適切な方法を使用してビューアを読み込みます。

ポップアップ操作モードには、標準提供のHTMLページを使用することをお勧めします。 このページは[!DNL VideoViewer.html]と呼ばれ、標準のIS-Viewersデプロイメントの[!DNL html5/]サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/VideoViewer.html]

カスタムCSSを適用することで、視覚的なカスタマイズを実現できます。

以下は、ビューアを新しいウィンドウで開くHTMLコードの例です。

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブ埋め込みモードについて**

埋め込みモードでは、ビューアは既存のWebページに追加されます。既に、ビューアに関連していない顧客コンテンツが含まれている場合があります。 ビューアは、通常、Webページの一部の領域のみを占有します。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、また、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用されます。 この選択は、静的ページレイアウトのWebページに最適です。

レスポンシブデザイン埋め込みは、コンテナ`DIV`のサイズ変更に対応して実行時にビューアのサイズを変更する必要がある場合を想定しています。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナ`DIV`のサイズ変更の方法によって、ビューアの動作が異なります。 Webページでコンテナ`DIV`の幅のみが設定され、高さは無制限のままの場合、ビューアでは、使用するアセットの縦横比に従って高さが自動的に選択されます。 この方法を使用すると、側面のパディングなしで、アセットが表示にぴったりと収まります。 この使用例は、Bootstrapや基盤などのレスポンシブデザインレイアウトフレームワークを使用するWebページで最も一般的です。

また、Webページでビューアのコンテナ`DIV`の幅と高さの両方が設定されている場合、ビューアはその領域を占め、Webページレイアウトで指定されたサイズに従います。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーウィンドウのサイズに従ってサイズ設定される場合があります。

**固定サイズ埋め込み**

ビューアをWebページに追加するには、次の手順を実行します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナ`DIV`を定義します。
1. ビューアのサイズを設定する。
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにscriptタグを追加する必要があります。 ビューアのAPIを使用するには、必ず[!DNL FlyoutViewer.js]を含めてください。 [!DNL FlyoutViewer.js]ファイルは、次に示すように、IS-Viewersの標準のデプロイ先の[!DNL html5/js/]サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

ビューアがDynamic Media ClassicAdobeのいずれかにデプロイされ、同じドメインから提供されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobeDynamic Media Classicサーバーの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>ページ上で、メインビューアのJavaScript `include`ファイルのみを参照します。 実行時にビューアのロジックによってダウンロードされる可能性のあるWebページコード内の追加のJavaScriptファイルは参照しないでください。 特に、ビューアによって`/s7viewers`コンテキストパスから読み込まれたHTML5 SDK `Utils.js`ライブラリを直接参照しないでください（いわゆる統合SDK `include`）。 理由は、`Utils.js`や類似のランタイムビューアライブラリの場所は、ビューアのロジックによって完全に管理され、ビューアのリリースによって位置が変わるからです。 Adobeでは、セカンダリビューア`includes`の古いバージョンはサーバに保持されません。
>
>
>その結果、新しい製品バージョンがデプロイされると、ビューアが使用するセカンダリJavaScript `include`への直接参照をページに配置すると、将来ビューア機能が壊れます。

1. コンテナDIVを定義する。

   ビューアを表示するページに空のDIV要素を追加します。 DIV要素では、IDが定義されている必要があります。このIDは、後でビューアのAPIに渡されます。 DIVのサイズはCSSで指定します。

   プレースホルダーDIVは配置を指定する要素で、CSSの`position`プロパティを`relative`または`absolute`に設定します。

   Internet Explorerで全画面表示機能が正しく機能することを確認します。 DOM内に、プレースホルダーDIVよりも重ね順の高い要素がないことを確認します。

   プレースホルダーDIV要素の定義例を次に示します。

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. ビューアサイズの設定

   ビューアの静的サイズを設定するには、`.s7videoviewer`最上位CSSクラスに対して絶対単位で宣言するか、修飾子`stagesize`を使用します。

   サイズ変更は、HTMLページのCSSで直接、またはカスタムビューアのCSSファイルで設定できます。 後でDynamic Media Classicのビューアプリセットレコードに割り当てられるか、スタイルコマンドを使用して明示的に渡されます。

   CSSを使用したビューアのスタイル設定について詳しくは、[ビデオビューアのカスタマイズ](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e)を参照してください。

   以下は、HTMLページで静的ビューアサイズを定義する例です。

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   `stagesize`修飾子は、Dynamic Media Classicのビューアプリセットレコードで設定するか、`params`コレクションを使用してビューア初期化コードで明示的に渡すことができます。 または、次のように、コマンドリファレンスの節で説明するAPI呼び出しとして使用できます。

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   CSSベースのアプローチを推奨し、この例で使用します。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、`s7viewers.VideoViewer`クラスのインスタンスを作成し、すべての設定情報をコンストラクターに渡して、ビューアインスタンスで`init()`メソッドを呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 最低でも、このオブジェクトには`containerId`フィールドが必要です。このフィールドには、ビューアのコンテナIDの名前と、ビューアでサポートされている設定パラメーターを含むネストされた`params` JSONオブジェクトが含まれています。 この場合、`params`オブジェクトには、`serverUrl`プロパティとして渡された画像サービングURL、`videoserverurl`プロパティとして渡されたビデオサーバーURL、および`asset`パラメーターとして最初のアセットが少なくとも含まれている必要があります。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、起動できます。

   ビューアのコードがIDでコンテナ要素を見つけられるように、ビューアのコンテナをDOMに追加することが重要です。 一部のブラウザーは、Webページの終わりまでDOMの構築を遅らせます。 互換性を最大にするには、 `BODY`終了タグの直前、または本文の`onload()`イベントで`init()`メソッドを呼び出します。

   同時に、コンテナ要素は、必ずしもWebページレイアウトの一部ではありません。 例えば、`display:none`スタイルを割り当てて非表示にすることができます。 この場合、Webページでコンテナ要素がレイアウトに戻るまで、ビューアの初期化プロセスが遅れます。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

   以下の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、 `init()`メソッドを呼び出します。 この例では、 `videoViewer`をビューアインスタンス、 `s7viewer`をプレースホルダー`DIV`の名前、 [!DNL http://s7d1.scene7.com/is/image/]を画像サービングのURL、 [!DNL http://s7d1.scene7.com/is/content/]をビデオサーバーのURL、 [!DNL Scene7SharedAssets/Glacier_Climber_MP4]をアセットと仮定します。

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

レスポンシブデザイン埋め込みでは、Webページには通常、ビューアのコンテナ`DIV`の実行時のサイズを指示する柔軟なレイアウトが指定されています。 この例では、Webページでビューアのコンテナ`DIV`がWebブラウザーのウィンドウサイズの40%を占めることを許可し、高さは無制限のままにするとします。 WebページのHTMLコードは次のようになります。

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

このようなページへのビューアの追加方法は、固定サイズ埋め込みの場合と似ています。唯一の違いは、ビューアのサイズを明示的に定義する必要がない点です。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVを定義する。
1. ビューアを作成し、初期化する。

上記の手順は、固定サイズ埋め込みの場合と同じです。 コンテナ`DIV`を既存の「ホルダー」`DIV`に追加します。 次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズがどのように変化するか、ビューアの縦横比がアセットと一致するかを確認できます。

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

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用方法を説明します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[代替のデモの場所](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**幅と高さが定義されたレスポンシブデザイン埋め込み**

幅と高さが定義されたレスポンシブデザイン埋め込みがある場合、Webページのスタイル設定は異なります。&quot;holder&quot; `DIV`に両方のサイズを提供し、ブラウザーウィンドウの中央に配置します。 また、Webページでは、`HTML`要素と`BODY`要素のサイズを100%に設定します。

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

残りの埋め込み手順は、高さ無制限のレスポンシブデザイン埋め込みと同じです。 結果の例は次のようになります。

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

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIでは、コンストラクターにパラメーターは不要です。設定パラメーターは、 `setContainerId()`、 `setParam()`および`setAsset()`の各APIメソッドを別々のJavaScript呼び出しで使用して指定します。

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
