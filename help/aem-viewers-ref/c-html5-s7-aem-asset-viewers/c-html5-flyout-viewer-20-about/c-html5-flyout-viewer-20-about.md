---
description: フライアウトビューアは画像ビューアです。 ユーザーがアクティブにするフライアウト表示に表示されるズームされたバージョンで、静的な画像を表示します。 このビューアは画像セットで機能し、スウォッチを使用してナビゲーションを行います。 デスクトップおよびモバイルデバイスで動作するように設計されています。
keywords: responsive
seo-description: フライアウトビューアは画像ビューアです。 ユーザーがアクティブにするフライアウト表示に表示されるズームされたバージョンで、静的な画像を表示します。 このビューアは画像セットで機能し、スウォッチを使用してナビゲーションを行います。 デスクトップおよびモバイルデバイスで動作するように設計されています。
seo-title: フライアウト
solution: Experience Manager
title: フライアウト
topic: Dynamic media
uuid: 588e1baa-4165-4aec-8fbe-1a916c0f409f
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2130'
ht-degree: 0%

---


# フライアウト{#flyout}

フライアウトビューアは画像ビューアです。 ユーザーがアクティブにするフライアウト表示に表示されるズームされたバージョンで、静的な画像を表示します。 このビューアは画像セットで機能し、スウォッチを使用してナビゲーションを行います。 デスクトップおよびモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR（画像レンダリング）またはUGC（ユーザ生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアタイプ504

必要 [システム構成と前提条件を参照してください](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## デモURL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## フライアウトビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

フライアウトビューアは、メインのJavaScriptファイルと、ビューアによって実行時にダウンロードされるヘルパーファイルのセット（この特定のビューアで使用されるすべてのビューアSDKコンポーネントが含まれる1つのJavaScriptインクルード、アセット、CSS）です

フライアウトビューアは、埋め込みでの使用のみが想定されています。つまり、ドキュメントに記述のあるAPIを使用してWebページに統合されます。 フライアウトビューアには、運用に対応しているWebページはありません。

設定とスキン表示は、他のビューアと同様です。 スキン表示の適用にカスタムCSSを使用できます。

すべてのビューアに共通の [コマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 、およびすべてのビューアに共通の [コマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## フライアウトビューアの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

フライアウトビューアは、他のモバイルアプリケーションで一般的なシングルタッチとマルチタッチのジェスチャに対応しています。

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
   <td colname="col2"> <p> フライアウト表示をアクティブにするか、プライマリズームレベルとセカンダリズームレベルを切り替えます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> スウォッチバー内のスウォッチのリストをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直スワイプ </p> </td> 
   <td colname="col2"> <p>スウォッチ領域内でこのジェスチャを行うと、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

また、タッチスクリーンとマウスを備えたWindowsデバイスでは、タッチ入力とマウス入力の両方がサポートされています。 ただし、このサポートは、Chrome、Internet Explorer 11およびEdgeのWebブラウザーにのみ制限されます。

このビューアは完全にキーボードでアクセスできます。

詳しくは、 [キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## フライアウトビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Webページごとに異なります。 Webページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは、主に次の2つの操作モードがサポートされています。 固定サイズ埋め込みとレスポンシブデザイン埋め込み

固定サイズ埋め込みモードは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 静的ページレイアウトのWebページには、この選択肢が最適です。

レスポンシブデザイン埋め込みモードは、コンテナのサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定してい `DIV`ます。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

フライアウトビューアでレスポンシブデザイン埋め込みモードを使用する場合は、 `imagereload` パラメーターを使用して、メイン表示画像の明示的なブレークポイントを必ず指定してください。 ブレークポイントは、WebページのCSSで指定されているビューアの幅のブレークポイントと一致させるのが理想的です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナのサイズ変更の方法に応じて、ビューアの動作が異なり `DIV`ます。 Webページでコンテナの幅のみが設定され、高さは無制限のままの場合 `DIV`、ビューアでは、使用するアセットの縦横比に従って高さが自動的に選択されます。 つまり、両側のパディングなしで、アセットは表示にぴったりと収まります。 この特定の使用例は、Bootstrap、Foundationなどのレスポンシブデザインレイアウトフレームワークを使用するWebページで最も一般的です。

また、Webページでビューアのコンテナの幅と高さの両方が設定されている場合 `DIV`、ビューアはその領域のみを占め、Webページレイアウトで指定されているサイズに従います。 良い使用例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合があります。

**固定サイズ埋め込み**

ビューアは、次の操作を行ってWebページに追加します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナの定義を参照して `DIV`ください。
1. ビューアのサイズを設定する。
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにスクリプトタグを追加する必要があります。 ビューアのAPIを使用するには、を必ず含め `FlyoutViewer.js`ます。 `FlyoutViewer.js` は、標準のIS-Viewersデプロイメントの次の [!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

ビューアがAdobe Scene7サーバの1つにデプロイされ、同じドメインから供給される場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobe Scene7サーバの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScript `include` ファイルのみを参照する必要があります。 Webページコード内で、ビューアのロジックによって実行時にダウンロードされる可能性のある追加のJavaScriptファイルは、参照しないでください。 特に、ビューアによって読み込まれたHTML5 SDK `Utils.js` ライブラリを、 `/s7viewers` コンテキストパスから直接参照しないでください(いわゆる統合SDK `include`)。 これは、実行時のViewerライブラリの場所がビューアのロジックで完全に管理され `Utils.js` 、ビューアのリリース間で場所が変わるためです。 アドビでは、古いバージョンのセカンダリViewerをサーバーに保持 `includes` しません。
>
>
>その結果、新しいバージョンの製品がデプロイされる際に、ビューアが `include` 使用するセカンダリJavaScriptへの直接参照をページに配置すると、将来、ビューアの機能が壊れる可能性があります。

1. コンテナDIVを定義する。

   ビューア追加を表示するページの空のDIV要素。 DIV要素は、IDが定義されている必要があります。このIDを、後でビューアのAPIに渡します。

   プレースホルダDIVは、配置済みの要素です。つまり、 `position` CSSプロパティが `relative` またはに設定され `absolute`ます。

   プレースホルダDIV要素の適切な値は、Webページ `z-index` で指定します。 これにより、ビューアのフライアウト部分が、Webページの他の要素の上に表示されます。

   プレースホルダDIV要素の定義例を次に示します。

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. ビューアのサイズを設定する。

   複数項目セットを処理する場合、このビューアにはサムネールが表示されます。 デスクトップシステムでは、サムネールはメイン表示の下に配置されます。 同時に、ビューアでは、実行時に `setAsset()` APIを使用してメインアセットを入れ替えることができます。 開発者は、新しいアセットの項目が1つだけの場合に、下部のサムネール領域をビューアがどのように管理するかを制御できます。 ビューアの外側のサイズはそのままにし、メイン表示の高さを拡大して、サムネール領域を表示させることができます。 または、メイン表示のサイズを静的に保ってビューアの外側の領域を折りたたみ、Webコンテンツを上に移動して、サムネールから残された空きページの領域を使用できます。

   ビューアの外側の境界をそのまま残すには、最上位 `.s7flyoutviewer` CSSクラスのサイズを絶対単位で定義します。 CSS内のサイズ調整は、HTMLページまたはカスタムビューアのCSSファイルに適用できます。このCSSファイルは、後でScene7 Publishing Systemのビューアプリセットレコードに割り当てるか、styleコマンドを使用して明示的に渡します。

   CSSでのビューアのスタイル設定について詳しくは、フライアウトビューアの [カスタマイズを参照してください](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) 。

   以下は、HTMLページでビューアの外側の静的なサイズを定義する例です。

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   以下のサンプルページでは、ビューアの外側の領域を固定した場合の動作を確認できます。 セットを切り替えても、ビューアの外側のサイズは変わりません。

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html)

   メイン表示のサイズを静的にするには、 `Container` CSSセレクターを使用して、内部の `.s7flyoutviewer .s7container` SDKコンポーネントのビューアサイズを絶対単位で定義します。 また、初期設定のビューアCSSの `.s7flyoutviewer` 最上位CSSクラスに定義されている固定サイズをに設定して上書きする必要があり `auto`ます。

   以下は、アセットを切り替えてもメイン表示領域のサイズが変更されないように、内部の `Container` SDKコンポーネントのビューアサイズを定義する例です。

   ```
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   以下のサンプルページは、メイン表示のサイズを固定した場合のビューアの動作を示しています。 セットを切り替えてもメイン表示は静的なままで、Webページのコンテンツは垂直方向に移動します。

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html)

   また、初期設定のビューアCSSでは、初期設定の外側領域に固定サイズが提供されています。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報をコンストラクターに渡して、ビューアインスタンスで `s7viewers.FlyoutViewer``init()` メソッドを呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 最低でも、このオブジェクトには、ビューアのコンテナIDの名前と、ビューアでサポートされている設定パラメーターを含むネストされた `containerId` JSONオブジェクトを保持する `params` フィールドが存在する必要があります。 この場合、 `params` オブジェクトには、プ `serverUrl` ロパティとして渡された画像サービングURLが最低限必要で、また、初期アセットが `asset` パラメーターとして含まれている必要があります。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、開始できます。

   ビューアのコンテナをDOMに追加して、ビューアのコードがIDでコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Webページが終わるまでDOMの構築が遅れます。 互換性を最大にするには、終了タグの直前、またはbody `init()` イベントでメソッドを呼び出し `BODY``onload()` ます。

   同時に、コンテナ要素がまだWebページレイアウトの一部である必要はありません。 例えば、割り当てられた `display:none` スタイルを使用して非表示にすることができます。 この場合、Webページからコンテナ要素がレイアウトに戻る瞬間まで、ビューアは初期化プロセスを遅延します。 この場合、ビューアの読み込みが自動的に再開されます。

   以下の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、 `init()` メソッドを呼び出します。 この例では、 `flyoutViewer` がビューアインスタンスであると仮定しています。 `s7viewer` はプレースホルダーの名前で `DIV`す。 `http://s7d1.scene7.com/is/image/` は画像サービングのURL; と `Scene7SharedAssets/ImageSet-Views-Sample` がアセットです。

   ```
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、固定サイズのフライアウトビューアを埋め込んだ簡単なWebページの例です。

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## 高さ無制限のレスポンシブデザイン埋め込み {#section-056cb574713c4d07be6d07cf3c598839}

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

このようなページへのビューアの追加手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、初期設定のビューアCSSの固定サイズを、相対単位で設定されたサイズで上書きする必要があることです。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナの定義を参照して `DIV`ください。
1. ビューアのサイズを設定する。
1. ビューアを作成し、初期化する。

上記の手順はすべて、以下の3つの例外を除き、固定サイズ埋め込みの場合と同じです。

* コンテナ `DIV` を既存の「保持者」に追加 `DIV`し、
* 明示的なブレークポイントを含む `imagereload` パラメーターを追加しました。
* 絶対単位を使用してビューアの固定サイズを設定する代わりに、次のようにビューアの幅と高さを100%に設定するCSSを使用します。

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化すること、ビューアの縦横比がアセットと一致することに注目してください。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用方法を説明しています。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## 幅と高さが定義されたフレキシブルサイズ埋め込み {#section-0a329016f9414d199039776645c693de}

幅と高さが定義されたフレキシブルサイズ埋め込みの場合、Webページのスタイリングは異なります。 これは両方のサイズを `"holder"` DIVに提供し、ブラウザーウィンドウの中央に配置します。 また、Webページでは、要素 `HTML` と要素のサイズを100%に設定し `BODY` ます。

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

残りの埋め込み手順は、高さ無制限のレスポンシブデザイン埋め込みで使用した手順と同じです。 結果の例を次に示します。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
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
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## セッターベースのAPIを使用した埋め込み {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合、コンストラクターにパラメーターは不要です。設定パラメーターは、 `setContainerId()`、 `setParam()`および `setAsset()` APIメソッドを使用し、それぞれ異なるJavaScript呼び出しを使用して指定します。

以下の例は、固定サイズ埋め込みとセッターベースのAPIを使用する場合を説明しています。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```

