---
title: インタラクティブ画像
description: インタラクティブ画像ビューアは、クリック可能なホットスポットを含む、ズームできない単一の画像を表示するビューアです。 このビューアの目的は、「買い物可能なバナー」エクスペリエンスを実装することです。 つまり、ユーザーはバナー画像の上にホットスポットを選択し、web サイトのクイックビューまたは製品詳細ページにリダイレクトされます。 デスクトップやモバイルデバイスで動作するように設計されています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: c7089ecd-6ff3-4fe9-9ee7-3b48c9201558
TQID: 'https://experienceleague.adobe.com/9fVU6wcEpas7t-D3XZWWVcFL1On25qOeLOsvfSSKaz0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1720
ht-degree: 0%

---

# インタラクティブ画像{#interactive-image}

インタラクティブ画像ビューアは、クリック可能なホットスポットを含む、ズームできない単一の画像を表示するビューアです。 このビューアの目的は、「買い物可能なバナー」エクスペリエンスを実装することです。 つまり、ユーザーはバナー画像の上にホットスポットを選択し、web サイトのクイックビューまたは製品詳細ページにリダイレクトされます。 デスクトップやモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR （画像レンダリング）またはUGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアータイプは508です。

## デモ URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html)

-->

## システム要件 {#section-b7270cc4290043399681dc504f043609}

[必要システム構成](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

## インタラクティブ画像ビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

Interactive Image Viewerは、メインのJavaScript ファイルと一連のヘルパーファイルを表します（1つのJavaScriptには、この特定のビューア、アセット、CSSで使用されるすべてのビューア SDK コンポーネントが含まれています）。実行時にビューアがダウンロードします。

インタラクティブ画像ビューアは埋め込みモードでのみ使用できます。このモードでは、文書化されたAPIを使用してターゲット web ページに統合されます。

設定とスキニングは、このヘルプに記載されている他のビューアと同様です。 すべてのスキニングは、カスタム CSSを使用して実行できます。

すべてのビューアに共通する[ コマンド参照 – 構成属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通するコマンド参照 – URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください

## インタラクティブ画像ビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

Video Image Viewerでサポートされているインタラクションは、デスクトップシステムでのホットスポットのアクティベーションです。 このアクティベーションは、ワンタップでクリックおよびタッチデバイス上で行われます。

ビューアは完全にキーボードアクセス可能です。

[ キーボードのアクセシビリティとナビゲーション ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## インタラクティブ画像ビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

インタラクティブ画像ビューアは、ホスティングページに埋め込まれています。 このようなweb ページは、静的なレイアウトを持つ場合もあれば、異なるデバイスや異なるブラウザーウィンドウのサイズに対して「レスポンシブ」で異なる表示を行う場合もあります。

これらのニーズに対応するために、ビューアでは、固定サイズ埋め込みとレスポンシブ埋め込みの2つの主要な操作モードをサポートしています。

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアが既存のweb ページに追加されます。 このweb ページには、ビューアに関連しない一部の顧客コンテンツが既に含まれている可能性があります。 通常、閲覧者はweb ページの不動産の一部しか占めていません。

主なユースケースは、デスクトップ PCやタブレットデバイス向けのweb ページと、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインのページです。

初期読み込み後にビューアのサイズが変更されない場合は、固定サイズ埋め込みが使用されます。 この方法は、静的レイアウトを持つweb ページに最適です。

レスポンシブデザイン埋め込みは、コンテナ `DIV`のサイズ変更に応じて、実行時にビューアのサイズを変更する必要があることを前提としています。 最も一般的なユースケースは、柔軟性の高いページレイアウトを使用するweb ページにビューアを追加することです。

レスポンシブデザイン埋め込みモードでは、web ページのサイズとコンテナ `DIV`のサイズによって、ビューアの動作が異なります。 Web ページでコンテナ `DIV`の幅のみを設定し、高さを制限しない場合、ビューアは使用するアセットの縦横比に応じて自動的に高さを選択します。 この機能により、側面にパディングすることなく、アセットをビューに完全に収めることができます。 このユースケースは、BootstrapやFoundationなどのレスポンシブ web デザインレイアウトフレームワークを使用するweb ページで最も一般的です。

それ以外の場合、web ページでビューアのコンテナ `DIV`の幅と高さの両方を設定すると、ビューアはその領域だけを塗りつぶします。 また、web ページレイアウトが提供するサイズにも従います。 良い例は、ビューアをモーダルオーバーレイに埋め込むことです。このオーバーレイは、web ブラウザーのウィンドウサイズに応じてサイズが調整されます。

**固定サイズ埋め込み**

次の操作を実行して、ビューアをweb ページに追加します。

1. ビューアのJavaScript ファイルをweb ページに追加します。
1. コンテナ `DIV`を定義しています。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. ビューアのJavaScript ファイルをweb ページに追加します。

   ビューアを作成するには、HTML ヘッドにスクリプトタグを追加する必要があります。 ビューアーAPIを使用する前に、[!DNL InterativeImage.js]を含めることを確認してください。 [!DNL InteractiveImage.js] ファイルは、標準のIS-Viewers デプロイメントの[!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

ビューアがAdobe Dynamic Media Classic サーバーのいずれかにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-ViewersがインストールされているAdobe Dynamic Media Classic サーバーの1つにフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>ページ上のメイン ビューア JavaScript `include` ファイルのみを参照してください。 実行時にビューアのロジックによってダウンロードされる可能性があるweb ページコード内の他のJavaScript ファイルを参照しないでください。 特に、`/s7viewers` コンテキストパス（いわゆる統合SDK `include`）からビューアによって読み込まれたHTML5 SDK `Utils.js` ライブラリを直接参照しないでください。 その理由は、`Utils.js`または類似のランタイムビューアーライブラリの場所が、ビューアーのロジックによって完全に管理され、ビューアーリリース間で場所が変更されるためです。 Adobeは、古いバージョンのセカンダリビューア `includes`をサーバー上に保持しません。
>
>
>その結果、ビューアがページ上で使用するセカンダリ JavaScript `include`を直接参照すると、新しい製品バージョンがデプロイされる際に、将来的にビューア機能が破損します。

1. コンテナ `DIV`を定義しています。

   ビューアを表示するページに、空の`DIV`要素を追加します。 このIDは後でビューア APIに渡されるので、`DIV`要素にはIDが定義されている必要があります。 DIVのサイズはCSSで指定します。

   プレースホルダー`DIV`は配置された要素です。`position` CSS プロパティが`relative`または`absolute`に設定されていることを意味します。

   次に、定義済みのプレースホルダー`DIV`要素の例を示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアサイズの設定

   ビューアの静的サイズは、`.s7interactiveimage` トップレベル CSS クラスを絶対単位で宣言するか、`stagesize`修飾子を使用することで設定できます。

   CSSで直接HTML ページにサイズを設定できます。 または、カスタムビューア CSS ファイルにサイズを設定して、後でAdobe Experience Manager Assets オンデマンドのビューアプリセットレコードに割り当てるか、`style` コマンドを使用して明示的に渡すことができます。

   ビューアのCSSでのスタイル設定について詳しくは、[ ビデオ ](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)を参照してください。

   次に、HTML ページで静的ビューアサイズを定義する例を示します。

   ```html {.line-numbers}
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   `params` コレクションを使用してビューア初期化コードを使用して`stagesize`修飾子を明示的に渡すか、次のように「コマンドリファレンス」セクションで説明されているように、API呼び出しとして渡すことができます。

   ```html {.line-numbers}
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   CSS ベースのアプローチを推奨し、この例で使用します。

1. ビューアの作成と初期化。

   上記の手順を完了したら、`s7viewers.InteractiveImage` クラスのインスタンスを作成し、すべての構成情報をそのコンストラクターに渡し、ビューアーインスタンスで`init()` メソッドを呼び出します。 構成情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアコンテナ IDの名前を保持する`containerId` フィールドと、ビューアでサポートされている設定パラメーターを含むネストされた`params` JSON オブジェクトが必要です。 この場合、`params` オブジェクトには、少なくとも`serverUrl` プロパティとして渡された画像サービング URLと、`asset` パラメーターとして最初のアセットが必要です。 JSON ベースの初期化APIを使用すると、1行のコードでビューアを作成して開始できます。

   ビューアコードがIDでコンテナ要素を見つけられるように、ビューアコンテナをDOMに追加することが重要です。 一部のブラウザーは、Web ページの最後までDOMの構築を遅らせます。 互換性を最大限に高めるには、終了`BODY` タグの直前または本文`onload()` イベントで`init()` メソッドを呼び出します。

   同時に、コンテナ要素は必ずしもweb ページレイアウトの一部であってはなりません。 例えば、割り当てられた`display:none` スタイルを使用して非表示にすることができます。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで初期化プロセスを遅らせます。 このイベントが発生すると、ビューアの読み込みが自動的に再開されます。

   次に、ビューアインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡して`init()` メソッドを呼び出す例を示します。 この例では、`interactiveImage`がビューアインスタンスであると仮定します。`s7viewer`はプレースホルダー`DIV`の名前、`http://aodmarketingna.assetsadobe.com/is/image`は画像サービング URL、`/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.`はアセットです。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   ```

   次のコードは、ビデオイメージビューアを固定サイズで埋め込む面倒なweb ページの完全な例です。

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**高さの制限のないレスポンシブデザイン埋め込み**

レスポンシブデザインの埋め込みでは、通常、web ページには、ビューアのコンテナ `DIV`のランタイムサイズを決定する、ある種の柔軟なレイアウトが配置されています。 次の例では、web ページでビューアのコンテナ `DIV`がweb ブラウザーのウィンドウ サイズの40%を使用できるようになったと仮定します。 そして、その高さは無制限に残されています。 Web ページのHTML コードは次のようになります。

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

このようなページにビューアを追加することは、固定サイズ埋め込みの手順と似ています。 唯一の違いは、ビューアサイズを明示的に定義する必要がないことです。

1. ビューアのJavaScript ファイルをweb ページに追加します。
1. コンテナ `DIV`を定義しています。
1. ビューアの作成と初期化。

上記のすべての手順は、固定サイズの埋め込みと同じです。 コンテナ `DIV`を既存の`"holder"` `DIV`に追加します。 次のコードは、完全な例です。 ブラウザーのサイズを変更するとビューアのサイズが変わり、ビューアの縦横比がアセットとどのように一致するかを確認します。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

<!-- The following examples page illustrates more real-life uses of responsive design embedding with unrestricted height: -->

<!--

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html)

-->

**幅と高さが定義された柔軟なサイズ埋め込み**

幅と高さが定義された柔軟なサイズの埋め込みがある場合、web ページのスタイルが異なります。 `"holder"` DIVに両方のサイズを提供し、ブラウザーウィンドウの中央に配置します。 また、web ページでは、`HTML`要素と`BODY`要素のサイズが100%に設定されています。

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

残りの埋め込み手順は、高さの制限のないレスポンシブ埋め込みに使用する手順と同じです。 結果として得られる例は次のとおりです。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Setter ベースのAPIを使用した埋め込み**

JSON ベースの初期化を使用する代わりに、セッターベースのAPIとno-args コンストラクターを使用できます。 このAPI コンストラクターを使用すると、パラメーターは受け取られず、設定パラメーターは`setContainerId()`、`setParam()`、`setAsset()`のAPI メソッドを使用して指定され、別々のJavaScript呼び出しが行われます。

次の例は、セッターベースのAPIで固定サイズの埋め込みを使用する方法を示しています。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactiveimage { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var interactiveImage = new s7viewers.InteractiveImage(); 
interactiveImage.setContainerId("s7viewer"); 
interactiveImage.setParam("serverurl", "http://aodmarketingna.assetsadobe.com/is/image"); 
interactiveImage.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg"); 
interactiveImage.init(); 
</script> 
</body> 
</html> 
```
