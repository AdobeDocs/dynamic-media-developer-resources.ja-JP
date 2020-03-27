---
description: カルーセルビューアは、ズーム可能でないバナー画像のカルーセルと、クリック可能なホットスポットまたは領域を表示するビューアです。 このビューアの目的は、「買い物可能なカルーセル」エクスペリエンスを実装し、バナー画像の上でホットスポットまたは領域を選択して、顧客のWebサイトのクイックビューまたは製品の詳細ページにリダイレクトすることです。 デスクトップや携帯端末で動作するように設計されています。
seo-description: カルーセルビューアは、ズーム可能でないバナー画像のカルーセルと、クリック可能なホットスポットまたは領域を表示するビューアです。 このビューアの目的は、「買い物可能なカルーセル」エクスペリエンスを実装し、バナー画像の上でホットスポットまたは領域を選択して、顧客のWebサイトのクイックビューまたは製品の詳細ページにリダイレクトすることです。 デスクトップや携帯端末で動作するように設計されています。
seo-title: カルーセル
solution: Experience Manager
title: カルーセル
topic: Dynamic media
uuid: 0ba4f40b-8dde-4479-b906-3115f09ab249
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# カルーセル{#carousel}

カルーセルビューアは、ズーム可能でないバナー画像のカルーセルと、クリック可能なホットスポットまたは領域を表示するビューアです。 このビューアの目的は、「買い物可能なカルーセル」エクスペリエンスを実装し、バナー画像の上でホットスポットまたは領域を選択して、顧客のWebサイトのクイックビューまたは製品の詳細ページにリダイレクトすることです。 デスクトップや携帯端末で動作するように設計されています。

>[!NOTE]
>
>画像レンダリングまたはユーザ生成コンテンツ(UGC)を使用する画像は、このビューアではサポートされていません。

ビューアのタイプは511です。

## デモURL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewerDemo.html)

## システム要件 {#section-b7270cc4290043399681dc504f043609}

必要システム [構成を参照してくださ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)い。

## カルーセルビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

カルーセルビューアは、メインのJavaScriptファイルと、ビューアによって実行時にダウンロードされるヘルパーファイルのセット（この特定のビューア、アセット、CSSで使用されるすべてのビューアSDKコンポーネントを含む1つのJavaScriptが含まれる）です。

カルーセルビューアは、ISビューアに付属の実稼動用HTMLページを使用するポップアップモードでも、ドキュメントに記載されたAPIを使用してターゲットWebページに統合される埋め込みモードでも使用できます。

設定とスキン表示は、このヘルプで説明する他のビューアと同様です。 スキン表示は、すべてカスタムCSSを使用して適用されます。

すべてのビ [ューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 、およびすべ [てのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## カルーセルビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

カルーセルセット内の移動は、メインビュー上で水平スワイプするか、デスクトップデバイスで2つの矢印ボタンを使用して行います。 設定インジケーターのドットは、セット内の現在の位置を示します。

ビューアは、バナー画像の上にホットスポットや領域をレンダリングして、製品上のインタラクティブ領域を示すことができます。

ホットスポットまたは領域をクリックまたはタップすると、作成時にその領域に関連付けられたアクションが実行されます。 アクションは、Webサイト上の別のページにリダイレクトされる場合や、製品情報をWebページのロジックに渡す場合があります。これにより、関連する製品コンテンツを含むクイックビューがトリガーされます。

ビューアは完全にキーボードでアクセスできます。

詳しくは、キーボ [ードのアクセシビリティとナビゲーションを参照してくださ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)い。

## カルーセルビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

**ポップアップモードについて**

ポップアップモードでは、ビューアはWebブラウザーの別のウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやモバイルデバイスの向きが変更された場合は調整されます。

ポップアップモードは、モバイルデバイスで最も一般的なモードです。 Webページでは、JavaScriptの呼び出し、適切に設定された `window.open()` HTML要素、またはその他の適切な方法を使用し `A` てビューアを読み込みます。

ポップアップ操作モードには、標準搭載されたHTMLページを使用することをお勧めします。 この場合、このISビューアは、とい `CarouselViewer.html` う名前で、標準のISビューアのデプ `html5/` ロイ先のサブフォルダー内にあります。

`<s7viewers_root>/html5/CarouselViewer.html`

カスタムCSSを適用すると、視覚的なカスタマイズを行うことができます。

次の例は、ビューアを新しいウィンドウで開くHTMLコードの例です。

```
<a href="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/CarouselViewer.html?asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner&serverurl=https://adobedemo62-h.assetsadobe.com/is/image" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存のWebページに追加されます。 このWebページには、Viewerに関連しない顧客コンテンツが既に含まれている場合があります。 ビューアは通常、Webページの一部のスペースのみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、およびデバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用されます。 これは、静的レイアウトのWebページに最適な選択肢です。

レスポンシブデザイン埋め込みは、コンテナのサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定していま `DIV`す。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナのサイズ変更の方法に応じて、ビューアの動作が異なりま `DIV`す。 Webページでコンテナの幅のみが設定され、高さは無制限のまま `DIV`の場合、ビューアは、使用されるアセットの縦横比に従って高さを自動的に選択します。 この機能により、両側のパディングなしで、アセットが表示範囲にぴったりと収まるようになります。 この使用例は、Bootstrap、FoundationなどのレスポンシブWebデザインレイアウトフレームワークを使用するWebページで最も一般的です。

それ以外の場合は、Webページでビューアのコンテナの幅と高さの両方が設定されている場合、ビ `DIV`ューアはその領域だけを占めます。 また、Webページのレイアウトのサイズに従います。 良い例は、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合です。

**固定サイズ埋め込み**

ビューアをWebページに追加するには、次の手順を実行します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナの定義を参照してくだ `DIV`さい。
1. ビューアのサイズの設定
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにスクリプトタグを追加する必要があります。 ビューアのAPIを使用する前に、を必ず含めてくださ [!DNL CarouselViewer.js]い。 このフ [!DNL CarouselViewer.js] ァイルは、次に示すように、 [!DNL html5/js/] 標準のISビューアのデプロイ先のサブフォルダーにあります。

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js]

ビューアがAdobe Dynamic Media Classicサーバーの1つにデプロイされ、同じドメインから供給されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobe Dynamic Media Classicサーバーの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScriptファイルのみ `include` を参照する必要があります。 Webページコード内の追加のJavaScriptファイルを参照してはなりません。Webページコードは、ビューアのロジックによって実行時にダウンロードされる可能性があります。 特に、ビューアによって読み込まれたHTML5 SDKライブラリを、コ `Utils.js` ンテキストパス(いわゆる統合SDK `/s7viewers` ) `include`から直接参照しないでください。 この理由は、実行時のViewerライブラリの場 `Utils.js` 所がビューアのロジックで完全に管理され、ビューアのリリース間で位置が変わるからです。 アドビでは、古いバージョンのセカンダリViewerをサーバーに保 `includes` 持していません。
>
>
>その結果、新しい製品バージョンがデプロイされると、ビューアで使用さ `include` れるセカンダリJavaScriptへの直接参照をページに配置すると、将来、ビューアの機能が機能しなくなります。

1. コンテナの定義を参照してくだ `DIV`さい。

   ビューアを表 `DIV` 示するページに空の要素を追加します。 このID `DIV` は後でビューアのAPIに渡されるので、要素のIDが定義されている必要があります。 DIVのサイズはCSSで指定されます。

   プレースホル `DIV` ダーは、位置固定要素です。つまり、 `position` CSSプロパティがまたはに設定さ `relative` れていま `absolute`す。

   次に、定義済みのプレースホルダー要素の例を示 `DIV` します。

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアのサイズの設定

   ビューアの静的サイズを設定するには、最上位CSSクラスに対して絶 `.s7carouselviewer` 対単位で宣言するか、修飾子を使用し `stagesize` ます。

   サイズ調整は、CSS内でHTMLページ上に直接、またはカスタムビューアのCSSファイル内に直接配置し、後でAEM Assetsのビューアプリセットレコード（オンデマンド）に割り当てるか、コマンドを使用して明示的に渡すことがで `style` きます。

   CSSを使用した [ビューアのスタイル設定について詳しくは](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 、カルーセルビューアのカスタマイズを参照してください。

   HTMLページで静的ビューアサイズを定義する例を次に示します。

   ```
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   この修飾子は、次のように、コ `stagesize` マンドリファレンスの節で説明するように、ビューアの初期化コ `params` ードと共に、またはAPI呼び出しとして、明示的に渡すことができます。

   ```
   carouselViewer.setParam("stagesize", "1174,500");
   ```

   CSSベースのアプローチを推奨し、この例で使用します。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報をコ `s7viewers.CarouselViewer` ンストラクターに渡し、ビューアインスタンスでメソッド `init()` を呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアのコン `containerId` テナIDの名前と、ビューアでサポートされている設定パラメータを含むネストされた `params` JSONオブジェクトを保持するフィールドが必要です。 この場合、オブジェクトに `params` は、プロパティとして渡された画像サービングURLが少なくとも含まれて `serverUrl` おり、最初のアセットがパラメーターとして含まれている必要が `asset` あります。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、起動できます。

   ビューアのコンテナをDOMに追加し、ビューアのコードがIDでコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Webページの最後までDOMの構築が遅れます。 互換性を最大にするには、終了 `init()` タグの直前、またはbodyイベ `BODY` ントでメソッドを呼び出す必要があ `onload()` ります。

   同時に、コンテナ要素は、まだWebページレイアウトの一部ではない必要があります。 例えば、割り当てられたスタイルを使用して非表 `display:none` 示にすることができます。 この場合、Webページがコンテナ要素をレイアウトに戻す瞬間まで、ビューアは初期化処理を遅延します。 この場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、メソッドを呼び出 `init()` します。 この例では、がビューアイ `carouselViewer` ンスタンスであると仮定しています。はプレ `s7viewer` ースホルダの名前で `DIV`す。は画 `https://adobedemo62-h.assetsadobe.com/is/image` 像サービングのURLで、はア `/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner` セットです。

   ```
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、固定サイズのカルーセルビューアを埋め込んだ簡単なWebページの例です。

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高さ無制限のレスポンシブデザイン埋め込み**

レスポンシブデザイン埋め込みでは、Webページには通常、ビューアのコンテナの実行時のサイズを指示する柔軟なレイアウトが指定されていま `DIV`す。 次の例では、WebページでビューアのコンテナがWebブラウザーのウィンド `DIV` ウサイズの40%を占めることを前提としています。 そして、その高さは無制限のままです。 WebページのHTMLコードは次のようになります。

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 80%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

このようなページへのビューアの追加手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、ビューアのサイズを明示的に定義する必要がないことです。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナの定義を参照してくだ `DIV`さい。
1. ビューアを作成し、初期化する。

上記の手順は、固定サイズ埋め込みの場合と同じです。 既存のコンテナに `DIV` コンテナを追加しま `"holder"``DIV`す。 次のコードは完全な例です。 ブラウザのサイズが変更されたときにビューアのサイズが変化することと、ビューアの縦横比がアセットと一致することに注目してください。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 80%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用方法を説明しています。

[https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewer-responsive-unrestricted-height.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewer-responsive-unrestricted-height.html)

**幅と高さが定義されたフレキシブルサイズ埋め込み**

幅と高さが定義されたフレキシブルサイズ埋め込みの場合、Webページのスタイルは異なります。 DIVに両方のサイズを提供し `"holder"` 、ブラウザーウィンドウの中央に配置します。 また、Webページでは、要素と要素のサイズを100% `HTML` に設 `BODY` 定しています。

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

残りの埋め込み手順は、高さ無制限のレスポンシブ埋め込みで使用された手順と同じです。 結果の例を次に示します。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**セッターベースのAPIを使用した埋め込み**

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合、コンストラクターはパラメーターを受け取りません。設定パラメーターは、、、および `setContainerId()`APIメソッド `setParam()`を使用して、個別のJavaScript呼び出し `setAsset()` で指定されます。

次の例は、固定サイズ埋め込みとセッターベースのAPIの使用を示しています。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7carouselviewer { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer(); 
carouselViewer.setContainerId("s7viewer"); 
carouselViewer.setParam("serverurl", "https://adobedemo62-h.assetsadobe.com/is/image"); 
carouselViewer.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner"); 
carouselViewer.init(); 
</script> 
</body> 
</html>
```

