---
title: インラインズーム
description: インラインズームビューアは、画像ビューアです。 ユーザーがメインビューにロールオーバーしたりタッチしたりすると、静的な画像の上にズームされたバージョンが表示され、静的な画像が表示されます。 このビューアは画像セットを操作し、スウォッチを使用してナビゲーションを行います。 デスクトップおよびモバイルデバイスで動作するように設計されています。
keywords: 応答
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 33e661b0-be5e-4d37-af88-47f7bc433c01
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2315'
ht-degree: 0%

---

# インラインズーム{#inline-zoom}

インラインズームビューアは、画像ビューアです。 ユーザーがメインビューにロールオーバーしたりタッチしたりすると、静的な画像の上にズームされたバージョンが表示され、静的な画像が表示されます。 このビューアは画像セットを操作し、スウォッチを使用してナビゲーションを行います。 デスクトップおよびモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR （画像レンダリング）または UGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアのタイプは 504 です。

[ システム要件と前提条件 ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842) を参照してください。

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400)

## インラインズームビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

インラインズームビューアは、実行時にビューアによってダウンロードされるメインのJavaScript ファイルとヘルパーファイルのセット（この特定のビューア、アセット、CSS で使用されるすべての Viewer SDK コンポーネントが含まれる 1 つのJavaScriptに相当）を表します。

インラインズームビューアは、画像サービングビューアに付属する実稼動対応のHTMLページを使用したポップアップモードと、ドキュメント化された API を使用してターゲットの web ページに統合する埋め込みモードの両方で使用できます。

設定とスキニングは、他のビューアと同様です。 カスタム CSS を使用してスキニングを適用できます。

[ すべてのビューアに共通のコマンドリファレンス – 設定属性 ](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [ すべてのビューアに共通のコマンドリファレンス - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) を参照してください

## インラインズームビューアの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

インラインズームビューアでは、他のモバイルアプリケーションに共通するシングルタッチジェスチャーとマルチタッチジェスチャーをサポートしています。

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
   <td colname="col2"> <p> フライアウト ビューをアクティブにするか、スウォッチのプライマリ ズーム レベルとセカンダリ ズーム レベルを変更して、新しいサムネイルを選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> スウォッチバーのスウォッチのリストをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直スワイプ </p> </td> 
   <td colname="col2"> <p>スウォッチ領域内でジェスチャーを行うと、ネイティブページのスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

また、このビューアは、タッチスクリーンとマウスを備えた Windows デバイスでのタッチ入力とマウス入力の両方をサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11、Edgeの web ブラウザーのみに制限されます。

このビューアは完全にキーボードでアクセス可能です。

詳しくは [ キーボードアクセシビリティとナビゲーション ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861) を参照してください。

## インラインズームビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

Web ページによって、ビューアの動作に対するニーズは異なります。 Web ページに、別のブラウザーウィンドウでビューアを開くクリック可能なリンクが表示される場合があります。 場合によっては、ビューアをホスティングページに直接埋め込む必要があります。 後者の場合、web ページのレイアウトが静的であったり、デバイスの違いやブラウザーウィンドウのサイズの違いによって表示が異なるレスポンシブデザインが使用されたりする場合があります。 これらのニーズに対応するために、ビューアでは 3 つの主要な操作モード（ポップアップ、固定サイズ埋め込み、レスポンシブ埋め込み）をサポートしています。

**ポップアップ**

ポップアップモードでは、ビューアは別の web ブラウザーウィンドウまたはタブで開きます。 ブラウザーウィンドウ領域全体を取得し、ブラウザーウィンドウのサイズが変更されたときや、デバイスの向きが変更されたときに調整されます。

このモードは、モバイルデバイスで最も一般的です。 Web ページは、JavaScript呼び出し、HTML要素 `window.open()` の適切な設定、またはその他の適切な方法 `A` 使用して、ビューアを読み込みます。

標準提供のHTMLページを `FlyoutViewer.html` というポップアップモードで使用することをお勧めします。 これは、標準の画像サービングビューアデプロイメントの [!DNL html5/] サブフォルダーにあります。

`<s7viewers_root>/html5/FlyoutViewer.html`

また、インラインズームモードで動作するように FlyoutZoomView コンポーネントを設定する必要もあります。 インラインズームビューアの標準の `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` プリセットまたはそれから派生したカスタムプリセットを使用することをお勧めします。 視覚的なカスタマイズは、カスタム CSS を適用することで実現できます。

次に、ビューアを新しいウィンドウで開くHTMLコードの例を示します。

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みとレスポンシブ埋め込み**

埋め込みモードでは、ビューアが既存の web ページに追加されます。これには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 閲覧者は通常、Web ページの不動産の一部のみを占有します。

主なユースケースは、デスクトップまたはタブレットデバイス向けの web ページと、デバイスタイプに応じて自動的にレイアウトを調整するレスポンシブ web ページです。

固定サイズ埋め込みモードは、ビューアの初回読み込み後にサイズが変更されない場合に使用されます。 この選択は、静的なページレイアウトを持つ web ページに最適です。

レスポンシブデザインの埋め込みモードでは、コンテナコンポー `DIV` ントのサイズ変更に応じて、実行時にビューアのサイズを変更する必要があることを前提としています。 最も一般的なユースケースは、柔軟なページレイアウトを使用する web ページにビューアを追加する場合です。

インラインズームビューアでレスポンシブデザインの埋め込みモードを使用する場合は、`imagereload` パラメーターを使用して、メインビュー画像の明示的なブレークポイントを指定していることを確認してください。 Web ページの CSS に記述されているビューア幅のブレークポイントを使用して、ブレークポイントを一致させるのが理想です。

レスポンシブデザインの埋め込みモードでは、web ページコンテナの `DIV` ージのサイズがどのように調整されるかによってビューアの動作が異なります。 Web ページでコンテナ `DIV` の幅のみが設定され、高さが制限されない場合、ビューアは、使用されるアセットの縦横比に応じて自動的に高さを選択します。 つまり、アセットは側面にパディングを入れずに、ビューに完全に収まります。 この特定のユースケースは、Bootstrapや基盤などのレスポンシブデザインレイアウトフレームワークを使用する web ページで最も一般的です。

Web ページでビューアのコンテナ `DIV` の幅と高さの両方が設定されている場合、ビューアはその領域のみを埋め、web ページレイアウトで提供されるサイズに従います。 良いユースケースの例は、ビューアをモーダルオーバーレイに埋め込む場合です。この場合、オーバーレイは web ブラウザーのウィンドウサイズに従ってサイズが調整されます。

**固定サイズ埋め込み**

Web ページにビューアを追加するには、次の手順を実行します。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ `DIV` を定義します。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. Web ページへのビューアJavaScript ファイルの追加

   ビューアを作成するには、HTMLの先頭にスクリプトタグを付ける必要があります。 ビューア API を使用する前に、必ず `FlyoutViewer.js` を含めてください。 `FlyoutViewer.js` は、標準の IS-Viewers デプロイメントの次の [!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

ビューアがAdobe Dynamic Media サーバーの 1 つにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 それ以外の場合は、IS-Viewers がインストールされているAdobe Dynamic Media サーバーの 1 つへのフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScript `include` ファイルのみを参照します。 実行時にビューアのロジックによってダウンロードされる可能性がある web ページコード内の追加のJavaScript ファイルを参照しないでください。 特に、ビューアによって読み込まれるHTML5 SDK `Utils.js` ライブラリをコンテキストパス（いわゆる統合 SDK `include`）から直接参照 `/s7viewers` ないでください。 これは、`Utils.js` や類似のランタイム・ビューア・ライブラリの場所はビューアのロジックによって完全に管理され、ビューア・リリース間で場所が変更されるためです。 Adobeは、古いバージョンのセカンダリ・ビューア `includes` をサーバ上に保持しません。
>
>
>その結果、ビューアが使用するセカンダリ JavaScript `include` ージをページ上で直接参照すると、今後、新しい製品バージョンがデプロイされた際に、ビューアの機能が損なわれます。

1. コンテナ DIV の定義。

   ビューアを表示するページに、空の DIV 要素を追加します。 DIV 要素には ID が定義されている必要があります。これは、この ID が後でビューア API に渡されるためです。

   プレースホルダー DIV が配置済み要素です（つまり、`position` CSS プロパティが `relative` または `absolute` に設定されています）。

   プレースホルダー DIV 要素に適した `z-index` を指定するのは、web ページの役割です。 これにより、ビューアのフライアウト部分が他の web ページ要素の上に表示されます。

   定義されたプレースホルダー DIV 要素の例を以下に示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. ビューアサイズの設定。

   このビューアには、複数項目セットを扱う際のサムネールが表示されます。 デスクトップ システムでは、サムネイルはメイン ビューの下に配置されます。 同時に、ビューアでは API を使用して、実行時にメインアセットを入れ替え `setAsset()` ことができます。 開発者は、新しいアセットに項目が 1 つしかない場合に、ビューアが下部のサムネール領域をどのように管理するかを制御できます。 外側のビューアのサイズはそのままにして、メインビューの高さを上げてサムネール領域を占有することができます。 または、メインビューのサイズを静的に保ち、外側のビューア領域を折りたたんで、web ページのコンテンツを上に移動させ、サムネールから残った空きページ領域を使用することもできます。

   外部ビューアの境界をそのままにするには、最上位の CSS クラス `.s7flyoutviewer` サイズを絶対単位で定義します。 CSS でのサイズ設定はHTMLページまたはカスタムビューア CSS ファイルに直接配置し、後でDynamic Media Classicのビューアプリセットレコードに割り当てるか、style コマンドを使用して明示的に渡すことができます。

   CSS を使用したビューアのスタイル設定について詳しくは、[ インラインズームビューアのカスタマイズ ](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) を参照してください。

   HTMLページで静的な外部ビューアのサイズを定義する例を次に示します。

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次のサンプルページでは、固定の外部ビューア領域での動作を確認できます。 セットを切り替えても、外側のビューアのサイズは変わりません。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html)

   メインビューのサイズを静的にするには、CSS セレクターを使用して、内部の `Container` SDK コンポーネントのビューアサイズ `.s7flyoutviewer .s7container` 絶対単位で定義します。 さらに、デフォルトのビューア CSS で `.s7flyoutviewer` の最上位レベルの CSS クラスに定義された固定サイズを `auto` に設定して上書きする必要があります。

   次に、アセットを切り替えるときにメイン表示領域のサイズが変更されないように、内部の `Container` SDK コンポーネントのビューアサイズを定義する例を示します。

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

   次のサンプルページは、固定のメインビューサイズを使用したビューアの動作を示しています。 セットを切り替えると、メインビューは静的なままになり、web ページコンテンツは垂直方向に移動します。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html)

   また、デフォルトのビューア CSS では、すぐに使用できる外部領域のサイズが固定されています。

1. ビューアの作成と初期化。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報 `s7viewers.FlyoutViewer` そのコンストラクターに渡して、ビューアインスタンスのメソッド `init()` 呼び出します。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトにはビューアコンテナ ID の名前を保持する `containerId` フィールドと、ビューアがサポートす `params` 設定パラメーターを含むネストされた JSON オブジェクトが必要です。 この場合、`params` オブジェクトには、少なくとも画像サービング URL がプロパティとして渡されてい `serverUrl` 必要があります。初期アセットは `asset` パラメーター、CSS を読み込むためのベースパスは `contentUrl` パラメーター、プリセット名は `config` パラメーターです。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成して開始できます。

   ビューアコードが ID でコンテナ要素を見つけられるように、ビューアコンテナを DOM に追加することが重要です。 一部のブラウザーでは、web ページの最後まで DOM の構築が遅れます。 互換性を最大限に高めるには、終了 `BODY` タグの直前または body `onload()` イベントで `init()` メソッドを呼び出します。

   同時に、コンテナ要素は、まだ web ページレイアウトの一部である必要はありません。 例えば、割り当てられたスタイルを使用して非表示 `display:none` する場合があります。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで、初期化プロセスを遅延します。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

   以下に、ビューアインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡して、`init()` メソッドを呼び出す例を示します。 この例では、`inlineZoomViewer` はビューアインスタンス、`s7viewer` はプレースホルダー `DIV` の名前、`http://s7d1.scene7.com/is/image/` は画像サービング URL、`Scene7SharedAssets/ImageSet-Views-Sample` はアセットであると仮定します。

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

   次のコードは、インラインズームビューアを固定サイズで埋め込む単純な web ページの完全な例です。

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

## 高さが制限されないレスポンシブデザインの埋め込み {#section-056cb574713c4d07be6d07cf3c598839}

レスポンシブデザインの埋め込みを使用すると、通常、web ページには、ビューアのコンテナ `DIV` ージの実行時サイズを指定する何らかの柔軟なレイアウトが配置されます。 次の例では、web ページで、ビューアのコンテナ `DIV` が web ブラウザーのウィンドウサイズの 40% を占め、高さは無制限であるとします。 Web ページのHTMLコードは次のようになります。

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

このようなページにビューアを追加する手順は、固定サイズの埋め込みを行う手順と似ています。 唯一の違いは、デフォルトのビューア CSS の固定サイズ設定を、相対単位で設定されたサイズで上書きする必要があることです。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ `DIV` を定義します。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

上記の手順はすべて、固定サイズの埋め込みを使用する場合と同じですが、次の 3 つの例外があります。

* コンテナ `DIV` を既存の「holder」 `DIV` ージに追加します。
* 明示的 `imagereload` ブレークポイントを持つパラメーターが追加されました。
* 絶対単位を使用して固定のビューアサイズを設定する代わりに、次のようにビューアの `width` と `height` を 100% に設定する CSS を使用します。

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

次のコードは完全な例です。 ブラウザーのサイズを変更するとビューアのサイズがどのように変化するか、ビューアの縦横比がアセットとどのように一致するかを確認します。

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

以下の例では、高さが制限されないレスポンシブデザインの埋め込みを使用した実際の使用例を示しています。

[ ライブデモ ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[ 代替デモの場所 ](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## 幅と高さが定義された柔軟なサイズ埋め込み {#section-0a329016f9414d199039776645c693de}

幅と高さが定義されたフレキシブルサイズの埋め込みがある場合、web ページのスタイル設定は異なります。 `"holder"` DIV のサイズとブラウザーウィンドウの中央に配置されるサイズの両方が指定されます。 また、web ページでは、`HTML` と `BODY` 要素のサイズが 100% に設定されます。

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

残りの埋め込み手順は、高さが制限されないレスポンシブデザインの埋め込みに使用される手順と同じです。 結果の例を次に示します。

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

## セッターベースの API を使用した埋め込み {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

JSON ベースの初期化を使用する代わりに、setter ベースの API および no-args コンストラクターを使用することができます。 この API コンストラクターを使用すると、パラメーターは取得されず、`setContainerId()`、`setParam()`、`setAsset()` の API メソッドを使用して、別個のJavaScript呼び出しで設定パラメーターが指定されます。

次の例は、setter ベースの API を使用した固定サイズの埋め込みの使用を示しています。

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
