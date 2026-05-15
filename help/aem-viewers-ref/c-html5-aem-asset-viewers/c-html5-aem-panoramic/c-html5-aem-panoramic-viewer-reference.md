---
title: パノラマビューアー
description: HTML5 Panoramic Viewerは、パノラマ画像を表示する画像ビューアです。 このビューアの目的は、等長方形画像とも呼ばれる球状のパノラマを表示することです。 ジャイロスコープの移動による自動パンニングとパンニングをサポートします。 デスクトップやモバイルデバイスで動作するように設計されています。 バーチャルリアリティ表示モードは、対応するモバイルデバイスで利用できます。
keywords: responsive
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
autotag-review: '2026-05-13T22:16:12.254Z'
TQID: 'https://experienceleague.adobe.com/lqrLpEdrL5vfhuF9GPmw-Yp1-FZmoEC-H-NlG0Z-i2Q'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 1950
ht-degree: 0%

---

# パノラマ{#panoramic}

HTML5 Panoramic Viewerは、パノラマ画像を表示する画像ビューアです。 このビューアの目的は、等長方形画像とも呼ばれる球状のパノラマを表示することです。 ジャイロスコープの移動による自動パンニングとパンニングをサポートします。 デスクトップやモバイルデバイスで動作するように設計されています。 バーチャルリアリティ表示モードは、対応するモバイルデバイスで利用できます。

[必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。


ビューアータイプ 514。

<!--
## Demo URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)
-->

## パノラマビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

HTML5 Panoramic Viewerは、メインのJavaScript ファイルと、実行時にビューアによってダウンロードされる一連のヘルパーファイルを表します。 ヘルパーファイルのセットは、この特定のビューア、アセット、CSSで使用されるすべてのHTML5 Viewer SDK コンポーネントを含む1つのJavaScriptです。
HTML5 Panoramic Viewerは、IS-Viewersを備えた実稼動対応のHTML ページを使用してポップアップモードで使用するか、ドキュメント化されたAPIを使用してターゲット web ページに統合する組み込みモードで使用できます。
設定とスキニングは、他のHTML 5 ビューアと同様です。 すべてのスキニングは、カスタム CSSを使用して実行できます。

すべてのビューアに共通する[&#x200B; コマンド参照 – 構成属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通するコマンド参照 – URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください

## HTML5 Panoramic Viewerの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5 Panoramic Viewerは、ドラッグまたはジャイロスコープによる自動パンニングとナビゲーションをサポートしています。

<table id="table_panoramic"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ナビゲーション </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>デスクトップ </p> </td> 
   <td colname="col2"> <p>オートパンとドラッグで移動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>タッチデバイス </p> </td> 
   <td colname="col2"> <p>自動パンとドラッグを使用すると、デフォルトで移動します。 VR レンダリングモードでジャイロスコープ移動で移動する（vrrender=true）。
 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビューアは、タッチスクリーンとマウスを備えたWindows デバイスでタッチ入力とマウス入力の両方をサポートしていますが、このサポートはChrome、Internet Explorer 11、Edge web ブラウザーのみに限定されています。
Panoramic Viewerは、vrrender修飾子を指定することで、パノラマ画像をVR （仮想現実）モードでレンダリングできます。 vrrenderを有効にすると、分割画面にパノラマ画像が表示されます。 一般的なユースケースとしては、バーチャルリアリティヘッドセットに搭載された携帯電話で画像を配信し、各目に個別の画像を提供することです。 ビューアは、頭のジャイロスコープの動きに応答し、画像をナビゲートします。

## HTML5 パノラマビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

web ページごとに、閲覧者の行動に対するニーズは異なります。 web ページにリンクが表示されることがあります。 このリンクを選択すると、別のブラウザーウィンドウでビューアが開きます。 それ以外の場合、ビューアをホスティングページに埋め込む必要がある場合があります。 後者の場合、web ページは静的なレイアウトを持っているか、「レスポンシブ」であり、異なるデバイスまたは異なるブラウザーウィンドウのサイズに対して異なる表示を行うことができます。 これらのニーズに対応するために、ビューアでは、ポップアップ、固定サイズの埋め込み、レスポンシブ埋め込みの3つの主要な操作モードをサポートしています。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別のweb ブラウザーウィンドウまたはタブで開きます。 ブラウザーのウィンドウ領域全体を使用し、ブラウザーのサイズ変更やデバイスの向きの変更に応じて調整します。

このモードは、モバイルデバイスで最も一般的です。 Web ページは、`window.open()` JavaScript呼び出し、適切に設定されたHTML要素、またはその他の適切な方法を使用してビューアを読み込みます。

ポップアップ操作モードには、標準のHTML ページを使用することをお勧めします。 [!DNL PanoramicViewer.html]と呼ばれ、標準のIS-Viewers デプロイメントの[!DNL html5/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

カスタム CSSを適用することで、視覚的なカスタマイズを実現できます。

新しいウィンドウでビューアを開くHTML コードの例を次に示します。

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブ埋め込みモードについて**

埋め込みモードでは、ビューアは既存のweb ページに追加されます。このページには、ビューアに関連しない顧客コンテンツが既に含まれている可能性があります。 通常、閲覧者はweb ページの不動産の一部しか占めていません。

主なユースケースは、デスクトップ PCやタブレットデバイス向けのweb ページです。デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブ web ページも使用できます。

初期読み込み後にビューアのサイズが変更されない場合は、固定サイズ埋め込みが使用されます。 この方法は、静的レイアウトを持つweb ページに最適です。

レスポンシブ埋め込みは、コンテナ DIVのサイズ変更に応じて、実行時にビューアのサイズを変更する必要があることを前提としています。 最も一般的なユースケースは、柔軟性の高いレイアウトを使用するweb ページにビューアを追加することです。

レスポンシブモードでは、web ページのサイズとコンテナ DIVによってビューアの動作が異なります。 web ページでコンテナ DIVの幅のみを設定し、高さを制限しない場合、ビューアは使用するアセットの縦横比に応じて自動的に高さを選択します。 この方法により、側面にパディングすることなく、アセットがビューに完全に収まります。 このユースケースは、BootstrapやFoundationなどのレスポンシブレイアウトフレームワークを使用するweb ページで最も一般的です。

それ以外の場合、web ページでビューアのコンテナ DIVの幅と高さの両方を設定すると、ビューアはその領域を塗りつぶし、web ページレイアウトで提供されるサイズに従います。 良い例は、ビューアをモーダルオーバーレイに埋め込むことです。このオーバーレイは、web ブラウザーのウィンドウサイズに応じてサイズが調整されます。

**固定サイズ埋め込み**

次の操作を実行して、ビューアをweb ページに追加します。

1. ビューアのJavaScript ファイルをweb ページに追加します。
1. コンテナ `DIV`を定義しています。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. ビューアのJavaScript ファイルをweb ページに追加します。

   ビューアを作成するには、HTML ヘッドにスクリプトタグを追加する必要があります。 ビューアーAPIを使用する前に、[!DNL PanoramicViewer.js]を含めることを確認してください。 [!DNL PanoramicViewer.js] ファイルは、標準のIS-Viewers デプロイメントの[!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

ビューアがAdobe Dynamic Media Classic サーバーのいずれかにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-ViewersがインストールされているAdobe Dynamic Media Classic サーバーの1つにフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメイン ビューア JavaScript `include` ファイルのみを参照してください。 実行時にビューアのロジックによってダウンロードされる可能性があるweb ページコード内の他のJavaScript ファイルを参照しないでください。 特に、`/s7viewers` コンテキストパス（いわゆる統合SDK `include`）からビューアによって読み込まれたHTML5 SDK `Utils.js` ライブラリを直接参照しないでください。 その理由は、`Utils.js`または類似のランタイムビューアーライブラリの場所が、ビューアーのロジックによって完全に管理され、ビューアーリリース間で場所が変更されるためです。 Adobeは、古いバージョンのセカンダリビューア `includes`をサーバー上に保持しません。
>
>
>その結果、ビューアがページ上で使用するセカンダリ JavaScript `include`を直接参照すると、新しい製品バージョンがデプロイされる際に、将来的にビューア機能が破損します。

1. コンテナ DIVの定義。

   ビューアを表示するページに、空のDIV エレメントを追加します。 このIDは後でビューア APIに渡されるので、DIV要素にはIDが定義されている必要があります。 DIVのサイズはCSSで指定します。

   プレースホルダーDIVは配置された要素です。`position` CSS プロパティが`relative`または`absolute`に設定されていることを意味します。


   次に、定義済みのプレースホルダーDIV要素の例を示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. ビューアサイズの設定

   ビューアの静的サイズは、`.s7panoramicviewer` トップレベル CSS クラスを絶対単位で宣言するか、修飾子`stagesize`を使用することで設定できます。

   CSSでのサイズ変更は、HTML ページに配置するか、カスタムビューア CSS ファイルに配置して、後でAODのビューアプリセットレコードに割り当てるか、スタイルコマンドを使用して明示的に渡すことができます。 CSSを使用したビューアのスタイル設定について詳しくは、ビューアのカスタマイズ セクションを参照してください。 HTML ページでの静的ビューアサイズの定義例を次に示します。

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize`修飾子は、params コレクションを使用してビューア初期化コードを使用するか、コマンドリファレンスの節で説明されているように、API呼び出しとして明示的に渡すことができます。

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   CSS ベースのアプローチが推奨され、この例で使用されます。

1. ビューアの作成と初期化。

   上記の手順を完了したら、`s7viewers.PanoramicViewer` クラスのインスタンスを作成し、すべての構成情報をそのコンストラクターに渡し、ビューアーインスタンスで`init(`） メソッドを呼び出します。 構成情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアコンテナ IDの名前を保持するcontainerId フィールドと、ビューアでサポートされる設定パラメーターを含むネストされたパラメーターJSON オブジェクトが必要です。 この場合、params オブジェクトには、少なくとも画像サービング URLが`serverUrl` プロパティとして渡され、最初のアセットがアセットパラメーターとして渡されている必要があります。 JSON ベースの初期化APIを使用すると、1行のコードでビューアを作成および開始できます。

   ビューアコードがIDでコンテナ要素を見つけられるように、ビューアコンテナをDOMに追加することが重要です。 一部のブラウザーは、Web ページの最後までDOMの構築を遅らせます。 互換性を最大限に高めるには、終了`BODY` タグの直前または本文`onload()` イベントで`init()` メソッドを呼び出します。

   同時に、コンテナ要素は必ずしもweb ページレイアウトの一部であってはなりません。 例えば、割り当てられた`display:none` スタイルを使用して非表示にすることができます。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで初期化プロセスを遅らせます。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

   次に、ビューアーインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡し、`init()` メソッドを呼び出す例を示します。 この例では、`panoramicViewer`がビューアインスタンスで、`s7viewer`がプレースホルダー`DIV`の名前、[!DNL http://s7d1.scene7.com/is/image/]が画像サービング URLで、[!DNL Scene7SharedAssets/PanoramicImage-Sample]がアセットであると仮定します。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var panoramicViewer = new s7viewers.PanoramicViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
     "asset":"Scene7SharedAssets/PanoramicImage-Sample",
     "serverurl":"http://s7d1.scene7.com/is/image/"
   } 
   }).init(); 
   </script> 
   ```

   次のコードは、パノラマビューアを固定サイズで埋め込む面倒なweb ページの完全な例です。

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
    <head>
    <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
    <style type="text/css">
    #s7viewer.s7panoramicviewer {
        width: 1024px;
        height: 512px;
    }
    </style>
    </head>
    <body>
    <div id="s7viewer" style="position:relative"></div>
    <script type="text/javascript">
    var panoramicViewer = new s7viewers.PanoramicViewer({
        "containerId":"s7viewer",
    "params":{
        "asset":"Scene7SharedAssets/PanoramicImage-Sample",
        "serverurl":"http://s7d1.scene7.com/is/image/"
    }
    }).init();
    </script>
    </body>
    </html>
   ```

**高さの制限のないレスポンシブデザイン埋め込み**

レスポンシブ埋め込みの場合、web ページには通常、ビューアのコンテナ DIVの実行時サイズを決定する、ある種の柔軟なレイアウトが配置されます。 この例では、web ページでビューアのコンテナ DIVがweb ブラウザーのウィンドウサイズの80%を使用でき、高さは制限されないと仮定します。 web ページのHTML コードは次のようになります。

```html {.line-numbers}
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

このようなページへのビューアの追加は、固定サイズの埋め込みと似ていますが、ビューアサイズを明示的に定義する必要がない唯一の違いは次のとおりです。

1. ビューアのJavaScript ファイルをweb ページに追加します。
1. コンテナ DIVの定義。
1. ビューアの作成と初期化。

上記のすべての手順は、固定サイズの埋め込みと同じです。 コンテナ DIVを既存の「ホルダ」 DIVに追加する必要があります。 次のコードは完全な例です。ブラウザーのサイズを変更するとビューアサイズがどのように変化するか、ビューアの縦横比がアセットとどのように一致するかを確認できます。

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

次のサンプルページでは、高さの制限のないレスポンシブデザイン埋め込みをより実際に使用する方法を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--

[Alternate demo location](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=ja)

-->

**幅と高さが定義されたレスポンシブデザイン埋め込み**

幅と高さが定義されたレスポンシブデザインの埋め込みがある場合、web ページのスタイルは異なります。「ホルダー」 `DIV`に両方のサイズを提供し、ブラウザーウィンドウに中央に配置します。 また、web ページでは、`HTML`要素と`BODY`要素のサイズを100%に設定しています。

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

残りの埋め込み手順は、高さの制限のないレスポンシブ埋め込みと同じです。 結果の例は次のとおりです

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

**Setter ベースのAPIを使用した埋め込み**

JSON ベースの初期化を使用する代わりに、セッターベースのAPIとno-args コンストラクターを使用できます。 このAPIでは、コンストラクターはパラメーターを受け取らず、設定パラメーターは`setContainerId()`、`setParam()`、および`setAsset()`のAPI メソッドを使用して指定され、別々のJavaScript呼び出しが行われます。

次の例は、セッターベースのAPIを使用した固定サイズの埋め込みを示しています。

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script language="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
#s7viewer.s7panoramicviewer {
    width: 1024;
    height: 512;
}
</style>
</head>
<body>
<div id="s7viewer" style="position:relative"></div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer();
panoramicViewer.setContainerId("s7viewer");
panoramicViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/");
panoramicViewer.setAsset("Scene7SharedAssets/PanoramicImage-Sample");
panoramicViewer.init();
</script>
</body>
</html>
```
