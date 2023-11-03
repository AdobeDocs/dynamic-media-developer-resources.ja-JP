---
title: Spin
description: スピンビューアは、画像の 360 度のビュー、または適切なスピンセットが使用されている場合は多次元ビューを提供する画像ビューアです。 このウィンドウには、ズームツールとスピンツール、フルスクリーンのサポートおよびオプションの閉じるボタンがあります。 デスクトップおよびモバイルデバイスで動作するように設計されています。
keywords: レスポンシブ
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4c802d42-ea5b-4f28-b6ef-2689aa16839d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2130'
ht-degree: 0%

---

# Spin{#spin}

スピンビューアは、画像の 360 度のビュー、または適切なスピンセットが使用されている場合は多次元ビューを提供する画像ビューアです。 このウィンドウには、ズームツールとスピンツール、フルスクリーンのサポートおよびオプションの閉じるボタンがあります。 デスクトップおよびモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR（画像レンダリング）または UGC（ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされません。

ビューアタイプ 503

詳しくは、 [必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400)

## スピンビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

スピンビューアは、メインの JavaScript ファイルと、ヘルパーファイルのセット（この特定のビューア、アセット、CSS で使用されるすべての Viewer SDK コンポーネントが含まれる単一の JavaScript インクルード）で、ビューアによって実行時にダウンロードされます。

スピンビューアは、IS ビューアに付属する実稼動用HTMLページを使用したポップアップモードでも、埋め込みモードでも、ドキュメント化された API を使用してターゲット Web ページに統合して使用できます。

設定とスキニングは、他のビューアと同様です。 スキニングはすべて、カスタム CSS を使用して実行できます。

詳しくは、 [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## スピンビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

スピンビューアは、他のモバイルアプリケーションで一般的な以下のタッチジェスチャに対応しています。 ビューアがユーザーのスワイプジェスチャを処理できない場合、このイベントが Web ブラウザーに転送され、ネイティブページスクロールが実行されます。 この機能を使用すると、デバイスの画面領域のほとんどをビューアが占めている場合でも、ユーザーはページ内を移動できます。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ジェスチャ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ダブルタップ </p> </td> 
   <td colname="col2"> <p> 最大の拡大率に達するまで、1 レベルズームインします。 次のダブルタップジェスチャでは、ビューアが初期の表示状態にリセットされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ピンチ </p> </td> 
   <td colname="col2"> <p>画像をズームインまたはズームアウトします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平方向のスワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態の場合、セットを水平方向にスピンします。 </p> <p> 画像がズームインされると、画像は水平方向に移動されます。 画像を表示の端まで移動しても、その方向でスワイプを実行すると、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直方向のスワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態の場合、多次元スピンセットが使用されている場合に垂直方向の表示角度が変更されます。 1 次元スピンセットでは、このジェスチャによってネイティブページスクロールが実行されます。 また、多次元のスピンセットが最後または最初の軸にある場合に、垂直方向のスワイプによって垂直方向の表示角度が変わらないように、このジェスチャではネイティブページスクロールも実行されます。 </p> <p> 画像がズームインされると、画像は垂直方向に移動されます。 画像を表示の端まで移動しても、その方向でスワイプを実行すると、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>また、タッチスクリーンとマウスを備えた Windows デバイスでは、タッチ入力とマウス入力の両方がサポートされます。 ただし、このサポートは、Chrome、Internet Explorer 11 および Edge Web ブラウザーにのみ制限されます。

このビューアは完全にキーボードでアクセス可能です。

詳しくは、 [キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## スピンビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Web ページごとに異なります。 Web ページにリンクが表示され、このリンクを選択すると、ビューアが別のブラウザーウィンドウで開かれる場合があります。 ホスティングページの右側にビューアを埋め込む必要がある場合もあります。 後者の場合は、Web ページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは、ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込みの 3 つの主要な操作モードをサポートしています。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別の Web ブラウザーウィンドウまたはタブで開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズが変更された場合や、モバイルデバイスの向きが変更された場合は調整されます。

ポップアップモードは、モバイルデバイスで最も一般的なモードです。 Web ページでは、 `window.open()` JavaScript 呼び出し（適切に設定） `A` HTML要素、またはその他の適切な方法。

ポップアップ操作モードには、標準のHTMLページを使用することをお勧めします。 この場合、 [!DNL SpinViewer.html] とは、 [!DNL html5/] 標準の IS-Viewers デプロイメントのサブフォルダー

[!DNL <s7viewers_root>/html5/SpinViewer.html]

カスタム CSS を適用することで、視覚的なカスタマイズを実現できます。

次に、ビューアを新しいウィンドウでHTMLする開封コードの例を示します。

```html {.line-numbers}
<a href="https://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存の Web ページに追加されます。ビューアに関連しない顧客コンテンツが既に存在する場合があります。 ビューアは、通常、Web ページの一部の領域のみを占有します。

主な使用例は、デスクトップやタブレットデバイス向けの Web ページと、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 このアクションは、静的レイアウトの Web ページに最適です。

レスポンシブデザイン埋め込みは、コンテナのサイズ変更に応じて実行時にビューアのサイズを変更する必要がある場合を想定しています `DIV`. 最も一般的な使用例は、柔軟なページレイアウトを使用する Web ページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Web ページによるコンテナのサイズ変更の方法によって、ビューアの動作が異なります `DIV`. Web ページでコンテナの幅のみが設定される場合 `DIV`で選択し、高さは無制限のままにし、使用するアセットの縦横比に従って、ビューアによって高さが自動的に選択されます。 この機能により、両側のパディングなしで、アセットが表示に完全に収まります。 この使用例は、Web ページや Foundation などのレスポンシブデザインレイアウトフレームワークを使用する WebBootstrapで最も一般的です。

それ以外の場合は、Web ページでビューアのコンテナの幅と高さの両方が設定されている場合 `DIV`を指定した場合、ビューアはその領域全体を占め、Web ページのレイアウトに従ってサイズが設定されます。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイが Web ブラウザーのウィンドウサイズに従ってサイズ変更される場合があります。

**固定サイズ埋め込み**

次の手順を実行して、スピンビューアを Web ページに追加します。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナの定義 `DIV`.
1. ビューアのサイズを設定します。
1. ビューアを作成および初期化する。

1. ビューアの JavaScript ファイルを Web ページに追加する。

   ビューアを作成するには、HTMLhead にスクリプトタグを追加する必要があります。 ビューア API を使用する前に、必ず `SpinViewer.js`. `SpinViewer.js` は、 [!DNL html5/js/] 標準の IS-Viewers デプロイメントのサブフォルダー

   `<s7viewers_root>/html5/js/SpinViewer.js`

   ビューアがDynamic MediaAdobeの 1 つにデプロイされ、同じドメインから提供されている場合は、相対パスを使用できます。 それ以外の場合は、IS-Viewers がインストールされているAdobeDynamic Mediaサーバーの 1 つへのフルパスを指定します。

   相対パスは次のようになります。

   ```html {.line-numbers}
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
   ```

   >[!NOTE]
   >
   >メインビューアの JavaScript のみを参照します。 `include` ファイルをページに貼り付けます。 実行時にビューアのロジックによってダウンロードされる可能性のある、Web ページコード内の追加の JavaScript ファイルは参照しないでください。 特に、HTML5 SDK を直接参照しないでください `Utils.js` からビューアによって読み込まれたライブラリ `/s7viewers` コンテキストパス（いわゆる統合 SDK） `include`) をクリックします。 理由は、 `Utils.js` または同様のランタイムビューアライブラリは、ビューアのロジックによって完全に管理され、ビューアのリリースによって位置が変わります。 Adobeは古いバージョンのセカンダリビューアを保持しません `includes` をサーバー上に置きます。
   >
   >
   >その結果、セカンダリ JavaScript への直接参照を配置する `include` ページ上でビューアが使用すると、新しい製品バージョンがデプロイされると、将来ビューア機能が機能しなくなります。

1. コンテナ DIV を定義する。

   ビューアを表示するページに空の DIV 要素を追加します。 DIV 要素の ID は、後でビューア API に渡されるので、定義する必要があります。

   プレースホルダ DIV は配置された要素です。つまり、 `position` CSS プロパティがに設定されている `relative` または `absolute`.

   次に、定義済みのプレースホルダ DIV 要素の例を示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアサイズの設定

   ビューアの静的サイズを設定するには、次のように宣言します `.s7spinviewer` トップレベルの CSS クラス ( 絶対単位で、または `stagesize` 修飾子

   サイズ調整は、HTMLページまたはカスタムビューアの CSS ファイルで直接 CSS に配置できます。 後でDynamic Media Classic内のビューアプリセットレコードに割り当てるか、スタイルコマンドを使用して明示的に渡します。

   詳しくは、 [スピンビューアのカスタマイズ](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) を参照してください。

   次に、HTMLページで静的ビューアサイズを定義する例を示します。

   ```html {.line-numbers}
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次の設定が可能です。 `stagesize` 修飾子がDynamic Media Classicのビューアプリセットレコードに含まれていること。 または、を使用して、ビューア初期化コードで明示的に渡すこともできます。 `params` コレクション、またはコマンドリファレンスの節で説明されている API 呼び出しとして、次のように使用できます。

   ```html {.line-numbers}
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   CSS ベースのアプローチを推奨します。この例では、を使用します。

1. ビューアを作成および初期化する。

   上記の手順を完了したら、のインスタンスを作成します。 `s7viewers.SpinViewer` クラス、すべての設定情報をコンストラクタに渡し、を呼び出します。 `init()` メソッドを使用して、ビューアインスタンス上に配置できます。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには `containerId` ビューアのコンテナ ID とネストされたコンテナの名前が格納されるフィールド `params` ビューアがサポートする設定パラメーターを含む JSON オブジェクト。 この場合、 `params` オブジェクトの場合は、少なくとも次のように画像サービング URL が渡されている必要があります。 `serverUrl` プロパティと初期アセット `asset` パラメーター。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成し、起動できます。

   ビューアのコンテナを DOM に追加して、ビューアのコードが ID でコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Web ページの終わりまで DOM の構築が遅れます。 互換性を最大限に高めるには、 `init()` 終了直前の方法 `BODY` タグ、または本文 `onload()` イベント。

   同時に、コンテナ要素は、必ずしも Web ページレイアウトに含まれているとは限りません。 例えば、 `display:none` スタイルが割り当てられています。 この場合、Web ページでコンテナ要素がレイアウトに戻るまで、ビューアは初期化プロセスを遅延します。 この操作を行うと、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、 `init()` メソッド。 この例では、次のように仮定します。 `spinViewer` はビューアインスタンスです。 `s7viewer` はプレースホルダーの名前です `DIV`, [!DNL http://s7d1.scene7.com/is/image/] は画像サービングの URL で、 [!DNL Scene7SharedAssets/SpinSet_Sample] はアセットです。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、固定サイズのスピンビューアを埋め込んだ簡単な Web ページの例です。

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高さ無制限のレスポンシブデザイン埋め込み**

レスポンシブデザイン埋め込みでは、Web ページには通常、ビューアのコンテナの実行時のサイズを指示する柔軟なレイアウトが指定されています `DIV`. この例では、Web ページがビューアのコンテナを許可しているとします。 `DIV` を使用すると、web ブラウザーのウィンドウサイズの 40%を占め、高さは無制限のままになります。 生成される Web ページHTMLコードは次のようになります。

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

このようなページへのビューアの追加方法は、固定サイズ埋め込みと似ていますが、唯一の違いは、ビューアのサイズを明示的に定義する必要がない点です。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナ DIV を定義する。
1. ビューアを作成および初期化する。

上記の手順はすべて、固定サイズ埋め込みの場合と同じです。 コンテナを追加 `DIV` 既存の「所有者」に対して `DIV`. 次のコードは完全な例です。 ブラウザーのサイズ変更時にビューアのサイズがどのように変化するか、およびビューアの縦横比がアセットとどのように一致するかを確認できます。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実際に使用される使用例を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[代替のデモの場所](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**幅と高さが定義されたフレキシブルサイズ埋め込み**

幅と高さが定義されたフレキシブルサイズ埋め込みがある場合、Web ページのスタイル設定は異なります。 つまり、&quot;holder&quot;に両方のサイズを提供します。 `DIV` ブラウザーウィンドウの中央に配置します。 また、Web ページでは `HTML` および `BODY` 要素を 100%に変更：

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

残りの埋め込み手順は、高さ無制限のレスポンシブデザイン埋め込みと同じです。 結果の例は次のようになります。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**セッターベースの API を使用した埋め込み**

JSON ベースの初期化を使用する代わりに、セッターベースの API と no-args コンストラクターを使用できます。 この API では、コンストラクターにパラメーターは不要で、設定パラメーターは `setContainerId()`, `setParam()`、および `setAsset()` API メソッドを個別の JavaScript 呼び出しで使用できます。

次の例は、セッターベースの API を使用した固定サイズ埋め込みを示しています。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```
