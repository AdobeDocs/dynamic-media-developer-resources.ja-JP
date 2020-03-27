---
description: インラインズームビューアは画像ビューアです。 ユーザーがメインビューをロールオーバーまたはタッチしたときに、ズームされたバージョンで静的な画像を表示します。 このビューアは画像セットで機能し、スウォッチを使用してナビゲーションを行います。 デスクトップや携帯端末で動作するように設計されています。
keywords: responsive
seo-description: インラインズームビューアは画像ビューアです。 ユーザーがメインビューをロールオーバーまたはタッチしたときに、ズームされたバージョンで静的な画像を表示します。 このビューアは画像セットで機能し、スウォッチを使用してナビゲーションを行います。 デスクトップや携帯端末で動作するように設計されています。
seo-title: インラインズーム
solution: Experience Manager
title: インラインズーム
topic: Dynamic media
uuid: 2287aef0-79ba-4d63-911a-969fa1c63385
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# インラインズーム{#inline-zoom}

インラインズームビューアは画像ビューアです。 ユーザーがメインビューをロールオーバーまたはタッチしたときに、ズームされたバージョンで静的な画像を表示します。 このビューアは画像セットで機能し、スウォッチを使用してナビゲーションを行います。 デスクトップや携帯端末で動作するように設計されています。

>[!NOTE]
>
>IR（画像レンダリング）またはUGC（ユーザ生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアのタイプは504です。

必要システム [構成と前提条件を参照してくださ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)い。

## デモURL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](http://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&stagesize=500,400)

## インラインズームビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

インラインズームビューアは、メインのJavaScriptファイルと、ビューアによって実行時にダウンロードされるヘルパーファイルのセット（この特定のビューア、アセット、CSSで使用されるすべてのビューアSDKコンポーネントを含む1つのJavaScriptが含まれる）です。

インラインズームビューアは、画像サービングビューアに付属の実稼働用HTMLページを使用するポップアップモードでも、ドキュメントに記載されたAPIを使用してターゲットWebページに統合される埋め込みモードでも、両方で使用できます。

設定とスキン表示は、他のビューアと同様です。 スキン表示を適用するには、カスタムCSSを使用します。

すべてのビ [ューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 、およびすべ [てのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## インラインズームビューアの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

インラインズームビューアは、他のモバイルアプリケーションで一般的なシングルタッチとマルチタッチのジェスチャに対応しています。

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
   <td colname="col2"> <p> フライアウトビューをアクティブにするか、スウォッチのプライマリズームレベルとセカンダリズームレベルを切り替え、新しいサムネールを選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> スウォッチバーのスウォッチリストをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直方向のスワイプ </p> </td> 
   <td colname="col2"> <p>スウォッチ領域内でこのジェスチャを行うと、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

また、タッチスクリーンとマウスを使用したWindowsデバイスでは、タッチ入力とマウス入力の両方がサポートされます。 ただし、このサポートは、Chrome、Internet Explorer 11およびEdge Webブラウザーのみに限定されます。

このビューアは完全にキーボードでアクセスできます。

詳しくは、キーボ [ードのアクセシビリティとナビゲーションを参照してくださ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)い。

## インラインズームビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

Webページが異なると、ビューアの動作に対するニーズが異なります。 Webページにクリック可能なリンクが表示され、ビューアが別のブラウザーウィンドウで開く場合があります。 ホストページに直接ビューアを埋め込む必要がある場合もあります。 後者の場合は、Webページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するため、ビューアでは、次の3つの主要な操作モードがサポートされています。ポップアップ埋め込み、固定サイズ埋め込みおよびレスポンシブ埋め込み。

**ポップアップ**

ポップアップモードでは、ビューアはWebブラウザーの別のウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーウィンドウのサイズやデバイスの向きが変更された場合は調整されます。

このモードは、モバイルデバイスで最も一般的なモードです。 Webページでは、JavaScript呼び出し、適切に設定された `window.open()` HTML要素、またはその他の適切な方法を使用し `A` てビューアを読み込みます。

というポップアップモードには、標準搭載されたHTMLページを使用することをお勧めします `FlyoutViewer.html`。 これは、次に示すように、標準の画 [!DNL html5/] 像サービングビューアのデプロイ先のサブフォルダーにあります。

`<s7viewers_root>/html5/FlyoutViewer.html`

また、FlyoutZoomViewコンポーネントをインラインズームモードで動作するように設定する必要があります。 インラインズームビューアには、あらかじめ用意されているプリセットを使用する `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` か、プリセットから派生するカスタムプリセットを使用することをお勧めします。 表示のカスタマイズは、カスタムCSSを適用することで実現できます。

次に、ビューアを新しいウィンドウで開くHTMLコードの例を示します。

```
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みとレスポンシブ埋め込み**

埋め込みモードでは、ビューアは既存のWebページに追加されます。既に既存のWebページには、ビューアに関連しない顧客コンテンツが含まれている場合があります。 ビューアは通常、Webページの一部のスペースのみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、また、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブWebページです。

固定サイズ埋め込みモードは、ビューアが最初の読み込み後にサイズを変更しない場合に使用されます。 この選択は、静的ページレイアウトのWebページに最適です。

レスポンシブデザイン埋め込みモードは、コンテナのサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定していま `DIV`す。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

インラインズームビューアでレスポンシブデザイン埋め込みモードを使用する場合は、パラメーターを使用して、メインビュー画像の明示的なブレークポイントを必ず指定して `imagereload` ください。 ブレークポイントは、WebページのCSSで指定されたビューアの幅のブレークポイントと一致させるのが理想的です。

レスポンシブデザイン埋め込みモードでは、Webページでのコンテナのサイズ変更の方法に応じて、ビューアの動作が異なりま `DIV`す。 Webページでコンテナの幅のみが設定され、高さは無制限のままの場合、 `DIV`ビューアは、使用されるアセットの縦横比に従って高さを自動的に選択します。 つまり、両側のパディングなしで、アセットがビューにぴったりと収まります。 この特定の使用例は、Bootstrap、Foundationなどのレスポンシブデザインレイアウトフレームワークを使用するWebページで最も一般的です。

それ以外の場合は、Webページでビューアのコンテナの幅と高さの両方が設定されている場合、ビューアはその領域のみを占め、Webページのレイアウトで指定されたサイズに従います。 `DIV`良い使用例は、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合です。

**固定サイズ埋め込み**

ビューアをWebページに追加するには、次の手順を実行します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナの定義を参照してくだ `DIV`さい。
1. ビューアのサイズの設定
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにスクリプトタグを追加する必要があります。 ビューアのAPIを使用する前に、を必ず含めてくださ `FlyoutViewer.js`い。 `FlyoutViewer.js` は、標準のISビューアデプ [!DNL html5/js/] ロイ先の次のサブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

ビューアがAdobe Scene7サーバの1つにデプロイされ、同じドメインから供給されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobe Scene7サーバの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScriptファイルのみ `include` を参照する必要があります。 Webページコード内の追加のJavaScriptファイルを参照してはなりません。Webページコードは、ビューアのロジックによって実行時にダウンロードされる可能性があります。 特に、ビューアによって読み込まれたHTML5 SDKライブラリを、コ `Utils.js` ンテキストパス(いわゆる統合SDK `/s7viewers` ) `include`から直接参照しないでください。 この理由は、実行時のViewerライブラリの場 `Utils.js` 所がビューアのロジックで完全に管理され、ビューアのリリース間で位置が変わるからです。 アドビでは、古いバージョンのセカンダリViewerをサーバーに保 `includes` 持していません。
>
>
>その結果、新しい製品バージョンがデプロイされると、ビューアで使用さ `include` れるセカンダリJavaScriptへの直接参照をページに配置すると、将来、ビューアの機能が機能しなくなります。

1. コンテナDIVの定義を参照してください。

   ビューアを表示するページに空のDIV要素を追加します。 このIDは後でビューアのAPIに渡されるので、DIV要素のIDを定義する必要があります。

   プレースホルダDIVは、位置固定要素です。つまり、 `position` CSSプロパティがまたはに設定さ `relative` れていま `absolute`す。

   プレースホルダDIV要素の適切な値は、Webページで `z-index` 指定する必要があります。 これにより、ビューアのフライアウト部分がWebページの他の要素の上に表示されます。

   プレースホルダDIV要素の定義例を次に示します。

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. ビューアのサイズの設定

   複数項目セットを扱う場合、このビューアにはサムネールが表示されます。 デスクトップシステムでは、サムネールはメインビューの下に配置されます。 同時に、ビューアでは、実行時に `setAsset()` APIを使用してメインアセットを入れ替えることができます。 開発者は、新しいアセットに項目が1つだけ含まれている場合に、下部のサムネール領域をビューアがどのように管理するかを制御できます。 ビューアの外側のサイズはそのままにし、メインビューの高さを拡大して、サムネール領域を表示させることができます。 また、メインビューのサイズを静的に保ち、ビューアの外側の領域を折りたたんで、Webコンテンツを上に移動し、サムネールの残りの空きページ領域を使用することもできます。

   ビューアの外側の境界をそのままに保つには、最上位CSSク `.s7flyoutviewer` ラスのサイズを絶対単位で定義します。 CSSのサイズ調整は、HTMLページまたはカスタムビューアのCSSファイルに適用できます。このファイルは、後でScene7 Publishing Systemのビューアプリセットレコードに割り当てられるか、styleコマンドを使用して明示的に渡されます。

   CSSを使用した [ビューアのスタイル設定について詳しくは](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) 、インラインズームビューアのカスタマイズを参照してください。

   HTMLページでビューアの外側の静的なサイズを定義する例を次に示します。

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   ビューアの外側の領域を固定した場合の動作は、次のサンプルページで確認できます。 セットを切り替えても、ビューアの外側のサイズは変わりません。

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-outer-area.html)

   メインビューのサイズを静的にするには、 `Container` CSSセレクターを使用して、内部の `.s7flyoutviewer .s7container` SDKコンポーネントのビューアサイズを絶対単位で定義します。 また、初期設定のビューアCSSの最上位CSSクラスに対して定 `.s7flyoutviewer` 義された固定サイズをに設定して上書きする必要がありま `auto`す。

   次の例では、アセットを切り替えてもメインビュー領域のサイズが変わらないように、内部 `Container` SDKコンポーネントのビューアサイズを定義します。

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

   次のサンプルページは、メインビューのサイズを固定した場合のビューアの動作を示しています。 セットを切り替えても、メインビューは静的なままで、Webページのコンテンツは垂直方向に移動します。

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-main-view.html)

   また、初期設定のビューアCSSでは、その外側の領域の固定サイズが標準で提供されます。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報をコ `s7viewers.FlyoutViewer` ンストラクターに渡して、ビューアインスタンスでメソッド `init()` を呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアのコンテ `containerId` ナIDの名前と、ビューアがサポートする設定パラメータを含むネストされた `params` JSONオブジェクトを保持するフィールドが必要です。 この場合、オブジェクト `params` には、プロパティとして渡された画像サービングURL、初期アセットをパラメーターとして、 `serverUrl` CSSをパラメーターとして読み込むためのベースパス、プリセット名をパラメ `asset` ーターとして含む `contentUrl` 必要が `config` あります。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、起動できます。

   ビューアのコンテナをDOMに追加し、ビューアのコードがIDでコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Webページの最後までDOMの構築が遅れます。 互換性を最大にするには、終了 `init()` タグの直前、またはbodyイベ `BODY` ントでメソッドを呼び出す必要があ `onload()` ります。

   同時に、コンテナ要素は、まだWebページレイアウトの一部ではない必要があります。 例えば、割り当てられたスタイルを使用して非表 `display:none` 示にすることができます。 この場合、Webページがコンテナ要素をレイアウトに戻す瞬間まで、ビューアは初期化処理を遅延します。 この場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、必要最小限の設定オプションをコンストラクターに渡して、メソッドを呼び出 `init()` します。 この例では、がビューアイ `inlineZoomViewer` ンスタンスであると仮定しています。はプレ `s7viewer` ースホルダの名前で `DIV`す。は画 `http://s7d1.scene7.com/is/image/` 像サービングのURLです。とは `Scene7SharedAssets/ImageSet-Views-Sample` アセットです。

   ```
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
   "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、固定サイズのインラインズームビューアを埋め込んだ簡単なWebページの例です。

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
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## 高さ無制限のレスポンシブデザイン埋め込み {#section-056cb574713c4d07be6d07cf3c598839}

レスポンシブデザイン埋め込みでは、Webページには通常、ビューアのコンテナの実行時のサイズを指示する柔軟なレイアウトが指定されていま `DIV`す。 次の例では、WebページでビューアのコンテナがWebブラウザーのウィンドウサイズの40%を取ることを許可し、高さ `DIV` は無制限のままにしているとします。 WebページのHTMLコードは次のようになります。

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

このようなページへのビューアの追加手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、初期設定のビューアCSSの固定サイズを、相対的な単位で設定されたサイズで上書きする必要がある点です。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナの定義を参照してくだ `DIV`さい。
1. ビューアのサイズの設定
1. ビューアを作成し、初期化する。

上記の手順はすべて、固定サイズ埋め込みの場合と同じですが、次の3つの例外があります。

* コンテナを既存の「 `DIV` ホルダー」に追加しま `DIV`す。
* 明示的なブレ `imagereload` ークポイントを持つパラメーターを追加しました。
* 絶対単位を使用してビューアの固定サイズを設定する代わりに、次のようにビューアを100 % `width` に設定 `height` するCSSを使用します。

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

次のコードは完全な例です。 ブラウザのサイズが変更されたときにビューアのサイズが変化することと、ビューアの縦横比がアセットと一致することに注目してください。

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
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用方法を説明しています。

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

## 幅と高さが定義されたフレキシブルサイズ埋め込み {#section-0a329016f9414d199039776645c693de}

幅と高さが定義されたフレキシブルサイズ埋め込みの場合、Webページのスタイルは異なります。 これは、両方のサイズを `"holder"` DIVに提供し、ブラウザーウィンドウの中央に配置します。 また、Webページでは、要素と要素のサイズを100% `HTML` に設 `BODY` 定しています。

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
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## セッターベースのAPIを使用した埋め込み {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合、コンストラクターはパラメーターを受け取りません。設定パラメーターは、、、お `setContainerId()`よびAPI `setParam()`メソッドを使用して、 `setAsset()` 別々のJavaScript呼び出しで指定されます。

次の例は、固定サイズ埋め込みとセッターベースのAPIの使用を示しています。

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
var inlineZoomViewer = new s7viewers.FlyoutViewer(); 
inlineZoomViewer.setContainerId("s7viewer"); 
inlineZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
inlineZoomViewer.setParam("config", "Scene7SharedAssets/Universal_HTML5_Zoom_Inline"); 
inlineZoomViewer.setParam("contenturl", "http://s7d1.scene7.com/is/content/"); 
inlineZoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
inlineZoomViewer.init(); 
</script> 
</body> 
</html>
```

