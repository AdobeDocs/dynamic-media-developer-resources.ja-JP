---
description: インタラクティブ画像ビューアは、ズーム可能でない単一の画像を表示するビューアで、クリック可能なホットスポットがあります。 このビューアの目的は、「買い物かごのバナー」エクスペリエンスを実装することです。 つまり、バナー画像の上にホットスポットを選択して、Webサイト上のクイック表示または製品の詳細ページにリダイレクトされます。 デスクトップおよびモバイルデバイスで動作するように設計されています。
seo-description: インタラクティブ画像ビューアは、ズーム可能でない単一の画像を表示するビューアで、クリック可能なホットスポットがあります。 このビューアの目的は、「買い物かごのバナー」エクスペリエンスを実装することです。 つまり、バナー画像の上にホットスポットを選択して、Webサイト上のクイック表示または製品の詳細ページにリダイレクトされます。 デスクトップおよびモバイルデバイスで動作するように設計されています。
seo-title: インタラクティブ画像
solution: Experience Manager
title: インタラクティブ画像
topic: Dynamic media
uuid: 18b7a0c3-c047-4ce1-8920-1d8ebc1ab60e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '1806'
ht-degree: 0%

---


# インタラクティブ画像{#interactive-image}

インタラクティブ画像ビューアは、ズーム可能でない単一の画像を表示するビューアで、クリック可能なホットスポットがあります。 このビューアの目的は、「買い物かごのバナー」エクスペリエンスを実装することです。 つまり、バナー画像の上にホットスポットを選択して、Webサイト上のクイック表示または製品の詳細ページにリダイレクトされます。 デスクトップおよびモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR（画像レンダリング）またはUGC（ユーザ生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアタイプ508

## デモURL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html)

## システム要件 {#section-b7270cc4290043399681dc504f043609}

[必要システム構成](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

## インタラクティブ画像ビューアの使用{#section-e6c68406ecdc4de781df182bbd8088b4}

インタラクティブ画像ビューアは、メインのJavaScriptファイルと、ビューアによって実行時にダウンロードされるヘルパーファイルのセット（このビューアで使用されるすべてのビューアSDKコンポーネントが含まれる1つのJavaScriptインクルード）です。

インタラクティブ画像ビューアは、ドキュメントに記載されているAPIを使用してターゲットのWebページに統合される埋め込みモードでのみ使用できます。

設定とスキン表示は、このヘルプで説明する他のビューアと同様です。 スキン表示はすべて、カスタムCSSを使用して適用します。

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)と[すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください。

## インタラクティブ画像ビューアの操作{#section-642e66ca38cd4032992840ec6c0b0cd2}

ビデオ画像ビューアでサポートされているインタラクションは、デスクトップシステムではホットスポットアクティベーションです。 このアクティベーションは、1回のタップでクリック時とタッチデバイス時に発生します。

ビューアは完全にキーボードでアクセスできます。

[キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## インタラクティブ画像ビューアの埋め込み{#section-6bb5d3c502544ad18a58eafe12a13435}

インタラクティブ画像ビューアは、ホスティングページに埋め込まれるように設計されています。 このようなWebページは静的レイアウトである場合や、「レスポンシブ」で、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わる場合があります。

これらのニーズに対応するために、ビューアでは、主に次の2つの操作モードがサポートされています。固定サイズ埋め込みとレスポンシブ埋め込み

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存のWebページに追加されます。 このWebページには、Viewerに関連しない顧客コンテンツが既に含まれている場合があります。 ビューアは通常、Webページの一部のスペースのみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、デバイスの種類に従ってレイアウトを自動調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 静的レイアウトのWebページには、これが最適です。

レスポンシブデザイン埋め込みは、コンテナ`DIV`のサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定しています。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナのサイズ変更の方法`DIV`によって、ビューアの動作が異なります。 Webページでコンテナ`DIV`の幅のみが設定され、高さは無制限のままの場合、ビューアでは、使用するアセットの縦横比に従って高さが自動的に選択されます。 この機能により、両側のパディングなしで、アセットは表示にぴったりと収まります。 この使用例は、Bootstrap、FoundationなどのレスポンシブWebデザインレイアウトフレームワークを使用するWebページで最も一般的です。

それ以外の場合は、Webページでビューアのコンテナ`DIV`の幅と高さの両方が設定されている場合、ビューアはその領域だけを占めます。 また、Webページのレイアウトのサイズに従います。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合があります。

**固定サイズ埋め込み**

ビューアは、次の操作を行ってWebページに追加します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナ`DIV`を定義しています。
1. ビューアのサイズを設定する。
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにスクリプトタグを追加する必要があります。 ビューアのAPIを使用するには、[!DNL InterativeImage.js]を必ず含めます。 [!DNL InteractiveImage.js]ファイルは、次に示すように、IS-Viewersの標準のデプロイ先の[!DNL html5/js/]サブフォルダーにあります。

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

ビューアがAdobeのDynamic Mediaクラシックサーバの1つにデプロイされ、同じドメインから供給されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobeDynamic Mediaクラシックサーバの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScript `include`ファイルのみを参照してください。 Webページコード内で、ビューアのロジックによって実行時にダウンロードされる可能性のある追加のJavaScriptファイルは、参照しないでください。 特に、ビューアによって読み込まれたHTML5 SDK `Utils.js`ライブラリを`/s7viewers`コンテキストパスから直接参照しないでください（いわゆる統合SDK `include`）。 理由は、`Utils.js`や類似のランタイムビューアライブラリの場所がビューアのロジックで完全に管理され、ビューアのリリース間で場所が変化するからです。 Adobeでは、古いバージョンのセカンダリビューア`includes`はサーバに保持されません。
>
>
>その結果、新しい製品バージョンがデプロイされる際に、ビューアが使用する任意のセカンダリJavaScript `include`への直接参照をページ上に置くと、ビューアの機能が将来的に機能しなくなります。

1. コンテナ`DIV`を定義しています。

   ビューア追加を表示するページの空の`DIV`要素。 `DIV`要素は、IDが定義されている必要があります。このIDが後でビューアのAPIに渡されます。 DIVのサイズはCSSで指定します。

   プレースホルダー`DIV`は位置固定要素です。つまり、`position` CSSプロパティは`relative`または`absolute`に設定されます。

   次に、定義済みのプレースホルダー`DIV`要素の例を示します。

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアのサイズの設定

   ビューアの静的サイズを設定するには、最上位CSSクラスに対して絶対単位で`.s7interactiveimage`宣言するか、`stagesize`修飾子を使用します。

   サイズ調整は、CSS内で直接HTMLページまたはカスタムビューアのCSSファイルに配置できます。その後、カスタムビューアのCSSファイルが、AEM Assetsのオンデマンドでビューアプリセットレコードに割り当てられるか、`style`コマンドを使用して明示的に渡されます。

   CSSでのビューアのスタイル設定について詳しくは、[ビデオ](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)を参照してください。

   以下は、HTMLページで静的ビューアサイズを定義する例です。

   ```
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   `stagesize`修飾子を、`params`コレクションを使用してビューア初期化コードと共に明示的に渡すか、次に示すように、コマンドリファレンスの節で説明するAPI呼び出しとして渡すことができます。

   ```
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   CSSベースのアプローチを推奨し、この例では使用します。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、`s7viewers.InteractiveImage`クラスのインスタンスを作成し、すべての設定情報をコンストラクターに渡して、ビューアインスタンスで`init()`メソッドを呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 最低でも、このオブジェクトには`containerId`フィールドが存在し、ビューアのコンテナIDの名前と、ビューアでサポートされている設定パラメーターを含むネストされた`params` JSONオブジェクトが含まれている必要があります。 この場合、`params`オブジェクトには、`serverUrl`プロパティとして渡された画像サービングURLが最低限必要で、初期アセットは`asset`パラメーターとして含まれている必要があります。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、開始できます。

   ビューアのコンテナをDOMに追加して、ビューアのコードがIDでコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Webページが終わるまでDOMの構築が遅れます。 互換性を最大にするには、`init()`メソッドを終了`BODY`タグの直前、または本文`onload()`イベントで呼び出します。

   同時に、コンテナ要素がまだWebページレイアウトの一部である必要はありません。 例えば、`display:none`スタイルを割り当てて非表示にすることができます。 この場合、Webページからコンテナ要素がレイアウトに戻る瞬間まで、ビューアは初期化プロセスを遅延します。 この場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、`init()`メソッドを呼び出します。 この例では、`interactiveImage`をビューアインスタンスと仮定しています。`s7viewer`はプレースホルダー`DIV`の名前です。`http://aodmarketingna.assetsadobe.com/is/image`は画像サービングのURL、`/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.`はアセットです。

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

レスポンシブデザイン埋め込みでは、Webページには通常、ビューアのコンテナ`DIV`の実行時のサイズを指示する柔軟なレイアウトが指定されています。 次の例では、Webページでビューアのコンテナ`DIV`がWebブラウザーのウィンドウサイズの40%を占めることを許可しているとします。 高さは無制限のままです。 WebページのHTMLコードは次のようになります。

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

このようなページへのビューアの追加手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、ビューアサイズを明示的に定義する必要がないことです。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナ`DIV`を定義しています。
1. ビューアを作成し、初期化する。

上記の手順はすべて、固定サイズ埋め込みの場合と同じです。 追加既存の`"holder"` `DIV`に対するコンテナ`DIV`。 次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化すること、ビューアの縦横比がアセットと一致することに注目してください。

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

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用方法を説明しています。

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html)

**幅と高さが定義されたフレキシブルサイズ埋め込み**

幅と高さが定義されたフレキシブルサイズ埋め込みの場合、Webページのスタイルは異なります。 `"holder"` DIVに両方のサイズを提供し、ブラウザーウィンドウの中央に配置します。 また、Webページでは、`HTML`要素と`BODY`要素のサイズを100%に設定します。

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

残りの埋め込み手順は、高さ無制限のレスポンシブ埋め込みで使用した手順と同じです。 結果の例を次に示します。

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

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合、コンストラクターにパラメーターは不要です。設定パラメーターは、`setContainerId()`、`setParam()`および`setAsset()`の各APIメソッドを別々のJavaScript呼び出しで使用して指定します。

以下の例は、固定サイズ埋め込みとセッターベースのAPIを使用する場合を説明しています。

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

