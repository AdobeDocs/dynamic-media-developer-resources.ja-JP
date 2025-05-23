---
title: カルーセル
description: カルーセルビューアは、クリック可能なホットスポットまたは領域のあるズームできないバナー画像のカルーセルを表示するビューアです。 このビューアは、「ショッパブルカルーセル」エクスペリエンスを実装するのに役立ちます。このエクスペリエンスでは、ユーザーがバナー画像上のホットスポットまたは領域を選択できます。 顧客の web サイトのクイックビューまたは製品詳細ページにリダイレクトできます。 デスクトップおよびモバイルデバイスで動作するように設計されています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: d506dc6e-8929-4f7f-a205-1683e77681f1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1867'
ht-degree: 0%

---

# カルーセル{#carousel}

カルーセルビューアは、クリック可能なホットスポットまたは領域のあるズームできないバナー画像のカルーセルを表示するビューアです。 このビューアは、「ショッパブルカルーセル」エクスペリエンスを実装するのに役立ちます。このエクスペリエンスでは、ユーザーがバナー画像上のホットスポットまたは領域を選択できます。 顧客の web サイトのクイックビューまたは製品詳細ページにリダイレクトできます。 デスクトップおよびモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>画像レンダリングまたはユーザー生成コンテンツ（UGC）を使用する画像は、このビューアではサポートされていません。

ビューアのタイプは 511 です。

## デモ URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html?lang=ja](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html?lang=ja)

## システム要件 {#section-b7270cc4290043399681dc504f043609}

[ 必要システム構成 ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842) を参照してください。

## カルーセルビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

カルーセルビューアは、実行時にビューアによってダウンロードされるメインのJavaScript ファイルと一連のヘルパーファイル（この特定のビューア、アセット、CSS で使用されるすべての Viewer SDK コンポーネントに含まれる 1 つのJavaScript インクルード）を表します。

カルーセルビューアは、IS ビューアに付属する実稼動用のHTMLページを使用するポップアップモードと、ドキュメント化された API を使用して目的の web ページに統合する埋め込みモードの両方で使用できます。

設定とスキニングは、このヘルプで説明する他のビューアの設定と似ています。 すべてのスキニングは、カスタム CSS を使用して行います。

[ すべてのビューアに共通のコマンドリファレンス – 設定属性 ](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [ すべてのビューアに共通のコマンドリファレンス - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) を参照してください

## カルーセルビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

カルーセルセット内の移動は、メインビューを水平にスワイプするか、デスクトップデバイスで使用できる 2 つの矢印ボタンを使用して行います。 セットインジケーターのドットは、セット内の現在の位置を示します。

ビューアでは、バナー画像上にホットスポットまたは領域をレンダリングして、製品上のインタラクティブな領域を示すことができます。

ホットスポットまたはリージョンをクリックまたはタップすると、オーサー時にホットスポットまたはリージョンに関連付けられたアクションがトリガーされます。 アクションは、web サイトの別のページにリダイレクトされる場合や、商品情報を web ページロジックに戻す場合があります。これにより、関連する商品コンテンツを含むクイックビューがトリガーになる可能性があります。

ビューアは完全にキーボードでアクセス可能です。

詳しくは [ キーボードアクセシビリティとナビゲーション ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861) を参照してください。

## カルーセルビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

**ポップアップモードについて**

ポップアップモードでは、ビューアは別の web ブラウザーウィンドウまたはタブで開きます。 ブラウザーのサイズが変更された場合や、モバイルデバイスの向きが変更された場合に、ブラウザーウィンドウ領域全体を使用して調整が行われます。

ポップアップモードは、モバイルデバイスで最も一般的です。 Web ページは、JavaScript呼び出し、HTML要素 `window.open()` の適切な設定、またはその他の適切なメソッド `A` 使用して、ビューアを読み込みます。

標準提供のHTMLページをポップアップ表示に使用することをお勧めします。 この場合、`CarouselViewer.html` という名前で、標準の IS-Viewers デプロイメントの `html5/` サブフォルダー内に配置されます。

`<s7viewers_root>/html5/CarouselViewer.html`

カスタム CSS を適用すると、視覚的にカスタマイズできます。

次に、ビューアを新しいウィンドウで開くHTMLコードの例を示します。

```html {.line-numbers}
<a href="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/CarouselViewer.html?asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner&serverurl=https://adobedemo62-h.assetsadobe.com/is/image" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアが既存の web ページに追加されます。 この Web ページには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 閲覧者は通常、Web ページの不動産の一部のみを占有します。

主なユースケースは、デスクトップまたはタブレットデバイス向けの web ページと、デバイスタイプに応じて自動的にレイアウトを調整するレスポンシブデザインのページです。

固定サイズの埋め込みは、初回読み込み後にビューアのサイズが変更されない場合に使用されます。 この方法は、静的なレイアウトを持つ web ページに最適です。

レスポンシブデザインの埋め込みは、コンテナコンポー `DIV` ントのサイズ変更に応じて、実行時にビューアのサイズを変更する必要があることを前提としています。 最も一般的なユースケースは、柔軟なページレイアウトを使用する web ページにビューアを追加する場合です。

レスポンシブデザインの埋め込みモードでは、web ページのコンテナコンポー `DIV` ントのサイズがどのように調整されるかに応じて、ビューアの動作が異なります。 Web ページでコンテナ `DIV` の幅のみが設定され、高さが制限されない場合、ビューアは、使用されるアセットの縦横比に応じて自動的に高さを選択します。 この機能により、アセットが側面にパディングを入れずに、ビューに完全に収まります。 このユースケースは、Bootstrapや基盤などのレスポンシブ web デザインレイアウトフレームワークを使用する web ページで最も一般的です。

そうでない場合、Web ページでビューアのコンテナ `DIV` の幅と高さの両方が設定されていると、ビューアはその領域だけを埋めます。 Web ページレイアウトで提供されるサイズにも従います。 良い例は、ビューアをモーダルオーバーレイに埋め込む場合です。この場合、オーバーレイは web ブラウザーのウィンドウサイズに応じてサイズが調整されます。

**固定サイズ埋め込み**

Web ページにビューアを追加するには、次の手順を実行します。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ `DIV` を定義します。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. Web ページへのビューアJavaScript ファイルの追加

   ビューアを作成するには、HTMLの先頭にスクリプトタグを付ける必要があります。 ビューア API を使用する前に、必ず [!DNL CarouselViewer.js] を含めてください。 [!DNL CarouselViewer.js] ファイルは、標準の IS-Viewers デプロイメントの [!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js]

ビューアがAdobe Dynamic Media Classic サーバーの 1 つにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-Viewers がインストールされているAdobe Dynamic Media Classic サーバーの 1 つへのフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScript `include` ファイルのみを参照します。 実行時にビューアのロジックによってダウンロードされる可能性がある web ページコード内の追加のJavaScript ファイルを参照しないでください。 特に、ビューアによって読み込まれるHTML5 SDK `Utils.js` ライブラリをコンテキストパス（いわゆる統合 SDK `include`）から直接参照 `/s7viewers` ないでください。 これは、`Utils.js` や類似のランタイム・ビューア・ライブラリの場所はビューアのロジックによって完全に管理され、ビューア・リリース間で場所が変更されるためです。 Adobeは、古いバージョンのセカンダリ・ビューア `includes` をサーバ上に保持しません。
>
>
>その結果、ビューアが使用するセカンダリ JavaScript `include` ージをページ上で直接参照すると、今後、新しい製品バージョンがデプロイされた際に、ビューアの機能が損なわれます。

1. コンテナ `DIV` を定義します。

   ビューアを表示するページに、空の `DIV` 要素を追加します。 `DIV` 要素には ID が定義されている必要があります。これは、この ID が後でビューア API に渡されるためです。 DIV のサイズは CSS で指定します。

   プレースホルダー `DIV` は配置済み要素です。つまり、`position` CSS プロパティは `relative` または `absolute` に設定されています。

   定義されたプレースホルダー `DIV` 要素の例を以下に示します。

   ```CSS {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアサイズの設定

   ビューアの静的サイズは、トップレベル CSS クラスに対して絶対単位で宣言す `.s7carouselviewer` か、修飾子を使用して設定 `stagesize` きます。

   HTMLページに直接、CSS でサイズ設定を指定できます。 サイズ設定はカスタムビューアの CSS ファイルに入れることができます。この CSS ファイルは、後でAEM Assetsのビューアプリセットレコードにオンデマンドで割り当てられるか、`style` コマンドを使用して明示的に渡されます。

   CSS を使用したビューアのスタイル設定について詳しくは、[ カルーセルビューアのカスタマイズ ](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) を参照してください。

   HTMLページで静的ビューアのサイズを定義する例を以下に示します。

   ```CSS {.line-numbers}
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   `stagesize` 修飾子は、コレクションを使用したビューア初期化コードまたは「コマンドリファレンス」セクションで説明されてい `params`API 呼び出しとして、次のように明示的に渡すことができます。

   ```CSS {.line-numbers}
   carouselViewer.setParam("stagesize", "1174,500");
   ```

   この例では、CSS ベースのアプローチをお勧めします。

1. ビューアの作成と初期化。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報 `s7viewers.CarouselViewer` そのコンストラクターに渡し、ビューアインスタンスのメソッド `init()` 呼び出します。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトにはビューアコンテナ ID の名前 `containerId` 保持するフィールドと、ビューアでサポートされ `params` 設定パラメーターを含むネストされた JSON オブジェクトが必要です。 この場合、`params` オブジェクトには、少なくとも画像サービング URL がプロパティとして渡され、初期アセット `serverUrl` パラメーターとして渡されてい `asset` 必要があります。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成して開始できます。

   ビューアコードが ID でコンテナ要素を見つけられるように、ビューアコンテナを DOM に追加することが重要です。 一部のブラウザーでは、web ページの最後まで DOM の構築が遅れます。 互換性を最大限に高めるには、終了 `BODY` タグの直前または body `onload()` イベントで `init()` メソッドを呼び出します。

   同時に、コンテナ要素は、まだ web ページレイアウトの一部である必要はありません。 例えば、割り当てられたスタイルを使用して非表示 `display:none` する場合があります。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで、初期化プロセスを遅延します。 この機能が発生すると、ビューアの読み込みが自動的に再開されます。

   次に、ビューアインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡して `init()` メソッドを呼び出す例を示します。 この例では、`carouselViewer` がビューアインスタンス、`s7viewer` がプレースホルダー `DIV` の名前、`https://adobedemo62-h.assetsadobe.com/is/image` が画像サービング URL、`/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner` がアセットであることを前提としています。

   ```javascript {.line-numbers}
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、カルーセルビューアを固定サイズで埋め込む簡単な web ページの完全な例です。

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高さが制限されないレスポンシブデザインの埋め込み**

レスポンシブデザインの埋め込みを使用すると、通常、web ページには、ビューアのコンテナ `DIV` ージの実行時サイズを指定する何らかの柔軟なレイアウトが配置されます。 次の例では、web ページで、ビューアのコンテナ `DIV` が web ブラウザーのウィンドウサイズの 40% を占めるとします。 そして、その高さは無制限に残されています。 Web ページのHTMLコードは次のようになります。

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

このようなページにビューアを追加する手順は、固定サイズの埋め込みを行う手順と似ています。 唯一の違いは、ビューアのサイズを明示的に定義する必要がないことです。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ `DIV` を定義します。
1. ビューアの作成と初期化。

上記の手順はすべて、固定サイズの埋め込みと同じです。 コンテナ `DIV` を既存の `"holder"` `DIV` に追加します。 次のコードは完全な例です。 ブラウザーのサイズを変更するとビューアのサイズがどのように変化するか、ビューアの縦横比がアセットとどのように一致するかを確認します。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下の例では、高さが制限されないレスポンシブデザインの埋め込みを使用した実際の使用例を示しています。

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html?lang=ja](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html?lang=ja)

**幅と高さが定義された柔軟なサイズの埋め込み**

幅と高さが定義されたフレキシブルサイズの埋め込みでは、web ページのスタイル設定が異なります。 `"holder"` DIV のサイズとブラウザーウィンドウの中央に合わせたサイズの両方が提供されます。 また、web ページでは、`HTML` と `BODY` 要素のサイズが 100% に設定されます。

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

残りの埋め込みステップは、高さが制限されないレスポンシブ埋め込みに使用されるステップと同じです。 結果の例を次に示します。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Setter ベースの API を使用した埋め込み**

JSON ベースの初期化を使用する代わりに、setter ベースの API および no-args コンストラクターを使用することができます。 この API コンストラクターを使用すると、パラメーターは取得されず、`setContainerId()`、`setParam()`、`setAsset()` の API メソッドを使用して、個別のJavaScript呼び出しで設定パラメーターが指定されます。

次の例は、setter ベースの API を使用した固定サイズの埋め込みの使用を示しています。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7carouselviewer { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer(); 
carouselViewer.setContainerId("s7viewer"); 
carouselViewer.setParam("serverurl", "https://adobedemo62-h.assetsadobe.com/is/image"); 
carouselViewer.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner"); 
carouselViewer.init(); 
</script> 
</body> 
</html>
```
