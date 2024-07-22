---
title: パノラマビューア
description: HTML 5 パノラマビューアは、パノラマ画像を表示する画像ビューアです。 このビューアの目的は、正距円筒図法とも呼ばれる球状のパノラマを表示することです。 ジャイロスコープ動作による自動パンニング、パンに対応しています。 デスクトップおよびモバイルデバイスで動作するように設計されています。 対応するモバイルデバイスでは、バーチャルリアリティ表示モードを使用できます。
keywords: 応答
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1924'
ht-degree: 0%

---

# パノラマ{#panoramic}

HTML 5 パノラマビューアは、パノラマ画像を表示する画像ビューアです。 このビューアの目的は、正距円筒図法とも呼ばれる球状のパノラマを表示することです。 ジャイロスコープ動作による自動パンニング、パンに対応しています。 デスクトップおよびモバイルデバイスで動作するように設計されています。 対応するモバイルデバイスでは、バーチャルリアリティ表示モードを使用できます。

[ システム要件と前提条件 ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842) を参照してください。


ビューアのタイプ 514。

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## パノラマビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

HTML5 パノラマビューアは、実行時にビューアがダウンロードするメインのJavaScript ファイルとヘルパーファイルのセットを表します。 ヘルパーファイルのセットは、1 つのJavaScript インクルードで、この特定のビューア、Assets、CSS で使用されるすべてのHTML5 Viewer SDK コンポーネントに含まれます。
HTML5 パノラマビューアは、IS-Viewers に付属の実稼動用HTMLーページを使用したポップアップモードと、ドキュメント化された API を使用して Target Web ページに統合する埋め込みモードの両方で使用できます。
設定とスキニングは、他のHTML5 ビューアと同様です。 すべてのスキニングは、カスタム CSS を使用して行うことができます。

[ すべてのビューアに共通のコマンドリファレンス – 設定属性 ](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [ すべてのビューアに共通のコマンドリファレンス - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) を参照してください

## HTML5 パノラマビューアの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5 パノラマビューアは、ドラッグまたはジャイロスコープ動作による自動パンニングおよびナビゲーションをサポートしています。

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
   <td colname="col2"> <p>自動パンおよびドラッグして移動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>タッチデバイス </p> </td> 
   <td colname="col2"> <p>デフォルトでは、自動パンとドラッグで移動します。 VR レンダリングモード（vrrender=true）でジャイロスコープ動作で移動します。
 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビューアは、タッチスクリーンとマウスを使用した Windows デバイスでは、タッチ入力とマウス入力の両方をサポートしていますが、このサポートは、Chrome、Internet Explorer 11、Edgeの web ブラウザーのみに制限されています。
パノラマビューアは、vrrender 修飾子を指定して、バーチャルリアリティ（VR）モードでパノラマ画像をレンダリングできます。 vrrender を有効にすると、分割画面にパノラマ画像が表示されます。 一般的なユースケースは、バーチャルリアリティヘッドセットにマウントされた携帯電話で画像を提供し、目ごとに別々の画像を提供することです。 ビューアは、ヘッドのジャイロスコープ動作に応答し、画像内を移動します。

## HTML5 パノラマビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

Web ページによって、ビューアの動作に対するニーズは異なります。 Web ページにリンクが表示される場合があります。 そのリンクを選択すると、ビューアが別のブラウザーウィンドウで開きます。 場合によっては、ホスティングページにビューアを埋め込む必要があります。 後者の場合、web ページが静的なレイアウトになっている可能性や、「レスポンシブ」でデバイスやブラウザーウィンドウのサイズによって表示が異なる可能性があります。 これらのニーズに対応するために、ビューアでは、ポップアップ、固定サイズ埋め込み、レスポンシブ埋め込みの 3 つの主要な操作モードをサポートしています。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別の web ブラウザーウィンドウまたはタブで開きます。 ブラウザーのウィンドウ領域全体を使用し、ブラウザーのサイズが変更された場合や、デバイスの向きが変更された場合に合わせて調整されます。

このモードは、モバイルデバイスで最も一般的です。 Web ページは、JavaScript呼び出し、HTML要素 `window.open()` 適切に設定された方法、またはその他の適切な方法を使用して、ビューアを読み込みます。

ポップアップ操作モードには、標準のHTMLページを使用することをお勧めします。 このフォルダーは [!DNL PanoramicViewer.html] と呼ばれ、標準の IS-Viewers デプロイメントの [!DNL html5/] サブフォルダーに配置されています。

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

視覚的なカスタマイズは、カスタム CSS を適用することで実現できます。

次に、新しいウィンドウでビューアを開くHTMLコードの例を示します。

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブ埋め込みモードについて**

埋め込みモードでは、ビューアが既存の web ページに追加されます。これには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 閲覧者は通常、Web ページの不動産の一部のみを占有します。

主なユースケースは、デスクトップまたはタブレットデバイス向けの web ページと、デバイスタイプに応じて自動的にレイアウトを調整するレスポンシブ web ページです。

固定サイズの埋め込みは、初回読み込み後にビューアがサイズを変更しない場合に使用されます。 この方法は、静的なレイアウトを持つ web ページに最適です。

レスポンシブ埋め込みは、コンテナ DIV のサイズ変更に応じて、実行時にビューアのサイズを変更する必要があることを前提としています。 最も一般的なユースケースは、柔軟なレイアウトを使用する web ページへのビューアの追加です。

レスポンシブモードでは、ビューアの動作は、web ページでのコンテナ DIV のサイズ設定によって異なります。 Web ページでコンテナ DIV の幅のみが設定され、高さが制限されない場合、ビューアは、使用されるアセットの縦横比に応じて自動的に高さを選択します。 この方法では、アセットが側面にパディングを入れずに、ビューに完全に収まります。 このユースケースは、Bootstrapや基盤などのレスポンシブレイアウトフレームワークを使用する web ページで最も一般的です。

Web ページでビューアのコンテナ DIV の幅と高さの両方が設定されている場合は、ビューアはその領域を埋め、web ページレイアウトで提供されるサイズに従います。 良い例は、ビューアをモーダルオーバーレイに埋め込む場合です。この場合、オーバーレイは web ブラウザーのウィンドウサイズに応じてサイズが調整されます。

**固定サイズ埋め込み**

Web ページにビューアを追加するには、次の手順を実行します。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ `DIV` を定義します。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. Web ページへのビューアJavaScript ファイルの追加

   ビューアを作成するには、HTMLの先頭にスクリプトタグを付ける必要があります。 ビューア API を使用する前に、必ず [!DNL PanoramicViewer.js] を含めてください。 [!DNL PanoramicViewer.js] ファイルは、標準の IS-Viewers デプロイメントの [!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

ビューアがAdobe Dynamic Media Classic サーバーの 1 つにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-Viewers がインストールされているAdobe Dynamic Media Classic サーバーの 1 つへのフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScript `include` ファイルのみを参照します。 実行時にビューアのロジックによってダウンロードされる可能性がある web ページコード内の追加のJavaScript ファイルを参照しないでください。 特に、ビューアによって読み込まれるHTML5 SDK `Utils.js` ライブラリをコンテキストパス（いわゆる統合 SDK `include`）から直接参照 `/s7viewers` ないでください。 これは、`Utils.js` や類似のランタイム・ビューア・ライブラリの場所はビューアのロジックによって完全に管理され、ビューア・リリース間で場所が変更されるためです。 Adobeは、古いバージョンのセカンダリ・ビューア `includes` をサーバ上に保持しません。
>
>
>その結果、ビューアが使用するセカンダリ JavaScript `include` ージをページ上で直接参照すると、今後、新しい製品バージョンがデプロイされた際に、ビューアの機能が損なわれます。

1. コンテナ DIV の定義。

   ビューアを表示するページに、空の DIV 要素を追加します。 DIV 要素には ID が定義されている必要があります。これは、この ID が後でビューア API に渡されるためです。 DIV のサイズは CSS で指定します。

   プレースホルダー DIV が配置済み要素です（つまり、`position` CSS プロパティが `relative` または `absolute` に設定されています）。


   定義されたプレースホルダー DIV 要素の例を以下に示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. ビューアサイズの設定

   ビューアの静的サイズは、最上位の CSS クラスに対して絶対単位で宣言す `.s7panoramicviewer` か、修飾子 `stagesize` を使用して設定できます。

   CSS のサイズ設定はHTMLページかカスタムビューア CSS ファイルに直接配置できます。この CSS ファイルは、後で AOD のビューアプリセットレコードに割り当てられたり、style コマンドを使用して明示的に渡されたりします。 CSS を使用したビューアのスタイル設定について詳しくは、ビューアのカスタマイズの節を参照してください。 HTMLページで静的ビューアサイズを定義する例を以下に示します。

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   修飾子 `stagesize`、params コレクションを使用したビューア初期化コードによって明示的に渡すことも、次のように「コマンドリファレンス」節で説明されているように API 呼び出しとして渡すこともできます。

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   この例では、CSS ベースのアプローチをお勧めします。これを使用します。

1. ビューアの作成と初期化。

   上記の手順を完了したら、クラスのインスタンスを作成し、`s7viewers.PanoramicViewer` のコンストラクターにすべての設定情報を渡して、ビューアインスタンスの `init(`） メソッドを呼び出します。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには containerId フィールドが必要です。このフィールドには、ビューアコンテナ ID の名前と、ビューアでサポートされている設定パラメーターを含んだネストされたパラメーターの JSON オブジェクトが格納されます。 この場合、params オブジェクトには、少なくとも画像サービング URL がプロパティとして渡され、初期アセット `serverUrl` アセットパラメーターとして渡されている必要があります。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成して開始できます。

   ビューアコードが ID でコンテナ要素を見つけられるように、ビューアコンテナを DOM に追加することが重要です。 一部のブラウザーでは、web ページの最後まで DOM の構築が遅れます。 互換性を最大限に高めるには、終了 `BODY` タグの直前または body `onload()` イベントで `init()` メソッドを呼び出します。

   同時に、コンテナ要素は、まだ web ページレイアウトの一部である必要はありません。 例えば、割り当てられたスタイルを使用して非表示 `display:none` する場合があります。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで、初期化プロセスを遅延します。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

   次に、ビューアインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡して、`init()` メソッドを呼び出す例を示します。 この例では、`panoramicViewer` がビューアインスタンス、`s7viewer` がプレースホルダー `DIV` の名前、[!DNL http://s7d1.scene7.com/is/image/] が画像サービング URL、[!DNL Scene7SharedAssets/PanoramicImage-Sample] がアセットであることを前提としています。

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

   次のコードは、パノラマビューアを固定サイズで埋め込んだ単純な web ページの完全な例です。

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

**高さが制限されないレスポンシブデザインの埋め込み**

レスポンシブ埋め込みを使用すると、通常、web ページには、ビューアのコンテナ DIV の実行時サイズを指示する何らかの柔軟なレイアウトが用意されます。 この例の目的上、web ページで、ビューアのコンテナ DIV が web ブラウザーのウィンドウサイズの 80% を占め、高さは無制限のままであるとします。 Web ページHTMLコードは次のようになります。

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

ビューアをこのようなページに追加する方法は、固定サイズの埋め込みに似ています。唯一の違いは、ビューアサイズを明示的に定義する必要がない点です。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ DIV の定義。
1. ビューアの作成と初期化。

上記の手順はすべて、固定サイズの埋め込みと同じです。 コンテナ DIV を既存の「ホルダー」 DIV に追加する必要があります。 次のコードは完全な例です。ブラウザーのサイズを変更するとビューアのサイズがどのように変化するか、ビューアの縦横比がアセットにどのように一致するかを確認できます。

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

次のページの例では、高さが制限されないレスポンシブデザインの埋め込みを使用した実際の使用例を示しています。

[ ライブデモ ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[ 代替デモの場所 ](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**幅と高さが定義されたレスポンシブデザインの埋め込み**

幅と高さが定義されたレスポンシブデザインの埋め込みがある場合、web ページのスタイルは異なります。これは、「ホルダー」 `DIV` ージのサイズと、ブラウザーウィンドウの中央にあるサイズの両方を提供します。 また、Web ページでは、`HTML` 要素と `BODY` 要素のサイズが 100% に設定されます。

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

残りの埋め込み手順は、高さが制限されないレスポンシブ埋め込みと同じです。 次に例を示します。

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

**Setter ベースの API を使用した埋め込み**

JSON ベースの初期化を使用する代わりに、setter ベースの API および no-args コンストラクターを使用することができます。 この API を使用する場合、コンストラクターはパラメーターを取らず、`setContainerId()`、`setParam()`、`setAsset()` の API メソッドを使用して、個別のJavaScript呼び出しで設定パラメーターを指定します。

次の例は、setter ベースの API を使用した固定サイズの埋め込みを示しています。

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
