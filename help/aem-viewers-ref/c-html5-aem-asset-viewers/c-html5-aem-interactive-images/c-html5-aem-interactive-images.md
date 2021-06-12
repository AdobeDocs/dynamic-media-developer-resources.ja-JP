---
description: インタラクティブ画像ビューアは、クリック可能なホットスポットを含む、ズーム不可能な単一の画像を表示するビューアです。 このビューアの目的は、「ショッパブルバナー」エクスペリエンスを実装することです。 つまり、バナー画像上のホットスポットを選択すると、Webサイトのクイックビューまたは製品の詳細ページにリダイレクトされます。 デスクトップおよびモバイルデバイスで動作するように設計されています。
solution: Experience Manager
title: インタラクティブ画像
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブ画像
role: Developer,Business Practitioner
exl-id: c7089ecd-6ff3-4fe9-9ee7-3b48c9201558
source-git-commit: e6ff4ed80b22e10fc2bd3fac0f4e39bbf5148f8e
workflow-type: tm+mt
source-wordcount: '1733'
ht-degree: 0%

---

# インタラクティブ画像{#interactive-image}

インタラクティブ画像ビューアは、クリック可能なホットスポットを含む、ズーム不可能な単一の画像を表示するビューアです。 このビューアの目的は、「ショッパブルバナー」エクスペリエンスを実装することです。 つまり、バナー画像上のホットスポットを選択すると、Webサイトのクイックビューまたは製品の詳細ページにリダイレクトされます。 デスクトップおよびモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR（画像レンダリング）またはUGC（ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアタイプは508です。

## デモURL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html)

## システム要件 {#section-b7270cc4290043399681dc504f043609}

[必要システム構成](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

## インタラクティブ画像ビューアの使用{#section-e6c68406ecdc4de781df182bbd8088b4}

インタラクティブ画像ビューアは、メインのJavaScriptファイルと、ビューアによって実行時にダウンロードされるヘルパーファイルのセット（この特定のビューア、アセット、CSSで使用されるすべてのビューアSDKコンポーネントを含む単一のJavaScriptインクルード）です。

インタラクティブ画像ビューアは、埋め込みモードでのみ使用でき、ドキュメントに記載されているAPIを使用してターゲットWebページに統合されます。

設定とスキン表示は、このヘルプで説明する他のビューアと同様です。 スキンの適用はすべて、カスタムCSSを使用して行います。

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください。

## インタラクティブ画像ビューアの操作{#section-642e66ca38cd4032992840ec6c0b0cd2}

ビデオ画像ビューアでサポートされているインタラクションは、デスクトップシステムでのホットスポットのアクティブ化です。 このアクティベーションは、1回のタップでのクリック時およびタッチデバイスで発生します。

ビューアは完全にキーボードでアクセス可能です。

[キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## インタラクティブ画像ビューアの埋め込み{#section-6bb5d3c502544ad18a58eafe12a13435}

インタラクティブ画像ビューアは、ホスティングページに埋め込むように設計されています。 このようなWebページは、静的なレイアウトを持つ場合や、「レスポンシブ」で、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わる場合があります。

これらのニーズに対応するために、ビューアでは、次の2つの主要な操作モードがサポートされています。固定サイズ埋め込みとレスポンシブ埋め込み。

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存のWebページに追加されます。 このWebページには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 ビューアは、通常、Webページの一部の領域のみを占有します。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、およびデバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 これは、静的レイアウトのWebページに最適です。

レスポンシブデザイン埋め込みは、コンテナ`DIV`のサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定しています。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナ`DIV`のサイズ変更の方法によって、ビューアの動作が異なります。 Webページでコンテナ`DIV`の幅のみが設定され、高さは無制限のままの場合、ビューアでは、使用するアセットの縦横比に従って高さが自動的に選択されます。 この機能により、側面のパディングなしで、アセットが表示にぴったりと収まります。 この使用例は、Bootstrap、FoundationなどのレスポンシブWebデザインレイアウトフレームワークを使用するWebページで最も一般的です。

それ以外の場合、Webページでビューアのコンテナ`DIV`の幅と高さの両方が設定されていると、ビューアはその領域だけを占めます。 また、Webページのレイアウトに従うサイズにもなります。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合があります。

**固定サイズ埋め込み**

ビューアをWebページに追加するには、次の手順を実行します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナ`DIV`を定義します。
1. ビューアのサイズを設定する。
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにscriptタグを追加する必要があります。 ビューアのAPIを使用するには、必ず[!DNL InterativeImage.js]を含めてください。 [!DNL InteractiveImage.js]ファイルは、次に示すように、IS-Viewersの標準のデプロイ先の[!DNL html5/js/]サブフォルダーにあります。

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

ビューアがDynamic Media ClassicAdobeのいずれかにデプロイされ、同じドメインから提供されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobeDynamic Media Classicサーバーの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>ページ上では、メインビューアのJavaScript `include`ファイルのみを参照する必要があります。 実行時にビューアのロジックによってダウンロードされる可能性のあるWebページコード内の追加のJavaScriptファイルは、参照しないでください。 特に、ビューアによって`/s7viewers`コンテキストパスから読み込まれたHTML5 SDK `Utils.js`ライブラリを直接参照しないでください（いわゆる統合SDK `include`）。 理由は、`Utils.js`や類似のランタイムビューアライブラリの場所は、ビューアのロジックによって完全に管理され、ビューアのリリースによって位置が変わるからです。 Adobeでは、セカンダリビューア`includes`の古いバージョンはサーバに保持されません。
>
>
>その結果、新しい製品バージョンがデプロイされると、ビューアが使用するセカンダリJavaScript `include`への直接参照をページに配置すると、将来ビューア機能が壊れます。

1. コンテナ`DIV`を定義します。

   ビューアを表示するページに空の`DIV`要素を追加します。 `DIV`要素のIDは、後でビューアのAPIに渡されるので、定義する必要があります。 DIVのサイズはCSSで指定します。

   プレースホルダー`DIV`は配置を指定する要素です。つまり、CSSの`position`プロパティを`relative`または`absolute`に設定します。

   次に、定義済みのプレースホルダー`DIV`要素の例を示します。

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアサイズの設定

   ビューアの静的サイズを設定するには、`.s7interactiveimage`最上位CSSクラスに対して絶対単位で宣言するか、`stagesize`修飾子を使用します。

   サイズ調整は、HTMLページ上またはカスタムビューアのCSSファイルで直接設定できます。その後、CSSファイルをAEM Assetsのオンデマンドでビューアプリセットレコードに割り当てるか、`style`コマンドを使用して明示的に渡します。

   CSSでのビューアのスタイル設定について詳しくは、[ビデオ](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)を参照してください。

   以下は、HTMLページで静的ビューアサイズを定義する例です。

   ```
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   `stagesize`修飾子を、`params`コレクションを使用したビューア初期化コードで明示的に渡すことも、次のように、コマンドリファレンスの節で説明するようにAPI呼び出しとして渡すこともできます。

   ```
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   CSSベースのアプローチを推奨し、この例で使用します。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、`s7viewers.InteractiveImage`クラスのインスタンスを作成し、すべての設定情報をコンストラクターに渡して、ビューアインスタンスで`init()`メソッドを呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 最低でも、このオブジェクトには`containerId`フィールドが必要です。このフィールドには、ビューアのコンテナIDの名前と、ビューアでサポートされている設定パラメーターを含むネストされた`params` JSONオブジェクトが含まれています。 この場合、`params`オブジェクトには、`serverUrl`プロパティとして渡された画像サービングURLが少なくとも含まれ、最初のアセットが`asset`パラメーターとして含まれている必要があります。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、起動できます。

   ビューアのコードがIDでコンテナ要素を見つけられるように、ビューアのコンテナをDOMに追加することが重要です。 一部のブラウザーは、Webページの終わりまでDOMの構築を遅らせます。 互換性を最大にするには、 `BODY`終了タグの直前、または本文の`onload()`イベントで`init()`メソッドを呼び出します。

   同時に、コンテナ要素は、必ずしもまだWebページレイアウトの一部ではないはずです。 例えば、`display:none`スタイルを割り当てて非表示にすることができます。 この場合、Webページでコンテナ要素がレイアウトに戻るまで、ビューアの初期化プロセスが遅れます。 この場合、ビューアの読み込みが自動的に再開されます。

   以下の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して`init()`メソッドを呼び出します。 この例では、 `interactiveImage`がビューアインスタンスであると仮定しています。`s7viewer`はプレースホルダー`DIV`の名前です。`http://aodmarketingna.assetsadobe.com/is/image`は画像サービングのURLで、`/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.`はアセットです。

   ```
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

   次のコードは、固定サイズのビデオ画像ビューアを埋め込んだ簡単なWebページの例です。

   ```
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

**高さ無制限のレスポンシブデザイン埋め込み**

レスポンシブデザイン埋め込みでは、Webページには通常、ビューアのコンテナ`DIV`の実行時のサイズを指示する柔軟なレイアウトが指定されています。 次の例では、Webページでビューアのコンテナ`DIV`がWebブラウザーのウィンドウサイズの40%を占めることを許可しているとします。 高さは無制限のままです WebページのHTMLコードは次のようになります。

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
1. コンテナ`DIV`を定義します。
1. ビューアを作成し、初期化する。

上記の手順は、固定サイズ埋め込みの場合と同じです。 コンテナ`DIV`を既存の`"holder"` `DIV`に追加します。 次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化すること、ビューアの縦横比がアセットと一致することに注意してください。

```
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

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用例を示します。

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html)

**幅と高さが定義されたフレキシブルサイズ埋め込み**

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

残りの埋め込み手順は、高さ無制限のレスポンシブ埋め込みで使用する手順と同じです。 結果の例は次のようになります。

```
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

**セッターベースのAPIを使用した埋め込み**

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合は、コンストラクターにパラメーターは不要です。設定パラメーターは、 `setContainerId()`、 `setParam()`および`setAsset()`の各APIメソッドを別々のJavaScript呼び出しで使用して指定します。

次の例は、固定サイズ埋め込みをセッターベースのAPIと共に使用する方法を示しています。

```
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
