---
title: インラインズーム
description: インラインズームビューアは、画像ビューアです。 ユーザーがロールオーバーするか、メインビューに触れたときに、その静止画像の上に表示されるズームバージョンの静止画像が表示されます。 このビューアは画像セットで機能し、ナビゲーションはスウォッチを使用して行われます。 デスクトップやモバイルデバイスで動作するように設計されています。
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 33e661b0-be5e-4d37-af88-47f7bc433c01
TQID: 'https://experienceleague.adobe.com/Ax15caVJejy24gSoUX0wsA4cOjSR08FLNtpAjr06LtI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 2305
ht-degree: 0%

---

# インラインズーム{#inline-zoom}

インラインズームビューアは、画像ビューアです。 ユーザーがロールオーバーするか、メインビューに触れたときに、その静止画像の上に表示されるズームバージョンの静止画像が表示されます。 このビューアは画像セットで機能し、ナビゲーションはスウォッチを使用して行われます。 デスクトップやモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR （画像レンダリング）またはUGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアータイプは504です。

[必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## インラインズームビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

インラインズームビューアは、メインのJavaScript ファイルと、実行時にビューアによってダウンロードされたすべてのビューアSDK コンポーネント、アセット、CSSを含む一連のヘルパーファイルを表します（1つのJavaScriptには、この特定のビューアで使用されるすべてのビューア コンポーネントが含まれます）。

インラインズームビューアは、画像サービングビューアを備えた実稼動対応のHTML ページを使用するポップアップモードと、文書化されたAPIを使用してターゲット web ページに統合する埋め込みモードの両方で使用できます。

設定とスキニングは、他のビューアと同様です。 カスタム CSSを使用してスキニングを適用できます。

すべてのビューアに共通する[&#x200B; コマンド参照 – 構成属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通するコマンド参照 – URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください

## インラインズームビューアの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

インラインズームビューアは、他のモバイルアプリケーションで一般的なシングルタッチおよびマルチタッチジェスチャーをサポートしています。

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
   <td colname="col2"> <p> フライアウトビューをアクティブ化するか、スウォッチのプライマリズームレベルとセカンダリズームレベルの間で変更し、新しいサムネールを選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> スウォッチバーのスウォッチのリストをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>縦方向スワイプ </p> </td> 
   <td colname="col2"> <p>ジェスチャーがスウォッチ領域内で行われた場合、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビューアは、タッチスクリーンとマウスを備えたWindows デバイスでのタッチ入力とマウス入力の両方をサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11、およびEdgeのweb ブラウザーのみに限定されます。

このビューアにはキーボードから完全にアクセス可能です。

[&#x200B; キーボードのアクセシビリティとナビゲーション &#x200B;](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## インラインズームビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

web ページごとに、閲覧者の行動に対するニーズは異なります。 Web ページで、別のブラウザーウィンドウでビューアを開くクリック可能なリンクが提供されることがあります。 それ以外の場合、ビューアをホスティングページに直接埋め込む必要がある場合があります。 後者の場合、web ページは静的なページレイアウトを使用するか、異なるデバイスで異なる表示を行うレスポンシブデザインを使用するか、または異なるブラウザーウィンドウのサイズを使用します。 これらのニーズに対応するために、ビューアでは、ポップアップ、固定サイズの埋め込み、レスポンシブ埋め込みの3つの主要な操作モードをサポートしています。

**ポップアップ**

ポップアップモードでは、ビューアは別のweb ブラウザーウィンドウまたはタブで開きます。 ブラウザーウィンドウ領域全体を使用し、ブラウザーウィンドウのサイズ変更やデバイスの向きの変更を行うときに調整します。

このモードは、モバイルデバイスで最も一般的です。 Web ページは、`window.open()` JavaScript呼び出し、適切に設定された`A` HTML要素、またはその他の適切な方法を使用してビューアを読み込みます。

`FlyoutViewer.html`というポップアップモードには、標準のHTML ページを使用することをお勧めします。 これは、標準のImage Serving-Viewers デプロイメントの[!DNL html5/] サブフォルダーにあります。

`<s7viewers_root>/html5/FlyoutViewer.html`

また、インラインズームモードで動作するようにFlyoutZoomView コンポーネントを設定する必要があります。 インラインズームビューアには、標準の`Scene7SharedAssets/Universal_HTML5_Zoom_Inline` プリセットまたはインラインズームビューアから派生したカスタムプリセットを使用することをお勧めします。 カスタム CSSを適用することで、視覚的なカスタマイズを実現できます。

次に、ビューアを新しいウィンドウで開くHTML コードの例を示します。

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みとレスポンシブ埋め込み**

埋め込みモードでは、ビューアは既存のweb ページに追加されます。このページには、ビューアに関連しない顧客コンテンツが既に含まれている可能性があります。 通常、閲覧者はweb ページの不動産の一部しか占めていません。

主なユースケースは、デスクトップ PCやタブレットデバイス向けのweb ページです。また、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブ web ページも使用できます。

固定サイズ埋め込みモードは、ビューアが初期読み込み後にサイズを変更しない場合に使用されます。 このオプションは、静的ページレイアウトを持つweb ページに最適です。

レスポンシブデザイン埋め込みモードは、コンテナ `DIV`のサイズ変更に応じて、実行時にビューアのサイズを変更する必要があることを前提としています。 最も一般的なユースケースは、柔軟性の高いページレイアウトを使用するweb ページにビューアを追加することです。

インラインズームビューアでレスポンシブデザイン埋め込みモードを使用する場合は、`imagereload` パラメーターを使用して、メインビュー画像に明示的なブレークポイントを指定してください。 理想的には、Web ページ CSSで指定されているビューアの幅のブレークポイントとブレークポイントを一致させます。

レスポンシブデザイン埋め込みモードでは、web ページコンテナ `DIV`のサイズに応じてビューアの動作が異なります。 Web ページがコンテナ `DIV`の幅のみを設定し、高さを制限しない場合、ビューアは使用されるアセットの縦横比に応じて自動的に高さを選択します。 この機能により、側面にパディングすることなく、アセットがビューに完全に収まります。 このユースケースは、BootstrapやFoundationなどのレスポンシブデザインレイアウトフレームワークを使用するweb ページで最も一般的です。

それ以外の場合、web ページがビューアのコンテナ `DIV`の幅と高さの両方を設定すると、ビューアはその領域のみを塗りつぶし、web ページレイアウトによって提供されるサイズに従います。 良い使用例は、ビューアをモーダルオーバーレイに埋め込むことです。このオーバーレイは、web ブラウザーのウィンドウサイズに応じてサイズが調整されます。

**固定サイズ埋め込み**

次の操作を実行して、ビューアをweb ページに追加します。

1. ビューアのJavaScript ファイルをweb ページに追加します。
1. コンテナ `DIV`を定義しています。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. ビューアのJavaScript ファイルをweb ページに追加します。

   ビューアを作成するには、HTML ヘッドにスクリプトタグを追加する必要があります。 ビューアーAPIを使用する前に、`FlyoutViewer.js`を含めることを確認してください。 `FlyoutViewer.js`は、標準のIS-Viewers デプロイメントの次の[!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

ビューアがAdobe Dynamic Media サーバーのいずれかにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-ViewersがインストールされているAdobe Dynamic Media サーバーの1つにフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメイン ビューア JavaScript `include` ファイルのみを参照してください。 実行時にビューアのロジックによってダウンロードされる可能性があるweb ページコード内の他のJavaScript ファイルを参照しないでください。 特に、`/s7viewers` コンテキストパス（いわゆる統合SDK `include`）からビューアによって読み込まれたHTML5 SDK `Utils.js` ライブラリを直接参照しないでください。 その理由は、`Utils.js`または類似のランタイムビューアーライブラリの場所が、ビューアーのロジックによって完全に管理され、ビューアーリリース間で場所が変更されるためです。 Adobeは、古いバージョンのセカンダリビューア `includes`をサーバー上に保持しません。
>
>
>その結果、ビューアがページ上で使用するセカンダリ JavaScript `include`を直接参照すると、新しい製品バージョンがデプロイされる際に、将来的にビューア機能が破損します。

1. コンテナ DIVの定義。

   ビューアを表示するページに、空のDIV エレメントを追加します。 このIDは後でビューア APIに渡されるので、DIV要素にはIDが定義されている必要があります。

   プレースホルダーDIVは配置された要素です。`position` CSS プロパティが`relative`または`absolute`に設定されていることを意味します。

   プレースホルダーのDIV要素に適切な`z-index`を指定するのは、web ページの責任です。 これにより、ビューアのフライアウト部分が他のweb ページ要素の上に表示されます。

   次に、定義済みのプレースホルダーDIV要素の例を示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. ビューアサイズの設定。

   このビューアは、複数の項目セットを操作する際にサムネールを表示します。 デスクトップシステムでは、サムネールはメインビューの下に配置されます。 同時に、ビューアでは、`setAsset()` APIを使用して、ランタイム中にメインアセットを入れ替えることができます。 開発者は、新しいアセットが1つのアイテムしか持たない場合に、ビューアが下部エリアのサムネール領域をどのように管理するかを制御できます。 外のビューアのサイズを維持し、メインビューの高さを上げてサムネール領域を占有させることができます。 または、メインビューサイズを静的にして外側のビューア領域を折りたたみ、web ページのコンテンツを上に移動させ、サムネールから残った無料ページの不動産を使用することもできます。

   外部ビューアの境界を維持するには、`.s7flyoutviewer` トップレベル CSS クラスのサイズを絶対単位で定義します。 CSSでのサイズ変更は、HTML ページまたはカスタムビューア CSS ファイルに配置し、後でDynamic Media Classicのビューアプリセットレコードに割り当てるか、スタイルコマンドを使用して明示的に渡すことができます。

   CSSを使用したビューアのスタイル設定について詳しくは、[&#x200B; インラインズームビューアのカスタマイズ &#x200B;](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451)を参照してください。

   次に、HTML ページの静的外部ビューアサイズを定義する例を示します。

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

<!-- You can see the behavior with a fixed outer viewer area on the following sample page. Notice that when you switch between sets, the outer viewer size does not change:-->

<!--

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html)

-->

メインビューのディメンションを静的にするには、`.s7flyoutviewer .s7container` CSS セレクターを使用して、内部`Container` SDK コンポーネントのビューアーサイズを絶対単位で定義します。 さらに、デフォルトのビューア CSSの`.s7flyoutviewer`の最上位CSS クラスに定義されている固定サイズを`auto`に設定して上書きする必要があります。

次に、アセットを切り替える際にメインビュー領域のサイズが変更されないように、内部`Container` SDK コンポーネントのビューアーサイズを定義する例を示します。

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: auto; 
 height: auto; 
}  
#s7viewer.s7flyoutviewer .s7container { 
 width: 640px; 
 height: 480px; 
}
```

<!-- The following sample page shows viewer behavior with a fixed main view size. Notice that when you switch between sets, the main view remains static and the web page content moves vertically: -->

<!--

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html)

-->

また、デフォルトのビューア CSSでは、標準装備の外部領域の固定サイズが提供されます。

1. ビューアの作成と初期化。

   上記の手順を完了したら、`s7viewers.FlyoutViewer` クラスのインスタンスを作成し、すべての構成情報をそのコンストラクターに渡し、ビューアーインスタンスで`init()` メソッドを呼び出します。 構成情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアコンテナ IDの名前を保持する`containerId` フィールドと、ビューアがサポートする設定パラメーターを含むネストされた`params` JSON オブジェクトが必要です。 この場合、`params` オブジェクトには、少なくとも`serverUrl` プロパティとして渡されたImage Serving URL、最初のアセットは`asset` パラメーター、CSSを`contentUrl` パラメーターとして読み込むための基本パス、プリセット名は`config` パラメーターである必要があります。 JSON ベースの初期化APIを使用すると、1行のコードでビューアを作成および開始できます。

   ビューアコードがIDでコンテナ要素を見つけられるように、ビューアコンテナをDOMに追加することが重要です。 一部のブラウザーは、Web ページの最後までDOMの構築を遅らせます。 互換性を最大限に高めるには、終了`BODY` タグの直前または本文`onload()` イベントで`init()` メソッドを呼び出します。

   同時に、コンテナ要素は必ずしもweb ページレイアウトの一部であってはなりません。 例えば、割り当てられた`display:none` スタイルを使用して非表示にすることができます。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで初期化プロセスを遅らせます。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

   次に、ビューアインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡して`init()` メソッドを呼び出す例を示します。 この例では、`inlineZoomViewer`がビューアインスタンスであり、`s7viewer`はプレースホルダー`DIV`の名前、`http://s7d1.scene7.com/is/image/`は画像サービング URLであり、`Scene7SharedAssets/ImageSet-Views-Sample`はアセットであると仮定しています。

   ```html {.line-numbers}
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

   次のコードは、インラインズームビューアを固定サイズで埋め込む面倒なweb ページの完全な例です。

   ```html {.line-numbers}
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

## 無制限の高さを持つレスポンシブデザイン埋め込み {#section-056cb574713c4d07be6d07cf3c598839}

レスポンシブデザインの埋め込みでは、通常、web ページには、ビューアのコンテナ `DIV`のランタイムサイズを決定する、ある種の柔軟なレイアウトが配置されています。 次の例では、web ページでビューアのコンテナ `DIV`がweb ブラウザーのウィンドウ サイズの40%を使用でき、高さは制限されないと仮定します。 Web ページのHTML コードは次のようになります。

```html {.line-numbers}
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

このようなページにビューアを追加することは、固定サイズ埋め込みの手順と似ています。 唯一の違いは、デフォルトのビューア CSSの固定サイズを、相対単位で設定したサイズで上書きする必要があることです。

1. ビューアのJavaScript ファイルをweb ページに追加します。
1. コンテナ `DIV`を定義しています。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

上記のすべての手順は、次の3つの例外を除いて、固定サイズの埋め込みと同じです。

* コンテナ `DIV`を既存の「所有者」 `DIV`に追加します。
* 明示的なブレークポイントを含む`imagereload` パラメーターを追加しました。
* 絶対単位を使用して固定のビューアサイズを設定する代わりに、次のようにビューア `width`と`height`を100%に設定するCSSを使用します。

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

次のコードは、完全な例です。 ブラウザーのサイズを変更するとビューアのサイズが変わり、ビューアの縦横比がアセットとどのように一致するかを確認します。

```html {.line-numbers}
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

次のサンプルページでは、高さの制限のないレスポンシブデザイン埋め込みをより実際に使用する方法を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--

[Alternate demo location](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

-->

## 幅と高さが定義された柔軟なサイズ埋め込み {#section-0a329016f9414d199039776645c693de}

幅と高さが定義された柔軟なサイズの埋め込みがある場合、web ページのスタイルが異なります。 `"holder"` DIVに両方のサイズを提供し、ブラウザーウィンドウに中央に配置します。 また、web ページでは、`HTML`要素と`BODY`要素のサイズが100%に設定されています。

```html {.line-numbers}
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

残りの埋め込み手順は、高さの制限のないレスポンシブデザイン埋め込みに使用する手順と同じです。 結果として得られる例は次のとおりです。

```html {.line-numbers}
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

## Setter ベースのAPIを使用した埋め込み {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

JSON ベースの初期化を使用する代わりに、セッターベースのAPIとno-args コンストラクターを使用できます。 このAPI コンストラクターを使用すると、パラメーターは受け取られず、設定パラメーターは`setContainerId()`、`setParam()`、および`setAsset()` API メソッドを使用して指定され、別々のJavaScript呼び出しが行われます。

次の例は、セッターベースのAPIを使用した固定サイズの埋め込みを使用する方法を示しています。

```html {.line-numbers}
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
