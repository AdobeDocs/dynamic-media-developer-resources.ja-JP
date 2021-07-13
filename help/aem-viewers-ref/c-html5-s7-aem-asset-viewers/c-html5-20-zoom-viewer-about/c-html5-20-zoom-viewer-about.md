---
description: ズームビューアは、ズーム可能な画像を表示する画像ビューアです。 このビューアは画像セットで機能し、ナビゲーションはスウォッチを使用しておこないます。 このビューアには、ズームツール、フルスクリーンのサポート、スウォッチ、およびオプションの閉じるボタンがあります。 デスクトップおよびモバイルデバイスで動作するように設計されています。
keywords: レスポンシブ
solution: Experience Manager
title: ズーム
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '2404'
ht-degree: 0%

---

# ズーム{#zoom}

ズームビューアは、ズーム可能な画像を表示する画像ビューアです。 このビューアは画像セットで機能し、ナビゲーションはスウォッチを使用しておこないます。 このビューアには、ズームツール、フルスクリーンのサポート、スウォッチ、およびオプションの閉じるボタンがあります。 デスクトップおよびモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR（画像レンダリング）またはUGC（ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアタイプ502

[必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

## デモURL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## ズームビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

ズームビューアは、メインのJavaScriptファイルと、ヘルパーファイルのセット（この特定のビューア、アセット、CSSで使用されるすべてのビューアSDKコンポーネントを含む単一のJavaScriptインクルード）です。

ズームビューアは、ISビューアに付属する実稼動用のHTMLページを使用してポップアップモードで、または埋め込みモードで、ドキュメントに記載されたAPIを使用してターゲットWebページに統合できます。

設定とスキン表示は、他のビューアと同様です。 スキンの適用はすべて、カスタムCSSを使用して行います。

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください。

## ズームビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

ズームビューアは、他のモバイルアプリケーションで一般的な以下のタッチジェスチャに対応しています。 ビューアでユーザのスワイプジェスチャを処理できない場合、このイベントがWebブラウザーに転送され、ネイティブページスクロールが実行されます。 このような機能を使用すると、デバイスの画面領域のほとんどをビューアが占めている場合でも、ユーザーはページ内を移動できます。

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
   <td colname="col2"> <p> スウォッチ内の新しいサムネールを選択します。 メインビューでは、ユーザーインターフェイス要素の表示と非表示が切り替わります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ダブルタップ </p> </td> 
   <td colname="col2"> <p> 最大の拡大率に達するまで、1レベルズームインします。 次のダブルタップジェスチャを実行すると、ビューアが初期の表示状態にリセットされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ピンチ </p> </td> 
   <td colname="col2"> <p>ズームインまたはズームアウトします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平方向のスワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> スウォッチバーのスウォッチリストをスクロールします。 </p> <p> 画像がリセット状態で、<span class="codeph"> frametransition </span>パラメーターがslideに設定されている場合、アセットはスライドアニメーションによって変更されます。 その他の<span class="codeph"> frametransition </span>モードの場合、このジェスチャはネイティブページスクロールを実行します。 </p> <p> 画像がズームインされると、画像は水平方向に移動します。 画像を表示の端まで移動して、同じ方向でスワイプを実行すると、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直方向のスワイプ </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態の場合にこのジェスチャを行うと、ネイティブページスクロールが実行されます。 </p> <p> 画像がズームインされると、画像は垂直方向に移動されます。 画像を表示の端まで移動して、同じ方向でスワイプを実行すると、ネイティブページスクロールが実行されます。 </p> <p> スウォッチ領域内でこのジェスチャを実行すると、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

タッチスクリーンとマウスを備えたWindowsデバイスでは、タッチ入力とマウス入力の両方がサポートされます。 ただし、このサポートは、Chrome、Internet Explorer 11およびEdge Webブラウザーのみに制限されます。

このビューアは完全にキーボードでアクセス可能です。

[キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## ズームビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Webページごとに異なります。 Webページにリンクが表示され、このリンクをクリックすると別のブラウザーウィンドウでビューアが開く場合があります。 ホスティングページに直接ビューアを埋め込む必要がある場合もあります。 後者の場合は、Webページが静的レイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは次の3つの主要な操作モードがサポートされています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別のWebブラウザーウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやデバイスの向きが変更された場合は調整されます。

このモードは、モバイルデバイスで最も一般的なモードです。 Webページでは、`window.open()` JavaScript呼び出し、適切に設定された`A` HTML要素またはその他の適切な方法を使用してビューアを読み込みます。

ポップアップ操作モードには、標準搭載されたHTMLページを使用することをお勧めします。 標準提供のHTMLページは`ZoomViewer.html`と呼ばれ、次のように、標準のIS-Viewersデプロイメントの`html5/`サブフォルダーにあります。

`<s7viewers_root>/html5/ZoomViewer.html`

カスタムCSSを適用して、ページの外観をカスタマイズします。

以下は、新しいウィンドウでビューアを開くHTMLコードの例です。

```
 <a 
href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存のWebページに追加されます。既に、ビューアに関連していない顧客コンテンツが含まれている場合があります。 ビューアは、通常、Webページの一部の領域のみを占有します。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、また、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 このオプションは、静的レイアウトのWebページに最適です。

レスポンシブデザイン埋め込みモードは、コンテナ`DIV`のサイズ変更により、実行時にビューアのサイズを変更する必要がある場合を想定しています。 最も一般的な使用例は、柔軟なレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナ`DIV`のサイズ変更の方法によって、ビューアの動作が異なります。 Webページでコンテナ`DIV`の幅のみが設定され、高さは無制限のままの場合、ビューアでは、使用するアセットの縦横比に従って高さが自動的に選択されます。 このロジックにより、両側のパディングなしで、アセットが表示にぴったりと収まります。 この使用例は、Bootstrap、Foundationなどのレスポンシブレイアウトフレームワークを使用するWebページで最も一般的です。

Webページでビューアのコンテナ`DIV`の幅と高さの両方が設定されている場合、ビューアはその領域を占め、Webページに指定されているサイズに従います。 例えば、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合などです。

## 固定サイズ埋め込み {#section-44f365e6c0dd40709467a459afa82a7f}

ビューアをWebページに追加するには、次の手順を実行します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVを定義する。
1. ビューアのサイズを設定する。
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにscriptタグを追加する必要があります。 ビューアのAPIを使用するには、必ず[!DNL ZoomViewer.js]を含めてください。 [!DNL ZoomViewer.js]ファイルは、次に示すように、IS-Viewersの標準のデプロイ先の[!DNL html5/js/]サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

ビューアがDynamic Media ClassicAdobeのいずれかにデプロイされ、同じドメインから提供されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobeDynamic Media Classicサーバーの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
```

>[!NOTE]
>
>ページ上では、メインビューアのJavaScript `include`ファイルのみを参照する必要があります。 実行時にビューアのロジックによってダウンロードされる可能性のあるWebページコード内の追加のJavaScriptファイルは、参照しないでください。 特に、ビューアによって`/s7viewers`コンテキストパスから読み込まれたHTML5 SDK `Utils.js`ライブラリを直接参照しないでください（いわゆる統合SDK `include`）。 理由は、`Utils.js`や類似のランタイムビューアライブラリの場所は、ビューアのロジックによって完全に管理され、ビューアのリリースによって位置が変わるからです。 Adobeでは、セカンダリビューア`includes`の古いバージョンはサーバに保持されません。
>
>
>その結果、新しい製品バージョンがデプロイされると、ビューアが使用するセカンダリJavaScript `include`への直接参照をページに配置すると、将来ビューア機能が壊れます。

1. コンテナDIVを定義する。

   ビューアを表示するページに空のDIV要素を追加します。 DIV要素では、IDが定義されている必要があります。このIDは、後でビューアのAPIに渡されます。

   プレースホルダーDIVは配置を指定する要素で、CSSの`position`プロパティを`relative`または`absolute`に設定します。

   プレースホルダーDIV要素の定義例を次に示します。

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアのサイズを設定する。

   複数項目セットを操作する場合、このビューアにはサムネールが表示されます。デスクトップシステムでは、サムネールはメインビューの下に配置されます。 同時に、ビューアでは、実行時に`setAsset()` APIを使用してメインアセットを入れ替えることができます。 開発者は、新しいアセットに項目が1つしかない場合に、下部のサムネール領域をビューアでどのように管理するかを制御できます。 ビューアの外側のサイズはそのままにし、メインビューの高さを拡大してサムネール領域を表示させることができます。 また、メインビューのサイズを静的に保ち、ビューアの外側の領域を折りたたみ、Webページコンテンツを上に移動して、サムネールから残された画面の空き領域を使用することもできます。

   ビューアの外側の境界をそのまま残すには、最上位CSSクラス`.s7zoomviewer`のサイズを絶対単位で定義します。 CSSのサイズ設定は、HTMLページまたはカスタムビューアのCSSファイルに適用できます。このCSSファイルは、後でDynamic Media Classicのビューアプリセットレコードに割り当てられるか、styleコマンドを使用して明示的に渡されます。

   CSSでのビューアのスタイル設定について詳しくは、 [ズームビューアのカスタマイズ](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)を参照してください。

   以下は、HTMLページでビューアの外側の静的サイズを定義する例です。

   ```
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次の例では、ビューアの外側を固定した場合の動作を確認できます。 セットを切り替えても、ビューアの外側のサイズは変わりません。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html)

   メインビューの画像サイズを静的にするには、`.s7zoomviewer` `.s7container` CSSセレクターを使用するか、`stagesize`修飾子を使用して、内部の`Container` SDKコンポーネントのビューアサイズを絶対単位で定義します。

   次の例では、アセットを切り替えてもメインビュー領域のサイズが変わらないように、内部の`Container` SDKコンポーネントのビューアサイズを定義します。

   ```
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次のデモページは、メインビューのサイズを固定した場合のビューアの動作を示しています。 セットを切り替えても、メインビューは静的なままになり、Webページのコンテンツは垂直に移動します。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html)

   `stagesize`修飾子は、Dynamic Media Classicのビューアプリセットレコードで設定することも、次に示すように、 `params`コレクションを使用してビューア初期化コードを明示的に、またはこのヘルプの「コマンドリファレンス」の節で説明するAPI呼び出しで渡すこともできます。

   ```
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   CSSベースのアプローチを推奨し、この例で使用します。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、`s7viewers.ZoomViewer`クラスのインスタンスを作成し、すべての設定情報をコンストラクターに渡して、ビューアインスタンスで`init()`メソッドを呼び出します。

   設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 最低でも、このオブジェクトには`containerId`フィールドが必要です。このフィールドには、ビューアのコンテナIDの名前と、ビューアがサポートする設定パラメーターを含むネストされた`params` JSONオブジェクトが含まれています。 この場合、`params`オブジェクトには、`serverUrl`プロパティとして渡された画像サービングURLが少なくとも含まれ、初期アセットが`asset`パラメーターとして含まれている必要があります。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、起動できます。

   ビューアのコードがIDでコンテナ要素を見つけられるように、ビューアのコンテナをDOMに追加することが重要です。 一部のブラウザーは、Webページの終わりまでDOMの構築を遅らせます。 互換性を最大にするには、 `BODY`終了タグの直前、または本文の`onload()`イベントで`init()`メソッドを呼び出します。

   同時に、コンテナ要素は、必ずしもまだWebページレイアウトの一部ではないはずです。 例えば、`display:none`スタイルを割り当てて非表示にすることができます。 この場合、Webページでコンテナ要素がレイアウトに戻るまで、ビューアの初期化プロセスが遅れます。 この場合、ビューアの読み込みが自動的に再開されます。

   以下の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、 `init()`メソッドを呼び出します。 この例では、 `zoomViewer`をビューアインスタンス、 `s7viewer`をプレースホルダーDIVの名前、 `http://s7d1.scene7.com/is/image/`を画像サービングURL、 `Scene7SharedAssets/ImageSet-Views-Sample`をアセットと仮定しています。

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

このようなページにビューアを追加する手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、ビューアのサイズを明示的に定義する必要がない点です。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVを定義する。
1. ビューアを作成し、初期化する。

上記の手順は、固定サイズ埋め込みの場合と同じです。 コンテナDIVを既存の`"holder"` DIVに追加します。 次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化することと、ビューアの縦横比がアセットと一致することに注意してください。

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

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用例を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## 幅と高さが定義されたフレキシブルサイズ埋め込み {#section-3674e6c032594441a6576b7fb1de6e64}

幅と高さが定義されたフレキシブルサイズ埋め込みの場合、Webページのスタイル設定は異なります。 `"holder"` DIVに両方のサイズを提供し、ブラウザーウィンドウの中央に配置します。 また、Webページでは、`HTML`要素と`BODY`要素のサイズを100%に設定します。

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

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合は、コンストラクターにパラメーターは不要です。設定パラメーターは、 `setContainerId()`、 `setParam()`および`setAsset()`の各APIメソッドを別々のJavaScript呼び出しで使用して指定します。

次の例は、固定サイズ埋め込みをセッターベースのAPIで使用する方法を示しています。

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
