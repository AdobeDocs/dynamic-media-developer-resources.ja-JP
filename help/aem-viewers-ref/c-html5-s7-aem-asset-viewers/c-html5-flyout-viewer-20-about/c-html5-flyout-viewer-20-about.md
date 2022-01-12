---
title: フライアウト
description: フライアウトビューアは画像ビューアです。 ユーザがアクティブにするフライアウトビューに表示されるズームされたバージョンで、静的な画像が表示されます。 このビューアは画像セットで機能し、ナビゲーションはスウォッチを使用しておこないます。 デスクトップおよびモバイルデバイスで動作するように設計されています。
keywords: レスポンシブ
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '2065'
ht-degree: 0%

---

# フライアウト{#flyout}

フライアウトビューアは画像ビューアです。 ユーザがアクティブにするフライアウトビューに表示されるズームされたバージョンで、静的な画像が表示されます。 このビューアは画像セットで機能し、ナビゲーションはスウォッチを使用しておこないます。 デスクトップおよびモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR（画像レンダリング）または UGC（ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされません。

ビューアのタイプは 504 です。

詳しくは、 [必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## フライアウトビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

フライアウトビューアは、メインの JavaScript ファイルと、ヘルパーファイルのセット（この特定のビューア、アセット、CSS で使用されるすべてのビューア SDK コンポーネントを含む単一の JavaScript インクルード）で、ビューアが実行時にダウンロードします

フライアウトビューアは、埋め込みでの使用のみを目的としています。つまり、ドキュメントに記載された API を使用して Web ページに統合されます。 フライアウトビューアには、実稼動に対応した Web ページはありません。

設定とスキニングは、他のビューアと同様です。 スキニングを適用するには、カスタム CSS を使用できます。

詳しくは、 [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

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

タッチスクリーンとマウスを備えた Windows デバイスでは、タッチ入力とマウス入力の両方がサポートされます。 ただし、このサポートは、Chrome、Internet Explorer 11 および Edge Web ブラウザーにのみ制限されます。

このビューアは完全にキーボードでアクセス可能です。

詳しくは、 [キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## フライアウトビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Web ページごとに異なります。 Web ページに静的ページレイアウトが含まれている場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは次の 2 つの主要な操作モードがサポートされています。固定サイズ埋め込みとレスポンシブデザイン埋め込みを使用しました。

固定サイズ埋め込みモードは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 この選択は、静的ページレイアウトの Web ページに最適です。

レスポンシブデザイン埋め込みモードは、コンテナのサイズ変更に応じて実行時にビューアのサイズを変更する必要がある場合を想定しています `DIV`. 最も一般的な使用例は、柔軟なページレイアウトを使用する Web ページにビューアを追加する場合です。

フライアウトビューアでレスポンシブデザイン埋め込みモードを使用する場合は、 `imagereload` パラメーター。 ブレークポイントを、Web ページの CSS で指定されているビューアの幅のブレークポイントと一致させるのが理想です。

レスポンシブデザイン埋め込みモードでは、Web ページのコンテナの動作方法によって、ビューアの動作が異なります `DIV` サイズが設定されています。 Web ページでコンテナの幅のみが設定される場合 `DIV`を指定し、高さは無制限のままにした場合、使用するアセットの縦横比に従って、ビューアによって高さが自動的に選択されます。 つまり、両側のパディングなしで、アセットが表示に完全に収まります。 この特定の使用例は、Web ページで、Web や Foundation などのレスポンシブデザインレイアウトフレームワークを使用する WebBootstrapで最も一般的です。

それ以外の場合は、Web ページでビューアのコンテナの幅と高さの両方が設定されている場合 `DIV`を指定した場合、ビューアはその領域のみを埋め、Web ページレイアウトで指定されるサイズに従います。 良い使用例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイが Web ブラウザーのウィンドウサイズに従ってサイズ変更される場合があります。

**固定サイズ埋め込み**

ビューアを Web ページに追加するには、次の手順を実行します。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナの定義 `DIV`.
1. ビューアのサイズを設定します。
1. ビューアを作成および初期化する。

1. ビューアの JavaScript ファイルを Web ページに追加する。

   ビューアを作成するには、HTMLhead にスクリプトタグを追加する必要があります。 ビューア API を使用する前に、 `FlyoutViewer.js`. `FlyoutViewer.js` が次の値に含まれる [!DNL html5/js/] 標準の IS-Viewers デプロイメントのサブフォルダー

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

ビューアがDynamic MediaAdobeの 1 つにデプロイされ、同じドメインから提供されている場合は、相対パスを使用できます。 それ以外の場合は、IS-Viewers がインストールされているAdobeDynamic Mediaサーバーの 1 つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>メインビューアの JavaScript のみを参照します。 `include` ファイルをページに貼り付けます。 実行時にビューアのロジックによってダウンロードされる可能性のある、Web ページコード内の追加の JavaScript ファイルは参照しないでください。 特に、HTML5 SDK を直接参照しないでください `Utils.js` からビューアによって読み込まれたライブラリ `/s7viewers` コンテキストパス（いわゆる統合 SDK） `include`) をクリックします。 理由は、 `Utils.js` または同様のランタイムビューアライブラリは、ビューアのロジックによって完全に管理され、ビューアのリリースによって位置が変わります。 Adobeは古いバージョンのセカンダリビューアを保持しません `includes` をサーバー上に置きます。
>
>
>その結果、セカンダリ JavaScript への直接参照を配置する `include` ページ上でビューアが使用すると、新しい製品バージョンがデプロイされると、将来ビューア機能が機能しなくなります。

1. コンテナ DIV を定義する。

   ビューアを表示するページに空の DIV 要素を追加します。 DIV 要素の ID は、後でビューアの API に渡されるので、定義する必要があります。

   プレースホルダ DIV は配置された要素です。つまり、 `position` CSS プロパティがに設定されている `relative` または `absolute`.

   適切な `z-index` プレースホルダ DIV 要素用。 これにより、ビューアのフライアウト部分が Web ページの他の要素の上に表示されます。

   次に、定義済みのプレースホルダ DIV 要素の例を示します。

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. ビューアのサイズを設定します。

   複数項目セットを操作する場合、このビューアにはサムネールが表示されます。 デスクトップシステムでは、サムネールはメインビューの下に配置されます。 同時に、ビューアでは、実行時に `setAsset()` API 開発者は、新しいアセットに項目が 1 つしかない場合に、下部のサムネール領域をビューアがどのように管理するかを制御できます。 ビューアの外側のサイズはそのままにして、メインビューの高さを増やし、サムネール領域を表示させることができます。 また、メインビューのサイズを静的に保ち、ビューアの外側の領域を折りたたんで、Web ページのコンテンツを上に移動して、サムネールから残されたページの空き領域を使用することもできます。

   ビューアの外側の境界をそのまま残すには、 `.s7flyoutviewer` 最上位 CSS クラス（絶対単位）。 CSS のサイズ変更は、HTMLページやカスタムビューア CSS ファイルに適用し、後でDynamic Media Classicのビューアプリセットレコードに割り当てるか、style コマンドを使用して明示的に渡すことができます。

   詳しくは、 [フライアウトビューアのカスタマイズ](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) を参照してください。

   次の例では、ビューアページでビューアの外側の静的サイズを定義しています。HTML

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次のサンプルページで、ビューアの外側の領域が固定された状態の動作を確認できます。 セットを切り替えても、ビューアの外側のサイズは変わりません。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   メインビューのサイズを静的にするには、内側の絶対単位でビューアのサイズを定義します `Container` を使用した SDK コンポーネント `.s7flyoutviewer .s7container` CSS セレクター。 また、 `.s7flyoutviewer` 初期設定のビューア CSS の最上位 CSS クラス（をに設定） `auto`.

   以下は、内部のビューアサイズを定義する例です `Container` アセットを切り替える際にメインビュー領域のサイズが変更されないようにする SDK コンポーネント：

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

   以下のサンプルページは、メインビューのサイズを固定した場合のビューアの動作を示しています。 セットを切り替えても、メインビューは静的なままになり、Web ページのコンテンツは垂直方向に移動します。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html)

   また、初期設定のビューア CSS では、その外側の領域のサイズが初期設定で固定されています。

1. ビューアを作成および初期化する。

   上記の手順を完了したら、のインスタンスを作成します。 `s7viewers.FlyoutViewer` クラス、すべての設定情報をコンストラクタに渡し、を呼び出します。 `init()` メソッドを使用して、ビューアインスタンス上に配置できます。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには `containerId` ビューアのコンテナ ID とネストされたコンテナの名前が格納されるフィールド `params` ビューアがサポートする設定パラメーターを含む JSON オブジェクト。 この場合、 `params` オブジェクトには、少なくとも `serverUrl` プロパティとして、最初のアセットを `asset` パラメーター。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成し、起動できます。

   ビューアのコンテナを DOM に追加して、ビューアのコードが ID でコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Web ページの終わりまで DOM の構築が遅れます。 互換性を最大限に高めるには、 `init()` 終了直前の方法 `BODY` タグ、または本文 `onload()` イベント。

   同時に、コンテナ要素は必ずしも Web ページレイアウトに含まれているとは限りません。 例えば、 `display:none` スタイルが割り当てられています。 この場合、Web ページでコンテナ要素がレイアウトに戻るまで、ビューアは初期化プロセスを遅延します。 この操作を実行すると、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、 `init()` メソッド。 この例では、次のように仮定します。 `flyoutViewer` はビューアインスタンスです。 `s7viewer` はプレースホルダーの名前です `DIV`; `http://s7d1.scene7.com/is/image/` は画像サービングの URL です。および `Scene7SharedAssets/ImageSet-Views-Sample` はアセットです。

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

   次のコードは、固定サイズのフライアウトビューアを埋め込んだ簡単な Web ページの例です。

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

レスポンシブデザイン埋め込みでは、Web ページには通常、ビューアのコンテナの実行時のサイズを指示する柔軟なレイアウトが指定されています `DIV`. 次の例では、Web ページがビューアのコンテナを許可しているとします `DIV` を使用すると、web ブラウザーのウィンドウサイズの 40%を占め、高さは無制限のままになります。 Web ページのHTMLコードは次のようになります。

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

このようなページにビューアを追加する手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、初期設定のビューア CSS の固定サイズを、相対単位で設定されたサイズで上書きする必要がある点です。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナの定義 `DIV`.
1. ビューアのサイズを設定します。
1. ビューアを作成および初期化する。

上記の手順はすべて、固定サイズ埋め込みの場合と同じですが、次の 3 つの例外があります。

* コンテナの追加 `DIV` 既存の「所有者」に `DIV`;
* 追加済み `imagereload` 明示的なブレークポイントを持つパラメーター
* 絶対単位を使用してビューアの固定サイズを設定する代わりに、次のようにビューアの幅と高さを 100%に設定する CSS を使用します。

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化すること、およびビューアの縦横比がアセットと一致することに注意してください。

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

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実際に使用されている例を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[代替のデモの場所](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## 幅と高さが定義されたフレキシブルサイズ埋め込み {#section-0a329016f9414d199039776645c693de}

幅と高さが定義されたフレキシブルサイズ埋め込みがある場合、Web ページのスタイル設定は異なります。 次の両方のサイズを `"holder"` DIV を指定し、ブラウザーウィンドウの中央に配置します。 また、Web ページでは `HTML` および `BODY` 要素を 100%に設定します。

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

残りの埋め込み手順は、高さ無制限のレスポンシブデザイン埋め込みで使用した手順と同じです。 結果の例は次のようになります。

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

## セッターベースの API を使用した埋め込み {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

JSON ベースの初期化を使用する代わりに、セッターベースの API と no-args コンストラクターを使用できます。 この API コンストラクターを使用する場合は、パラメーターは必要ありません。設定パラメーターは、 `setContainerId()`, `setParam()`、および `setAsset()` API メソッドと個別の JavaScript 呼び出し。

次の例は、固定サイズ埋め込みをセッターベースの API で使用する方法を示しています。

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
