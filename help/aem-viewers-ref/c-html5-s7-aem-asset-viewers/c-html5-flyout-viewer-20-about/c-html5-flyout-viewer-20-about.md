---
description: フライアウトビューアは画像ビューアです。 ユーザーがアクティブにするフライアウトビューに表示されるズームされたバージョンで、静的な画像が表示されます。 このビューアは画像セットで機能し、ナビゲーションはスウォッチを使用しておこないます。 デスクトップおよびモバイルデバイスで動作するように設計されています。
keywords: レスポンシブ
solution: Experience Manager
title: フライアウト
feature: Dynamic Media Classic，ビューア，SDK/API，フライアウト
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: f77dc0c1ac8305037bbb561451317c8e62209cec
workflow-type: tm+mt
source-wordcount: '2072'
ht-degree: 0%

---

# フライアウト{#flyout}

フライアウトビューアは画像ビューアです。 ユーザーがアクティブにするフライアウトビューに表示されるズームされたバージョンで、静的な画像が表示されます。 このビューアは画像セットで機能し、ナビゲーションはスウォッチを使用しておこないます。 デスクトップおよびモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR（画像レンダリング）またはUGC（ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアタイプは504です。

[必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

## デモURL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## フライアウトビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

フライアウトビューアは、メインのJavaScriptファイルと、ヘルパーファイルのセット（この特定のビューア、アセット、CSSで使用されるすべてのビューアSDKコンポーネントを含む単一のJavaScriptインクルード）です

フライアウトビューアは、埋め込みでの使用のみが想定されています。つまり、ドキュメントに記載されているAPIを使用してWebページに統合されます。 フライアウトビューアには、実稼動に対応したWebページはありません。

設定とスキン表示は、他のビューアと同様です。 スキニングを適用するには、カスタムCSSを使用できます。

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください。

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
   <td colname="col2"> <p> フライアウトビューをアクティブにするか、プライマリズームレベルとセカンダリズームレベルを切り替えます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平方向のスワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> スウォッチバーのスウォッチリストをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直方向のスワイプ </p> </td> 
   <td colname="col2"> <p>スウォッチ領域内でこのジェスチャを実行すると、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

タッチスクリーンとマウスを備えたWindowsデバイスでは、タッチ入力とマウス入力の両方がサポートされます。 ただし、このサポートは、Chrome、Internet Explorer 11およびEdge Webブラウザーのみに制限されます。

このビューアは完全にキーボードでアクセス可能です。

[キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## フライアウトビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Webページごとに異なります。 Webページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは、次の2つの主要な操作モードがサポートされています。固定サイズ埋め込みとレスポンシブデザイン埋め込み。

固定サイズ埋め込みモードは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 この選択は、静的ページレイアウトのWebページに最適です。

レスポンシブデザイン埋め込みモードでは、コンテナ`DIV`のサイズ変更に対応して実行時にビューアのサイズを変更する必要がある場合を想定しています。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

フライアウトビューアでレスポンシブデザイン埋め込みモードを使用する場合は、`imagereload`パラメーターを使用して、メインビュー画像の明示的なブレークポイントを必ず指定してください。 ブレークポイントは、WebページのCSSで指定されているビューアの幅のブレークポイントと一致させるのが理想的です。

レスポンシブデザイン埋め込みモードでは、Webページコンテナ`DIV`のサイズに応じて、ビューアの動作が異なります。 Webページでコンテナ`DIV`の幅のみが設定され、高さは無制限のままの場合、ビューアでは、使用するアセットの縦横比に従って高さが自動的に選択されます。 つまり、側面のパディングなしで、アセットは表示にぴったりと収まります。 この特定の使用例は、Bootstrapや基盤などのレスポンシブデザインレイアウトフレームワークを使用するWebページで最も一般的です。

それ以外の場合、Webページでビューアのコンテナ`DIV`の幅と高さの両方が設定されている場合、ビューアはその領域のみを占め、Webページレイアウトで指定されたサイズに従います。 良い使用例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合があります。

**固定サイズ埋め込み**

ビューアをWebページに追加するには、次の手順を実行します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナ`DIV`を定義します。
1. ビューアのサイズを設定する。
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにscriptタグを追加する必要があります。 ビューアのAPIを使用するには、必ず`FlyoutViewer.js`を含めてください。 `FlyoutViewer.js` は、標準のIS-Viewersデプ [!DNL html5/js/] ロイメントの次のサブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

ビューアがDynamic MediaAdobeのいずれかにデプロイされ、同じドメインから提供されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobeDynamic Mediaサーバーの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>ページ上で、メインビューアのJavaScript `include`ファイルのみを参照します。 実行時にビューアのロジックによってダウンロードされる可能性のあるWebページコード内の追加のJavaScriptファイルは参照しないでください。 特に、ビューアによって`/s7viewers`コンテキストパスから読み込まれたHTML5 SDK `Utils.js`ライブラリを直接参照しないでください（いわゆる統合SDK `include`）。 理由は、`Utils.js`や類似のランタイムビューアライブラリの場所は、ビューアのロジックによって完全に管理され、ビューアのリリースによって位置が変わるからです。 Adobeでは、セカンダリビューア`includes`の古いバージョンはサーバに保持されません。
>
>
>その結果、新しい製品バージョンがデプロイされると、ビューアが使用するセカンダリJavaScript `include`への直接参照をページに配置すると、将来ビューア機能が壊れます。

1. コンテナDIVを定義する。

   ビューアを表示するページに空のDIV要素を追加します。 DIV要素では、IDが定義されている必要があります。このIDは、後でビューアのAPIに渡されます。

   プレースホルダーDIVは配置を指定する要素で、CSSの`position`プロパティを`relative`または`absolute`に設定します。

   プレースホルダDIV要素に適切な`z-index`を指定するのはWebページの責任です。 これにより、ビューアのフライアウト部分が、他のWebページ要素の上に表示されます。

   プレースホルダーDIV要素の定義例を次に示します。

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. ビューアのサイズを設定する。

   複数項目セットを操作する場合、このビューアにはサムネールが表示されます。 デスクトップシステムでは、サムネールはメインビューの下に配置されます。 同時に、ビューアでは、実行時に`setAsset()` APIを使用してメインアセットを入れ替えることができます。 開発者は、新しいアセットに項目が1つしかない場合に、下部のサムネール領域をビューアでどのように管理するかを制御できます。 ビューアの外側のサイズはそのままにし、メインビューの高さを拡大してサムネール領域を表示できます。 または、メインビューのサイズを静的に保ち、ビューアの外側の領域を折りたたみ、Webページのコンテンツを上に移動して、サムネールから残された空きページの領域を使用できます。

   ビューアの外側の境界をそのまま残すには、最上位CSSクラス`.s7flyoutviewer`のサイズを絶対単位で定義します。 CSSのサイズ変更は、HTMLページやカスタムビューアのCSSファイルで、後でDynamic Media Classicのビューアプリセットレコードに割り当てたり、styleコマンドを使用して明示的に渡したりできます。

   CSSでのビューアのスタイル設定について詳しくは、 [フライアウトビューアのカスタマイズ](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451)を参照してください。

   以下は、HTMLページでビューアの外側の静的サイズを定義する例です。

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次のサンプルページで、ビューアの外側の領域を固定した場合の動作を確認できます。 セットを切り替えても、ビューアの外側のサイズは変わりません。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   メインビューの画像サイズを静的にするには、`.s7flyoutviewer .s7container` CSSセレクターを使用して、内部の`Container` SDKコンポーネントのビューアサイズを絶対単位で定義します。 また、初期設定のビューアCSSの最上位CSSクラス`.s7flyoutviewer`に対して定義されている固定サイズを`auto`に設定して上書きする必要があります。

   次の例では、アセットを切り替えてもメインビュー領域のサイズが変わらないように、内部の`Container` SDKコンポーネントのビューアサイズを定義します。

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

   以下のサンプルページは、メインビューのサイズを固定した場合のビューアの動作を示しています。 セットを切り替えても、メインビューは静的なままになり、Webページのコンテンツは垂直方向に移動します。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html)

   また、初期設定のビューアCSSでは、そのすぐに使用できる外側領域の固定サイズが提供されています。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、`s7viewers.FlyoutViewer`クラスのインスタンスを作成し、すべての設定情報をコンストラクターに渡して、ビューアインスタンスで`init()`メソッドを呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 最低でも、このオブジェクトには`containerId`フィールドが必要です。このフィールドには、ビューアのコンテナIDの名前と、ビューアがサポートする設定パラメーターを含むネストされた`params` JSONオブジェクトが含まれています。 この場合、`params`オブジェクトには、`serverUrl`プロパティとして渡された画像サービングURLが少なくとも含まれ、最初のアセットが`asset`パラメーターとして含まれている必要があります。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、起動できます。

   ビューアのコードがIDでコンテナ要素を見つけられるように、ビューアのコンテナをDOMに追加することが重要です。 一部のブラウザーは、Webページの終わりまでDOMの構築を遅らせます。 互換性を最大にするには、 `BODY`終了タグの直前、または本文の`onload()`イベントで`init()`メソッドを呼び出します。

   同時に、コンテナ要素は、必ずしもWebページレイアウトの一部ではありません。 例えば、`display:none`スタイルを割り当てて非表示にすることができます。 この場合、Webページでコンテナ要素がレイアウトに戻るまで、ビューアの初期化プロセスが遅れます。 この操作がおこなわれると、ビューアの読み込みが自動的に再開されます。

   以下の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して`init()`メソッドを呼び出します。 この例では、 `flyoutViewer`がビューアインスタンスであると仮定しています。`s7viewer`はプレースホルダー`DIV`の名前です。`http://s7d1.scene7.com/is/image/`は画像サービングのURLです。`Scene7SharedAssets/ImageSet-Views-Sample`はアセットです。

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

レスポンシブデザイン埋め込みでは、Webページには通常、ビューアのコンテナ`DIV`の実行時のサイズを指示する柔軟なレイアウトが指定されています。 次の例では、Webページでビューアのコンテナ`DIV`がWebブラウザーのウィンドウサイズの40%を占めることを許可し、高さは無制限のままにするとします。 WebページのHTMLコードは次のようになります。

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

このようなページにビューアを追加する手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、初期設定のビューアCSSの固定サイズを、相対単位で設定されたサイズで上書きする必要がある点です。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナ`DIV`を定義します。
1. ビューアのサイズを設定する。
1. ビューアを作成し、初期化する。

上記の手順はすべて、次の3つの例外を除き、固定サイズ埋め込みの場合と同じです。

* コンテナ`DIV`を既存の&quot;holder&quot; `DIV`に追加します。
* 明示的なブレークポイントを含む`imagereload`パラメーターを追加しました。
* 絶対単位を使用してビューアの固定サイズを設定する代わりに、次のようにビューアの幅と高さを100%に設定するCSSを使用します。

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化すること、ビューアの縦横比がアセットと一致することに注意してください。

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

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用例を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[代替のデモの場所](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## 幅と高さが定義されたフレキシブルサイズ埋め込み {#section-0a329016f9414d199039776645c693de}

幅と高さが定義されたフレキシブルサイズ埋め込みがある場合、Webページのスタイル設定は異なります。 `"holder"` DIVに両方のサイズを提供し、ブラウザーウィンドウの中央に配置します。 また、Webページでは、`HTML`要素と`BODY`要素のサイズを100%に設定します。

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

残りの埋め込み手順は、高さ無制限のレスポンシブデザイン埋め込みで使用する手順と同じです。 結果の例は次のようになります。

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

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合、コンストラクターにパラメーターは不要です。設定パラメーターは、 `setContainerId()`、 `setParam()`および`setAsset()`の各APIメソッドを別々のJavaScript呼び出しで使用して指定します。

次の例は、固定サイズ埋め込みをセッターベースのAPIで使用する方法を示しています。

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
