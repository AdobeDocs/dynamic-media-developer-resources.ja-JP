---
title: パノラマビューア
description: HTML5 パノラマビューアは、パノラマ画像を表示する画像ビューアです。 このビューアの目的は、エクイレクタングラー画像とも呼ばれる球パノラマを表示することです。 ジャイロスコープによる自動パンニングとパンニングをサポートします。  デスクトップおよびモバイルデバイスで動作するように設計されています。  サポートするモバイルデバイスでは、バーチャルリアリティ表示モードが利用可能です。
keywords: レスポンシブ
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: null
source-git-commit: 959089682d432a72b1860f2180daac7de0afedf2
workflow-type: tm+mt
source-wordcount: '1961'
ht-degree: 0%

---

# パノラマ{#panoramic}

HTML5 パノラマビューアは、パノラマ画像を表示する画像ビューアです。 このビューアの目的は、エクイレクタングラー画像とも呼ばれる球パノラマを表示することです。 ジャイロスコープによる自動パンニングとパンニングをサポートします。  デスクトップおよびモバイルデバイスで動作するように設計されています。  サポートするモバイルデバイスでは、バーチャルリアリティ表示モードが利用可能です。

詳しくは、 [必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


ビューアタイプ 514

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## パノラマビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

HTML5 パノラマビューアは、メインの JavaScript ファイルと、ヘルパーファイルのセット ( この特定のビューア、アセット、CSS で使用されるすべてのHTML5 Viewer SDK コンポーネントを含む 1 つの JavaScript インクルード ) です。
HTML5 パノラマビューアは、IS-Viewers に付属する実稼動用HTMLページを使用するポップアップモードと、API を使用して target Web ページに統合される埋め込みモードの両方で使用できます。
設定とスキニングは、他のHTML5 ビューアと同様です。 スキニングはすべて、カスタム CSS を使用して適用できます。

詳しくは、 [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## HTML5 パノラマビューアの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5 パノラマビューアは、ドラッグまたはジャイロスコープ移動による自動パンおよびナビゲーションをサポートしています。

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
   <td colname="col2"> <p>自動パンとドラッグで移動 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>タッチデバイス </p> </td> 
   <td colname="col2"> <p>デフォルトでは、自動パンとドラッグで移動します。 VR レンダリングモード (vrrender=true) でジャイロスコープ移動によって移動します。
 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビューアは、タッチスクリーンとマウスを備えた Windows デバイスで、タッチ入力とマウス入力の両方をサポートしています。ただし、このサポートは、Chrome、Internet Explorer 11 および Edge Web ブラウザーに限られます。
パノラマビューアは、vrrender 修飾子を指定することで、Virtual Reality(VR) モードでパノラマ画像をレンダリングする機能を備えています。  Vrrender が有効な場合、分割画面にパノラマ画像が表示されます。  一般的な使用例としては、仮想現実ヘッドセットに取り付けられた携帯電話で画像を提供し、各目に別々の画像を提供する場合が考えられます。  ビューアはヘッドのジャイロスコープの動きに応答し、画像内を移動します。

## HTML5 パノラマビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Web ページごとに異なります。 Web ページにリンクが表示され、そのリンクをクリックすると、別のブラウザーウィンドウでビューアが開く場合があります。 ホスティングページにビューアを埋め込む必要が生じる場合もあります。 後者の場合は、Web ページが静的レイアウトである場合や、「レスポンシブ」で、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わる場合があります。 これらのニーズに対応するために、ビューアでは次の 3 つの主要な操作モードがサポートされています。ポップアップ、固定サイズ埋め込みおよびレスポンシブ埋め込み。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別の Web ブラウザーウィンドウまたはタブで開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやデバイスの向きが変更された場合は調整されます。

このモードは、モバイルデバイスで最も一般的なモードです。 Web ページでは、window.open() JavaScript 呼び出し、適切に設定された AHTML要素またはその他の適切な方法を使用してビューアを読み込みます。

ポップアップ操作モードには、標準のHTMLページを使用することをお勧めします。 これは、と呼ばれます。 [!DNL PanoramicViewer.html] そしてそれは以下の場所にある [!DNL html5/] 標準の IS-Viewers デプロイメントのサブフォルダー

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

カスタム CSS を適用すると、視覚的なカスタマイズを実現できます。

次に、ビューアを新しいウィンドウで開くHTMLコードの例を示します。

```
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブ埋め込みモードについて**

埋め込みモードでは、ビューアは既存の Web ページに追加されます。ビューアに関連しない顧客コンテンツが既に存在する場合があります。 ビューアは、通常、Web ページの一部の領域のみを占有します。

主な使用例は、デスクトップやタブレットデバイス向けの Web ページと、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブ Web ページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 これは、静的レイアウトの Web ページに最適です。

レスポンシブ埋め込みは、コンテナ DIV のサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定しています。 最も一般的な使用例は、柔軟なレイアウトを使用する Web ページにビューアを追加する場合です。

レスポンシブモードでは、Web ページによるコンテナ DIV のサイズ変更の方法に応じて、ビューアの動作が異なります。 Web ページでコンテナ DIV の幅のみが設定され、高さは無制限のままの場合、ビューアでは、使用中のアセットの縦横比に応じて高さが自動的に選択されます。これにより、両側のパディングなしで、アセットが表示に完全に収まります。 この使用例は、Bootstrap、Foundation などのレスポンシブレイアウトフレームワークを使用する Web ページで最も一般的です。

それ以外の場合、Web ページでビューアのコンテナ DIV の幅と高さの両方が設定されている場合、ビューアはその領域を埋め、Web ページレイアウトで指定されるサイズに従います。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイが Web ブラウザーのウィンドウサイズに従ってサイズ変更される場合があります。


**固定サイズ埋め込み**

ビューアを Web ページに追加するには、次の手順を実行します。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナの定義 `DIV`.
1. ビューアのサイズを設定します。
1. ビューアを作成および初期化する。

1. ビューアの JavaScript ファイルを Web ページに追加する。

   ビューアを作成するには、HTMLhead にスクリプトタグを追加する必要があります。 ビューア API を使用する前に、 [!DNL PanoramicViewer.js]. この [!DNL PanoramicViewer.js] ファイルは [!DNL html5/js/] 標準の IS-Viewers デプロイメントのサブフォルダー

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

ビューアがいずれかのAdobe Dynamic Media Classicサーバーにデプロイされ、同じドメインから提供されている場合は、相対パスを使用できます。 それ以外の場合は、IS-Viewers がインストールされているAdobe Dynamic Media Classicのいずれかのサーバーへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>メインビューアの JavaScript のみを参照します。 `include` ファイルをページに貼り付けます。 実行時にビューアのロジックによってダウンロードされる可能性のある、Web ページコード内の追加の JavaScript ファイルは参照しないでください。 特に、HTML5 SDK を直接参照しないでください `Utils.js` からビューアによって読み込まれたライブラリ `/s7viewers` コンテキストパス（いわゆる統合 SDK） `include`) をクリックします。 理由は、 `Utils.js` または同様のランタイムビューアライブラリは、ビューアのロジックによって完全に管理され、ビューアのリリースによって位置が変わります。 Adobeは古いバージョンのセカンダリビューアを保持しません `includes` をサーバー上に置きます。
>
>
>その結果、セカンダリ JavaScript への直接参照を配置する `include` ページ上でビューアが使用すると、新しい製品バージョンがデプロイされると、将来ビューア機能が機能しなくなります。

1. コンテナ DIV を定義する。

   ビューアを表示するページに空の DIV 要素を追加します。 DIV 要素の ID は、後でビューア API に渡されるので、定義する必要があります。 DIV のサイズは CSS で指定されます。

   プレースホルダ DIV は配置された要素です。つまり、 `position` CSS プロパティがに設定されている `relative` または `absolute`.


   次に、定義済みのプレースホルダ DIV 要素の例を示します。

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. ビューアサイズの設定

   ビューアの静的サイズを設定するには、次のように宣言します `.s7panoramicviewer` トップレベルの CSS クラス（絶対単位）、または修飾子を使用 `stagesize`.

   CSS のサイズ変更は、HTMLページまたはカスタムビューアの CSS ファイルに適用できます。この CSS ファイルは、後で AOD のビューアプリセットレコードに割り当てられるか、style コマンドを使用して明示的に渡されます。 CSS を使用したビューアのスタイル設定について詳しくは、ビューアのカスタマイズの節を参照してください。 以下に、HTMLページで静的ビューアサイズを定義する例を示します。

   ```
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` 修飾子は、次のように、 params コレクションを含むビューア初期化コード、またはコマンドリファレンスの節で説明されている API 呼び出しを使用して、明示的に渡すことができます。

   ```
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   CSS ベースのアプローチを推奨します。この例では、を使用します。


1. ビューアを作成および初期化する。

   上記の手順を完了したら、のインスタンスを作成します。 `s7viewers.PanoramicViewer` クラス、すべての設定情報をコンストラクタに渡し、を呼び出します。 `init(`) メソッドを使用して、ビューアインスタンス上に配置できます。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには containerId フィールドが存在し、ビューアの container ID の名前と、ビューアでサポートされている設定パラメーターを含むネストされた params JSON オブジェクトが含まれている必要があります。 この場合、 params オブジェクトには、少なくとも次のように画像サービング URL が渡されている必要があります。 `serverUrl` プロパティおよび初期アセットをアセットパラメーターとして追加します。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成し、起動できます。

   ビューアのコンテナを DOM に追加して、ビューアのコードが ID でコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Web ページの終わりまで DOM の構築が遅れます。 互換性を最大限に高めるには、 `init()` 終了直前の方法 `BODY` タグ、または本文 `onload()` イベント。

   同時に、コンテナ要素は必ずしも Web ページレイアウトに含まれているとは限りません。 例えば、 `display:none` スタイルが割り当てられています。 この場合、Web ページでコンテナ要素がレイアウトに戻るまで、ビューアは初期化プロセスを遅延します。 この操作を行うと、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、 `init()` メソッド。 この例では、次の点を前提としています。 `panoramicViewer` はビューアインスタンスです。 `s7viewer` はプレースホルダーの名前です `DIV`, [!DNL http://s7d1.scene7.com/is/image/] は画像サービングの URL で、 [!DNL Scene7SharedAssets/PanoramicImage-Sample] はアセットです。

   ```
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

   次のコードは、固定サイズのパノラマビューアを埋め込んだ簡単な Web ページの例です。

   ```
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

**高さ無制限のレスポンシブデザイン埋め込み**

レスポンシブ埋め込みでは、Web ページには通常、ビューアのコンテナ DIV の実行時のサイズを指示する柔軟なレイアウトが指定されています。 この例では、Web ページで、ビューアのコンテナ DIV が Web ブラウザーのウィンドウサイズの 80%を占めることを許可し、高さは無制限のままにしておくとします。 Web ページのHTMLコードは次のようになります。

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

このようなページへのビューアの追加方法は、固定サイズ埋め込みの場合とよく似ていますが、ビューアのサイズを明示的に定義する必要がない点が異なります。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナ DIV を定義する。
1. ビューアを作成および初期化する。

上記の手順はすべて、固定サイズ埋め込みの場合と同じです。 コンテナ DIV を既存の&quot;holder&quot; DIV に追加する必要があります。 次のコードは完全な例で、ブラウザーのサイズ変更時にビューアのサイズがどのように変化するか、およびビューアの縦横比がアセットとどのように一致するかを示します。

```
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

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実際に使用される例を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[代替のデモの場所](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**幅と高さが定義されたレスポンシブデザイン埋め込み**

幅と高さが定義されたレスポンシブデザイン埋め込みがある場合、Web ページのスタイル設定は異なります。&quot;holder&quot;に両方のサイズを提供します `DIV` ブラウザーウィンドウの中央に配置します。 また、Web ページでは `HTML` および `BODY` 要素を 100%に変更：

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

残りの埋め込み手順は、高さ無制限のレスポンシブ埋め込みと同じです。 結果の例は次のようになります。

```
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

**セッターベースの API を使用した埋め込み**

JSON ベースの初期化を使用する代わりに、セッターベースの API と no-args コンストラクターを使用できます。 この API では、コンストラクターはパラメーターを受け取らず、設定パラメーターは `setContainerId()`, `setParam()`、および `setAsset()` API メソッドを個別の JavaScript 呼び出しで使用できます。

次の例は、セッターベースの API を使用した固定サイズ埋め込みを示しています。

```
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
