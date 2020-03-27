---
description: ズームビューアは、ズーム可能な画像を表示する画像ビューアです。 このビューアは画像セットで機能し、スウォッチを使用してナビゲーションを行います。 ズームツール、フルスクリーンのサポート、スウォッチ、およびオプションの閉じるボタンがあります。 デスクトップや携帯端末で動作するように設計されています。
keywords: responsive
seo-description: ズームビューアは、ズーム可能な画像を表示する画像ビューアです。 このビューアは画像セットで機能し、スウォッチを使用してナビゲーションを行います。 ズームツール、フルスクリーンのサポート、スウォッチ、およびオプションの閉じるボタンがあります。 デスクトップや携帯端末で動作するように設計されています。
seo-title: ズーム
solution: Experience Manager
title: ズーム
topic: Dynamic media
uuid: ec2a91e2-ce2c-48b1-a2b2-8671524288c7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ズーム{#zoom}

ズームビューアは、ズーム可能な画像を表示する画像ビューアです。 このビューアは画像セットで機能し、スウォッチを使用してナビゲーションを行います。 ズームツール、フルスクリーンのサポート、スウォッチ、およびオプションの閉じるボタンがあります。 デスクトップや携帯端末で動作するように設計されています。

>[!NOTE]
>
>IR（画像レンダリング）またはUGC（ユーザ生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアタイプ502

必要システム [構成と前提条件を参照してくださ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)い。

## デモURL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## ズームビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

ズームビューアは、メインのJavaScriptファイルと、ビューアによって実行時にダウンロードされるヘルパーファイルのセット（この特定のビューア、アセット、CSSで使用されるすべてのビューアSDKコンポーネントを含む1つのJavaScriptが含まれる）です。

ズームビューアは、ISビューアに付属の実稼動用HTMLページを使用するか、埋め込みモードで使用できます。また、ドキュメントに記載されたAPIを使用して、ビューアをターゲットWebページに統合します。

設定とスキン表示は、他のビューアと同様です。 スキン表示は、すべてカスタムCSSを使用して適用されます。

すべてのビ [ューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 、およびすべ [てのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## ズームビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

ズームビューアは、他のモバイルアプリケーションで一般的な次のタッチジェスチャに対応しています。 ビューアは、ユーザのスワイプジェスチャを処理できない場合、このイベントをWebブラウザに転送して、ネイティブページスクロールを実行します。 このような機能を使用すると、デバイスの画面領域のほとんどをビューアが占めている場合でも、ページ内を移動できます。

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
   <td colname="col2"> <p> スウォッチ内の新しいサムネールを選択します。 メインビューで、ユーザインターフェイス要素の表示/非表示を切り替えます。 </p> </td> 
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
   <td colname="col2"> <p> スウォッチバーのスウォッチリストをスクロールします。 </p> <p> 画像がリセット状態で、frametransitionパラメータがslideに設定さ <span class="codeph"> れてい </span> る場合、アセットはスライドアニメーションを使用して変更されます。 その他のframetransitionモードで <span class="codeph"> は、こ </span> のジェスチャはネイティブページスクロールを実行します。 </p> <p> 画像がズームインされると、画像が水平方向に移動します。 画像を表示の端まで移動し、同じ方向でスワイプを実行すると、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直方向のスワイプ </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態の場合、このジェスチャはネイティブページスクロールを実行します。 </p> <p> 画像がズームインされると、画像が垂直方向に移動します。 画像を表示の端まで移動し、同じ方向でスワイプを実行すると、ネイティブページスクロールが実行されます。 </p> <p> スウォッチ領域内でこのジェスチャを行うと、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビューアは、タッチスクリーンとマウスを備えたWindowsデバイスで、タッチ入力とマウス入力の両方をサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11およびEdge Webブラウザーのみに限定されます。

このビューアは完全にキーボードでアクセスできます。

詳しくは、キーボ [ードのアクセシビリティとナビゲーションを参照してくださ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)い。

## ズームビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

Webページが異なると、ビューアの動作に対するニーズが異なります。 Webページをクリックすると、別のブラウザーウィンドウでビューアを開くリンクが表示される場合があります。 ホストページに直接ビューアを埋め込む必要がある場合もあります。 後者の場合は、Webページが静的レイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するため、ビューアでは、次の3つの主要な操作モードがサポートされています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

**ポップアップモードについて**

ポップアップモードでは、ビューアはWebブラウザーの別のウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやデバイスの向きが変更された場合は調整されます。

このモードは、モバイルデバイスで最も一般的なモードです。 Webページでは、JavaScript呼び出し、適切に設定された `window.open()` HTML要素、またはその他の適切な方法を使用し `A` てビューアを読み込みます。

ポップアップ操作モードには、標準搭載されたHTMLページを使用することをお勧めします。 標準搭載のHTMLページが呼び出され、次のように `ZoomViewer.html` ISビューアの標準のデプロイ先の `html5/` サブフォルダーに格納されます。

`<s7viewers_root>/html5/ZoomViewer.html`

カスタムCSSを適用して、ページの外観をカスタマイズします。

次の例は、ビューアを新しいウィンドウで開くHTMLコードの例です。

```
 <a 
href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存のWebページに追加されます。既に既存のWebページには、ビューアに関連しない顧客コンテンツが含まれている場合があります。 ビューアは通常、Webページの一部のスペースのみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、また、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用されます。 このオプションは、静的レイアウトのWebページに最適です。

レスポンシブデザイン埋め込みモードは、コンテナのサイズ変更により、実行時にビューアのサイズを変更する必要があることを前提としていま `DIV`す。 最も一般的な使用例は、柔軟なレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナのサイズ変更の方法に応じて、ビューアの動作が異なりま `DIV`す。 Webページでコンテナの幅のみが設定され、高さは無制限のままの場合、 `DIV`ビューアは、使用されるアセットの縦横比に従って高さを自動的に選択します。 このロジックにより、両側のパディングなしで、アセットがビューにぴったりと収まるようになります。 この使用例は、Bootstrap、Foundationなどのレスポンシブレイアウトフレームワークを使用するWebページで最も一般的です。

Webページでビューアのコンテナの幅と高さの両方が設定されている場合、ビューアはWebペー `DIV`ジのサイズに従って領域全体を占めます。 例えば、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合などです。

## 固定サイズ埋め込み {#section-44f365e6c0dd40709467a459afa82a7f}

ビューアをWebページに追加するには、次の手順を実行します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVの定義を参照してください。
1. ビューアのサイズの設定
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにスクリプトタグを追加する必要があります。 ビューアのAPIを使用する前に、を必ず含めてくださ [!DNL ZoomViewer.js]い。 このフ [!DNL ZoomViewer.js] ァイルは、次に示すように、 [!DNL html5/js/] 標準のISビューアのデプロイ先のサブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

ビューアがAdobe Dynamic Media Classicサーバーの1つにデプロイされ、同じドメインから供給されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobe Dynamic Media Classicサーバーの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
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

   プレースホルダDIV要素の定義例を次に示します。

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアのサイズの設定

   複数項目セットを扱う場合、このビューアにはサムネールが表示され、デスクトップシステムでは、サムネールはメインビューの下に配置されます。 同時に、ビューアでは、 `setAsset()` APIを使用して実行時にメインアセットを入れ替えることができます。 開発者は、新しいアセットに項目が1つだけ含まれる場合に、下部のサムネール領域をビューアがどのように管理するかを制御できます。 ビューアの外側のサイズはそのままにし、メインビューの高さを拡大し、サムネール領域を表示させることができます。 また、メインビューのサイズを静的に保ち、ビューアの外側の領域を折りたたみ、Webコンテンツを上に移動し、サムネールから残った画面の空き領域を使用することもできます。

   ビューアの外側の境界をそのままに保つには、最上位CSSクラスの `.s7zoomviewer` サイズを絶対単位で定義します。 CSSのサイズ調整は、HTMLページまたはカスタムビューアのCSSファイルに適用できます。このCSSファイルは、後でScene7 Publishing Systemのビューアプリセットレコードに割り当てられるか、styleコマンドを使用して明示的に渡されます。

   CSSを使用した [ビューアのスタイル設定について詳しくは](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 、ズームビューアのカスタマイズを参照してください。

   HTMLページでビューアの外側の静的なサイズを定義する例を次に示します。

   ```
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次の例では、ビューアの外側を固定した場合の動作を確認できます。 セットを切り替えても、ビューアの外側のサイズは変わりません。

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html)

   メインビューのサイズを静的にするには、 `Container` SDKコンポーネントの内部のビューアサイズを、 `.s7zoomviewer` CSSセレクターを使用するか、修飾子を使用して、絶対単位で `.s7container` 定義 `stagesize` します。

   次の例では、アセットを切り替えてもメインビュー領域のサイズが変わらないように、内部 `Container` SDKコンポーネントのビューアサイズを定義します。

   ```
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次のデモページは、メインビューのサイズを固定した場合のビューアの動作を示しています。 セットを切り替えても、メインビューは静的なままで、Webページのコンテンツは垂直方向に移動します。

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html)

   修飾子は、Scene7 Publishing Systemのビ `stagesize` ューアプリセットレコードで設定するか、次に示すように、このヘルプの「コマンドリファレンス」の節で説明するように、ビューア初期化コードまたは `params` API呼び出しで明示的に渡すことができます。

   ```
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   CSSベースのアプローチを推奨し、この例で使用します。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報をコ `s7viewers.ZoomViewer` ンストラクターに渡して、ビューアインスタンスでメソッド `init()` を呼び出します。

   設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアの `containerId` コンテナIDの名前と、ビューアがサポートする設定パラメータを含むネストされた `params` JSONオブジェクトを保持するフィールドが必要です。 この場合、オブジェクトには、 `params` 少なくともプロパティとして渡された画像サービングURLと、最初のアセッ `serverUrl` トがパラメーターとして含まれている必要が `asset` あります。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、起動できます。

   ビューアのコンテナをDOMに追加し、ビューアのコードがIDでコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Webページの最後までDOMの構築が遅れます。 互換性を最大にするには、終了 `init()` タグの直前、またはbodyイベ `BODY` ントでメソッドを呼び出す必要があ `onload()` ります。

   同時に、コンテナ要素は、まだWebページレイアウトの一部ではない必要があります。 例えば、割り当てられたスタイルを使用して非表 `display:none` 示にすることができます。 この場合、Webページがコンテナ要素をレイアウトに戻す瞬間まで、ビューアは初期化処理を遅延します。 この場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、必要最小限の設定オプションをコンストラクターに渡して、メソッドを呼び出 `init()` します。 この例では、が `zoomViewer` ビューアインスタ `s7viewer` ンス、がプレースホルダDIVの名前、が画像サー `http://s7d1.scene7.com/is/image/` ビングURL、がアセットであると `Scene7SharedAssets/ImageSet-Views-Sample` 仮定しています。

   ```
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、固定サイズのビデオビューアを埋め込んだ簡単なWebページの例です。

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
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

## 高さ無制限のレスポンシブデザイン埋め込み {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

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

このようなページへのビューアの追加手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、ビューアのサイズを明示的に定義する必要がないことです。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVの定義を参照してください。
1. ビューアを作成し、初期化する。

上記の手順は、固定サイズ埋め込みの場合と同じです。 コンテナDIVを既存の `"holder"` DIVに追加します。 次のコードは完全な例です。 ブラウザのサイズが変更された場合にビューアのサイズが変化し、ビューアの縦横比がアセットと一致することに注目してください。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
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

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用方法を説明しています。

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

## 幅と高さが定義されたフレキシブルサイズ埋め込み {#section-3674e6c032594441a6576b7fb1de6e64}

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

残りの埋め込み手順は、高さ無制限のレスポンシブデザイン埋め込みで使用した手順と同じです。 結果の例を次に示します。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
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

## セッターベースのAPIを使用した埋め込み {#section-44e014925f24418b900696003855c0a9}

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合、コンストラクターはパラメーターを受け取りません。設定パラメーターは、、、および `setContainerId()`APIメソッド `setParam()`を使用して、個別のJavaScript呼び出し `setAsset()` で指定されます。

次の例は、固定サイズ埋め込みとセッターベースのAPIの使用を示しています。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 
```

