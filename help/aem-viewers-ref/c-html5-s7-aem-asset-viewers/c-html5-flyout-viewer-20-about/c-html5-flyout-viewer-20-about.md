---
title: フライアウト
description: Flyout ビューアは、画像ビューアです。 ユーザーがアクティブにするズームされたバージョンを含む静的画像がフライアウト表示に表示されます。 このビューアは画像セットを操作し、スウォッチを使用してナビゲーションを行います。 デスクトップおよびモバイルデバイスで動作するように設計されています。
keywords: 応答
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '1941'
ht-degree: 0%

---

# フライアウト{#flyout}

Flyout ビューアは、画像ビューアです。 ユーザーがアクティブにするズームされたバージョンを含む静的画像がフライアウト表示に表示されます。 このビューアは画像セットを操作し、スウォッチを使用してナビゲーションを行います。 デスクトップおよびモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR （画像レンダリング）または UGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアのタイプは 504 です。

[&#x200B; システム要件と前提条件 &#x200B;](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842) を参照してください。

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Flyout ビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

Flyout ビューアは、実行時にビューアによってダウンロードされるメインのJavaScript ファイルと一連のヘルパーファイル（1 つのJavaScriptに、この特定のビューア、アセット、CSS で使用されるすべてのビューア SDK コンポーネントが含まれます）を表します

Flyout ビューアは、埋め込み用途のみを目的としています。つまり、ドキュメントに記載された API を使用して web ページに統合されます。 Flyout ビューアでは、実稼動用の Web ページは使用できません。

設定とスキニングは、他のビューアと同様です。 カスタム CSS を使用してスキニングを適用できます。

[&#x200B; すべてのビューアに共通のコマンドリファレンス – 設定属性 &#x200B;](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [&#x200B; すべてのビューアに共通のコマンドリファレンス - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) を参照してください

## Flyout ビューアの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

フライアウトビューアは、他のモバイルアプリケーションで一般的なシングルタッチジェスチャとマルチタッチジェスチャをサポートしています。

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
   <td colname="col2"> <p> フライアウト ビューをアクティブにするか、メイン ズーム レベルとサブ ズーム レベルの間を変更します。 </p> </td> 
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

詳しくは [&#x200B; キーボードアクセシビリティとナビゲーション &#x200B;](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861) を参照してください。

## Flyout ビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

Web ページによって、ビューアの動作に対するニーズは異なります。 Web ページは、静的なページレイアウトを持っている場合や、異なるデバイスや異なるブラウザーウィンドウサイズに異なる表示を行うレスポンシブデザインを使用している場合があります。 これらのニーズに対応するために、ビューアでは 2 つの主要な操作モード（固定サイズの埋め込みとレスポンシブデザインの埋め込み）をサポートしています。

固定サイズ埋め込みモードは、ビューアの初回読み込み後にサイズが変更されない場合に使用されます。 この選択は、静的なページレイアウトを持つ web ページに最適です。

レスポンシブデザインの埋め込みモードでは、コンテナコンポー `DIV` ントのサイズ変更に応じて、実行時にビューアのサイズを変更する必要があることを前提としています。 最も一般的なユースケースは、柔軟なページレイアウトを使用する web ページにビューアを追加する場合です。

Flyout ビューアでレスポンシブデザインの埋め込みモードを使用する場合は、`imagereload` パラメーターを使用して、メインビュー画像の明示的なブレークポイントを指定してください。 Web ページの CSS に記述されているビューア幅のブレークポイントを使用して、ブレークポイントを一致させるのが理想です。

レスポンシブデザインの埋め込みモードでは、web ページコンテナの `DIV` ージのサイズがどのように調整されるかによってビューアの動作が異なります。 Web ページでコンテナ `DIV` の幅のみが設定され、高さが制限されない場合、ビューアは、使用されるアセットの縦横比に応じて自動的に高さを選択します。 つまり、アセットは側面にパディングを入れずに、ビューに完全に収まります。 この特定のユースケースは、Bootstrapや Foundation などのレスポンシブデザインレイアウトフレームワークを使用する web ページで最も一般的です。

Web ページでビューアのコンテナ `DIV` の幅と高さの両方が設定されている場合、ビューアはその領域のみを埋め、web ページレイアウトで提供されるサイズに従います。 良いユースケースの例は、ビューアをモーダルオーバーレイに埋め込む場合です。この場合、オーバーレイは web ブラウザーのウィンドウサイズに従ってサイズが調整されます。

**固定サイズ埋め込み**

Web ページにビューアを追加するには、次の手順を実行します。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ `DIV` を定義します。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. Web ページへのビューアJavaScript ファイルの追加

   ビューアを作成するには、HTMLのヘッドにスクリプトタグを追加する必要があります。 ビューア API を使用する前に、必ず `FlyoutViewer.js` を含めてください。 `FlyoutViewer.js` は、標準の IS-Viewers デプロイメントの次の [!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

ビューアがAdobe Dynamic Media サーバーのいずれかにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-Viewers がインストールされているAdobe Dynamic Media サーバーのいずれかに対するフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScript `include` ファイルのみを参照します。 実行時にビューアのロジックによってダウンロードされる可能性がある web ページコード内の追加のJavaScript ファイルを参照しないでください。 特に、ビューアによって読み込まれるHTML5 SDK `Utils.js` ライブラリを、コンテキストパス（いわゆる統合SDK `/s7viewers`）から直接参照 `include` ないでください。 これは、`Utils.js` や類似のランタイム・ビューア・ライブラリの場所はビューアのロジックによって完全に管理され、ビューア・リリース間で場所が変更されるためです。 Adobeは、古いバージョンのセカンダリビューア `includes` をサーバーに保持しません。
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

   外部ビューアの境界をそのままにするには、最上位の CSS クラス `.s7flyoutviewer` サイズを絶対単位で定義します。 CSS のサイズ設定は、HTML ページに直接配置するか、カスタムビューア CSS ファイルに配置することができます。また、後でDynamic Media Classicのビューアプリセットレコードに割り当てたり、style コマンドを使用して明示的に渡すこともできます。

   CSS を使用したビューアのスタイル設定について詳しくは、[Flyout ビューアのカスタマイズ &#x200B;](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) を参照してください。

   HTML ページで静的な外部ビューアのサイズを定義する例を次に示します。

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

<!-- You can see the behavior with a fixed outer viewer area on the following sample page. Notice that when you switch between sets, the outer viewer size does not change:-->

<!--

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html?lang=ja](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html?lang=ja)

-->

メインビューの寸法を静的にするには、CSS セレクターを使用して、内部の `Container` SDK コンポーネントのビューアサイズ `.s7flyoutviewer .s7container` 絶対単位で定義します。 さらに、デフォルトのビューア CSS で `.s7flyoutviewer` の最上位レベルの CSS クラスに定義された固定サイズを `auto` に設定して上書きする必要があります。

次に、アセットを切り替えるときにメイン表示領域のサイズが変わらないように、内部の `Container` SDK コンポーネントのビューアサイズを定義する例を示します。

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

<!-- The following sample page shows viewer behavior with a fixed main view size. Notice that when you switch between sets, the main view remains static and the web page content moves vertically:-->

<!--

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html?lang=ja](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html?lang=ja)

-->

また、デフォルトのビューア CSS では、すぐに使用できる外部領域のサイズが固定されています。

1. ビューアの作成と初期化。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報 `s7viewers.FlyoutViewer` そのコンストラクターに渡して、ビューアインスタンスのメソッド `init()` 呼び出します。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトにはビューアコンテナ ID の名前を保持する `containerId` フィールドと、ビューアがサポートす `params` 設定パラメーターを含むネストされた JSON オブジェクトが必要です。 この場合、`params` オブジェクトには、少なくとも画像サービング URL がプロパティとして渡され、初期アセット `serverUrl` パラメーターとして渡されてい `asset` 必要があります。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成して開始できます。

   ビューアコードが ID でコンテナ要素を見つけられるように、ビューアコンテナを DOM に追加することが重要です。 一部のブラウザーでは、web ページの最後まで DOM の構築が遅れます。 互換性を最大限に高めるには、終了 `init()` タグの直前または body `BODY` イベントで `onload()` メソッドを呼び出します。

   同時に、コンテナ要素は、まだ web ページレイアウトの一部である必要はありません。 例えば、割り当てられたスタイルを使用して非表示 `display:none` する場合があります。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで、初期化プロセスを遅延します。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

   以下に、ビューアインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡して、`init()` メソッドを呼び出す例を示します。 この例では、`flyoutViewer` はビューアインスタンス、`s7viewer` はプレースホルダー `DIV` の名前、`http://s7d1.scene7.com/is/image/` は画像サービング URL、`Scene7SharedAssets/ImageSet-Views-Sample` はアセットであると仮定します。

   ```html {.line-numbers}
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

   次のコードは、Flyout ビューアを固定サイズで埋め込む単純な web ページの完全な例です。

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

## 高さが制限されないレスポンシブデザインの埋め込み {#section-056cb574713c4d07be6d07cf3c598839}

レスポンシブデザインの埋め込みを使用すると、通常、web ページには、ビューアのコンテナ `DIV` ージの実行時サイズを指定する何らかの柔軟なレイアウトが配置されます。 次の例では、web ページで、ビューアのコンテナ `DIV` が web ブラウザーのウィンドウサイズの 40% を占め、高さは無制限であるとします。 Web ページのHTML コードは次のようになります。

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
* 絶対単位を使用して固定のビューアサイズを設定する代わりに、次のようにビューアの幅と高さを 100% に設定する CSS を使用します。

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

以下の例では、高さが制限されないレスポンシブデザインの埋め込みを使用した実際の使用例を示しています。

[&#x200B; ライブデモ &#x200B;](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--

[Alternate demo location](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=ja)

-->

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
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```
