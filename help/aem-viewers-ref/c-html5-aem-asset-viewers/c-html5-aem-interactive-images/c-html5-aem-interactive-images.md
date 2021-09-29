---
title: インタラクティブ画像
description: インタラクティブ画像ビューアは、クリック可能なホットスポットを含む、ズーム不可能な 1 つの画像を表示するビューアです。 このビューアの目的は、「ショッパブルバナー」エクスペリエンスを実装することです。 つまり、ユーザーはバナー画像の上のホットスポットを選択して、Web サイトのクイックビューまたは製品の詳細ページにリダイレクトされます。 デスクトップおよびモバイルデバイスで動作するように設計されています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: c7089ecd-6ff3-4fe9-9ee7-3b48c9201558
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '1720'
ht-degree: 0%

---

# インタラクティブ画像{#interactive-image}

インタラクティブ画像ビューアは、クリック可能なホットスポットを含む、ズーム不可能な 1 つの画像を表示するビューアです。 このビューアの目的は、「ショッパブルバナー」エクスペリエンスを実装することです。 つまり、ユーザーはバナー画像の上のホットスポットを選択して、Web サイトのクイックビューまたは製品の詳細ページにリダイレクトされます。 デスクトップおよびモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR（画像レンダリング）または UGC（ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアタイプは 508。

## デモ URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html)

## システム要件 {#section-b7270cc4290043399681dc504f043609}

[ 必要システム構成 ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842) を参照してください。

## インタラクティブ画像ビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

インタラクティブ画像ビューアは、メインの JavaScript ファイルと、ヘルパーファイルのセット（この特定のビューア、アセット、CSS で使用されるすべてのビューア SDK コンポーネントを含む単一の JavaScript インクルード）です。

インタラクティブ画像ビューアは、埋め込みモードでのみ使用でき、ドキュメントに記載されている API を使用してターゲット Web ページに統合されます。

設定とスキン表示は、このヘルプで説明する他のビューアと同様です。 スキン表示はすべて、カスタム CSS を使用して適用できます。

[ すべてのビューアに共通のコマンドリファレンス — 設定属性 ](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [ すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) を参照してください。

## インタラクティブ画像ビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

ビデオ画像ビューアでサポートされているインタラクションは、デスクトップシステムでのホットスポットのアクティベーションです。 このアクティベーションは、1 回のタップでのクリックおよびタッチデバイスで発生します。

ビューアが完全にキーボードでアクセス可能。

[ キーボードのアクセシビリティとナビゲーション ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861) を参照してください。

## インタラクティブ画像ビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

インタラクティブ画像ビューアは、ホスティングページに埋め込まれます。 このような Web ページは、静的なレイアウトである場合や、「レスポンシブ」で、デバイスごと、ブラウザーウィンドウのサイズごとに表示が異なる場合があります。

これらのニーズに対応するために、ビューアでは次の 2 つの主要な操作モードがサポートされています。固定サイズ埋め込みとレスポンシブ埋め込み。

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存の Web ページに追加されます。 この Web ページには、閲覧者とは関係のない顧客コンテンツが既に含まれている場合があります。 ビューアは通常、Web ページの一部の領域のみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けの Web ページ、およびデバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 この方法は、静的レイアウトの Web ページに最適です。

レスポンシブデザイン埋め込みは、コンテナ `DIV` のサイズ変更に対応して実行時にビューアのサイズを変更する必要がある場合を想定しています。 最も一般的な使用例は、柔軟なページレイアウトを使用する Web ページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Web ページによるコンテナ `DIV` のサイズ変更の方法によって、ビューアの動作が異なります。 Web ページでコンテナ `DIV` の幅のみが設定され、高さは無制限のままの場合、ビューアでは、使用するアセットの縦横比に応じて高さが自動的に選択されます。 この機能により、両側のパディングなしで、アセットが表示にぴったりと収まります。 この使用例は、Bootstrapや基盤などのレスポンシブ Web デザインレイアウトフレームワークを使用する Web ページで最も一般的です。

それ以外の場合、Web ページでビューアのコンテナ `DIV` の幅と高さの両方が設定されている場合、ビューアはその領域だけを占めます。 また、Web ページのレイアウトで指定されているサイズに従います。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイが Web ブラウザーのウィンドウサイズに従ってサイズ設定される場合があります。

**固定サイズ埋め込み**

ビューアを Web ページに追加するには、次の手順を実行します。

1. ビューアの JavaScript ファイルを Web ページに追加します。
1. コンテナ `DIV` を定義します。
1. ビューアのサイズを設定します。
1. ビューアを作成して初期化する

1. ビューアの JavaScript ファイルを Web ページに追加します。

   ビューアを作成するには、HTML の head にスクリプトタグを追加する必要があります。 ビューアの API を使用する前に、必ず [!DNL InterativeImage.js] を含めてください。 [!DNL InteractiveImage.js] ファイルは、次に示すように、標準の IS-Viewers デプロイメントの [!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

ビューアがAdobeのDynamic Media Classic サーバの 1 つにデプロイされ、同じドメインから提供されている場合は、相対パスを使用できます。 それ以外の場合は、IS ビューアがインストールされているAdobeDynamic Media Classic サーバーの 1 つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>ページでは、メインビューアの JavaScript `include` ファイルのみを参照します。 実行時にビューアのロジックによってダウンロードされる可能性のある Web ページコード内の追加の JavaScript ファイルは参照しないでください。 特に、`/s7viewers` コンテキストパス（いわゆる統合 SDK `include`）からビューアによって読み込まれた HTML5 SDK `Utils.js` ライブラリを直接参照しないでください。 この理由は、`Utils.js` や類似のランタイムビューアライブラリの場所がビューアのロジックによって完全に管理され、ビューアのリリース間で位置が変わるからです。 Adobeは、古いバージョンのセカンダリビューア `includes` をサーバ上に保持しません。
>
>
>その結果、新しい製品バージョンがデプロイされると、ビューアが使用するセカンダリ JavaScript `include` への直接参照をページに配置すると、将来ビューア機能が壊れます。

1. コンテナ `DIV` を定義します。

   ビューアを表示するページに空の `DIV` 要素を追加します。 `DIV` 要素の ID は、後でビューアの API に渡されるので、定義する必要があります。 DIV のサイズは CSS で指定します。

   プレースホルダー `DIV` は配置する要素です。つまり、CSS の `position` プロパティを `relative` または `absolute` に設定します。

   次に、定義済みのプレースホルダー `DIV` 要素の例を示します。

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアサイズの設定

   ビューアの静的サイズを設定するには、最上位 CSS クラスに対して絶対単位で宣言するか、`.s7interactiveimage` 修飾子を使用します。`stagesize`

   サイズ調整は HTML ページで CSS に直接適用できます。 または、カスタムビューアの CSS ファイルにサイズ調整を挿入し、その後、Adobe Experience Manager Assets のビューアプリセットレコード（オンデマンド）に割り当てるか、`style` コマンドを使用して明示的に渡すことができます。

   CSS でのビューアのスタイル設定について詳しくは、[ ビデオ ](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) を参照してください。

   以下は、HTML ページで静的ビューアサイズを定義する例です。

   ```
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   `stagesize` 修飾子を、`params` コレクションを使用したビューア初期化コードで明示的に渡すことも、次のように、コマンドリファレンスの節で説明するように API 呼び出しとして渡すこともできます。

   ```
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   CSS ベースのアプローチを推奨し、この例で使用します。

1. ビューアを作成して初期化する

   上記の手順を完了したら、`s7viewers.InteractiveImage` クラスのインスタンスを作成し、すべての設定情報をコンストラクターに渡して、ビューアインスタンスで `init()` メソッドを呼び出します。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 最低でも、このオブジェクトには `containerId` フィールドが必要です。このフィールドには、ビューアのコンテナ ID の名前と、ビューアでサポートされている設定パラメーターを含むネストされた `params` JSON オブジェクトが含まれています。 この場合、 `params` オブジェクトには、少なくとも `serverUrl` プロパティとして渡された画像サービング URL が含まれ、最初のアセットが `asset` パラメーターとして含まれている必要があります。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成し、起動できます。

   ビューアのコンテナを DOM に追加して、ビューアのコードが ID でコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Web ページの末尾まで DOM の構築が遅れます。 互換性を最大にするには、 `BODY` 終了タグの直前、または本文の `onload()` イベントで `init()` メソッドを呼び出します。

   同時に、コンテナ要素は、まだ Web ページレイアウトの一部ではない必要があります。 例えば、`display:none` スタイルを割り当てて非表示にすることができます。 この場合、Web ページでコンテナ要素がレイアウトに戻るまで、ビューアは初期化プロセスを遅延します。 このイベントが発生すると、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、 `init()` メソッドを呼び出します。 この例では、 `interactiveImage` がビューアインスタンスであると仮定しています。`s7viewer` はプレースホルダー `DIV` の名前です。`http://aodmarketingna.assetsadobe.com/is/image` は画像サービングの URL で、`/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` はアセットです。

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

   次のコードは、固定サイズのビデオ画像ビューアを埋め込んだ簡単な Web ページの例です。

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

レスポンシブデザイン埋め込みでは、Web ページには通常、ビューアのコンテナ `DIV` の実行時のサイズを指示する柔軟なレイアウトが指定されています。 次の例では、Web ページでビューアのコンテナ `DIV` が Web ブラウザーのウィンドウサイズの 40%を占めることを許可しているとします。 そして、その高さは無制限のままです。 Web ページの HTML コードは次のようになります。

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

このようなページにビューアを追加する手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、ビューアのサイズを明示的に定義する必要がないことです。

1. ビューアの JavaScript ファイルを Web ページに追加します。
1. コンテナ `DIV` を定義します。
1. ビューアを作成して初期化する

上記の手順は、固定サイズ埋め込みの場合と同じです。 コンテナ `DIV` を既存の `"holder"` `DIV` に追加します。 次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化し、ビューアの縦横比がアセットと一致していることに注意してください。

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

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用方法を説明します。

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html)

**幅と高さが定義されたフレキシブルサイズ埋め込み**

幅と高さが定義されたフレキシブルサイズ埋め込みがある場合、Web ページのスタイル設定は異なります。 `"holder"` DIV に両方のサイズを提供し、ブラウザーウィンドウの中央に配置します。 また、Web ページでは、`HTML` 要素と `BODY` 要素のサイズを 100%に設定します。

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

残りの埋め込み手順は、高さ無制限のレスポンシブ埋め込みに使用した手順と同じです。 結果の例を次に示します。

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

**セッターベースの API を使用した埋め込み**

JSON ベースの初期化を使用する代わりに、セッターベースの API と no-args コンストラクターを使用できます。 この API を使用する場合は、コンストラクターにパラメーターは不要です。設定パラメーターは、 `setContainerId()` 、 `setParam()` および `setAsset()` の各 API メソッドを別々の JavaScript 呼び出しで使用して指定します。

次の例は、固定サイズ埋め込みをセッターベースの API と共に使用する方法を示しています。

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
