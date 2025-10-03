---
title: ズーム
description: ズームビューアは、ズーム可能な画像を表示する画像ビューアです。 このビューアは画像セットを操作し、スウォッチを使用してナビゲーションを行います。 ズームツール、フルスクリーンサポート、スウォッチ、オプションの「閉じる」ボタンがあります。 デスクトップおよびモバイルデバイスで動作するように設計されています。
keywords: 応答
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '2278'
ht-degree: 0%

---

# ズーム{#zoom}

ズームビューアは、ズーム可能な画像を表示する画像ビューアです。 このビューアは画像セットを操作し、スウォッチを使用してナビゲーションを行います。 ズームツール、フルスクリーンサポート、スウォッチ、オプションの「閉じる」ボタンがあります。 デスクトップおよびモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR （画像レンダリング）または UGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアのタイプは 502 です。

[&#x200B; システム要件と前提条件 &#x200B;](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842) を参照してください。

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## ズームビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

ズームビューアは、実行時にビューアによってダウンロードされるメインのJavaScript ファイルと一連のヘルパーファイル（この特定のビューア、アセット、CSS で使用されるすべてのビューア SDK コンポーネントに含まれる 1 つのJavaScriptに相当します）を表します。

ズームビューアは、IS-Viewers に付属している実稼動用HTML ページを使用したポップアップモードか、埋め込みモードで使用できます。この場合、ドキュメント化された API を使用して対象の web ページに統合されます。

設定とスキニングは、他のビューアと同様です。 すべてのスキニングは、カスタム CSS を使用して行います。

[&#x200B; すべてのビューアに共通のコマンドリファレンス – 設定属性 &#x200B;](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [&#x200B; すべてのビューアに共通のコマンドリファレンス - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) を参照してください

## ズームビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

ズームビューアでは、他のモバイルアプリケーションに共通する次のタッチジェスチャーをサポートしています。 ビューアがユーザーのスワイプジェスチャーを処理できない場合は、イベントを web ブラウザーに転送して、ネイティブページのスクロールを実行します。 このような機能により、ビューアがデバイスの画面領域のほとんどを占めている場合でも、ユーザーはページ内を移動できます。

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
   <td colname="col2"> <p> スウォッチの新しいサムネールを選択します。 メインビューでは、ユーザーインターフェイス要素が表示または非表示になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ダブルタップ </p> </td> 
   <td colname="col2"> <p> 最大の倍率に達するまで 1 レベルでズームします。 次にダブルタップのジェスチャーを行うと、ビューアは最初の表示状態にリセットされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ピンチ </p> </td> 
   <td colname="col2"> <p>ズームインまたはズームアウトします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> スウォッチバーのスウォッチのリストをスクロールします。 </p> <p> 画像がリセット状態で、<span class="codeph"> frametransition </span> パラメーターがスライドに設定されている場合、アセットはスライドアニメーションと共に変更されます。 他の <span class="codeph"> フレーム遷移 </span> モードの場合、ジェスチャはネイティブのページスクロールを実行します。 </p> <p> 画像がズームインされると、画像は水平方向に移動します。 画像がビューの端に移動され、同じ方向にスワイプが実行されると、ジェスチャはネイティブページのスクロールを実行します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直スワイプ </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態の場合、ジェスチャーはネイティブページのスクロールを実行します。 </p> <p> 画像がズームインされると、画像が垂直方向に移動します。 画像がビューの端に移動され、同じ方向にスワイプが実行されると、ジェスチャはネイティブページスクロールを実行します。 </p> <p> スウォッチ領域内でジェスチャーを行うと、ネイティブページのスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビューアは、タッチスクリーンとマウスを備えた Windows デバイスでのタッチ入力とマウス入力の両方をサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11、Edgeの web ブラウザーのみに制限されます。

このビューアは完全にキーボードでアクセス可能です。

詳しくは [&#x200B; キーボードアクセシビリティとナビゲーション &#x200B;](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861) を参照してください。

## ズームビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

Web ページによって、ビューアの動作に対するニーズは異なります。 選択するとビューアが別のブラウザーウィンドウで開くリンクが、web ページに表示される場合があります。 それ以外の場合は、ビューアをホスティングページに直接埋め込む必要があります。 後者の場合、web ページのレイアウトが静的であるか、異なるデバイスや異なるブラウザーウィンドウサイズに異なる表示を行うレスポンシブデザインが使用されている可能性があります。 これらのニーズに対応するために、ビューアでは 3 つの主要な操作モード（ポップアップ、固定サイズの埋め込み、レスポンシブデザインの埋め込み）をサポートしています。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別の web ブラウザーウィンドウまたはタブで開きます。 ブラウザーのウィンドウ領域全体を取得し、ブラウザーのサイズが変更された場合や、デバイスの向きが変更された場合に備えて調整されます。

このモードは、モバイルデバイスで最も一般的です。 Web ページは、JavaScript呼び出し、HTML要素 `window.open()` の適切な設定、またはその他の適切なメソッド `A` 使用して、ビューアを読み込みます。

ポップアップオペレーションモードには、標準のHTMLページを使用することをお勧めします。 標準提供のHTML ページは `ZoomViewer.html` と呼ばれ、標準の IS-Viewers デプロイメントの `html5/` サブフォルダーに次のように配置されています。

`<s7viewers_root>/html5/ZoomViewer.html`

カスタム CSS を適用して、ページの外観をカスタマイズします。

以下は、新しいウィンドウでビューアを開くHTML コードの例です。

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアが既存の web ページに追加されます。これには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 閲覧者は通常、Web ページの領域の一部のみを占有します。

主なユースケースは、デスクトップまたはタブレットデバイス向けの web ページと、デバイスタイプに応じて自動的にレイアウトを調整するレスポンシブデザインのページです。

固定サイズの埋め込みは、初回読み込み後にビューアのサイズが変更されない場合に使用されます。 このオプションは、静的なレイアウトの web ページに最適です。

レスポンシブデザインの埋め込みモードでは、コンテナビュー `DIV` ーのサイズが変更されるので、実行時にビューアのサイズを変更する必要があると想定します。 最も一般的なユースケースは、柔軟なレイアウトを使用する web ページにビューアを追加することです。

レスポンシブデザインの埋め込みモードでは、web ページのコンテナコンポー `DIV` ントのサイズがどのように調整されるかに応じて、ビューアの動作が異なります。 Web ページでコンテナ `DIV` の幅のみが設定され、高さが制限されない場合、ビューアは、使用されるアセットの縦横比に応じて自動的に高さを選択します。 このロジックにより、アセットがビューに完全に収まり、側面にパディングが表示されなくなります。 このユースケースは、Bootstrapや Foundation などのレスポンシブレイアウトフレームワークを使用する web ページで最も一般的です。

Web ページでビューアのコンテナ `DIV` の幅と高さの両方が設定されている場合、ビューアはその領域を埋め、web ページが提供するサイズに従います。 例えば、ビューアをモーダルオーバーレイに埋め込む場合、オーバーレイは web ブラウザーのウィンドウサイズに応じてサイズが変更されます。

## 固定サイズの埋め込み {#section-44f365e6c0dd40709467a459afa82a7f}

Web ページにビューアを追加するには、次の手順を実行します。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ DIV の定義。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. Web ページへのビューアJavaScript ファイルの追加

   ビューアを作成するには、HTMLのヘッドにスクリプトタグを追加する必要があります。 ビューア API を使用する前に、必ず [!DNL ZoomViewer.js] を含めてください。 [!DNL ZoomViewer.js] ファイルは、標準の IS-Viewers デプロイメントの [!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

ビューアがAdobe Dynamic Media Classic サーバーの 1 つにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-Viewers がインストールされているAdobe Dynamic Media Classic サーバーの 1 つへのフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
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

   定義されたプレースホルダー DIV 要素の例を以下に示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアサイズの設定。

   このビューアにはサムネールが表示されます。複数の項目セットを操作する場合、デスクトップシステムではサムネールがメインビューの下に配置されます。 同時に、ビューアでは API を使用して、実行時にメインアセットを入れ替え `setAsset()` ことができます。 開発者は、新しいアセットに項目が 1 つしかない場合に、ビューアが下部のサムネール領域を管理する方法を制御できます。 外側のビューアのサイズはそのままにして、メインビューの高さを上げてサムネール領域を占有することができます。 または、メインビューのサイズを静的に保ち、外側のビューア領域を折りたたんで、web ページコンテンツを上に移動したり、サムネールから残った無料の画面領域を使用したりできます。

   外側のビューアの境界をそのままにするには、`.s7zoomviewer` の最上位レベル CSS クラスのサイズを絶対単位で定義します。 CSS でのサイズ設定は、HTMLページに直接配置できます。 または、カスタムビューア CSS ファイルに入れて、後でDynamic Media Classicのビューアプリセットレコードに割り当てたり、style コマンドを使用して明示的に渡したりできます。

   CSS を使用したビューアのスタイル設定について詳しくは、[&#x200B; ズームビューアのカスタマイズ &#x200B;](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) を参照してください。

   HTML ページで静的な外部ビューアのサイズを定義する例を以下に示します。

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

<!-- You can see the behavior with a fixed outer viewer in the following example. Notice that when you switch between sets, the outer viewer size does not change: -->

<!--

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html?lang=ja](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html?lang=ja)

-->

メインビューの寸法を静的にするには、`Container` `.s7zoomviewer` CSS セレクターを使用するか、修飾子を使用して、内部の `.s7container` SDK コンポーネントのビューアサイズを絶対単位で定義 `stagesize` ます。

次に、アセットを切り替えるときにメイン表示領域のサイズが変わらないように、内部の `Container` SDK コンポーネントのビューアサイズを定義する例を示します。

```html {.line-numbers}
#s7viewer.s7zoomviewer .s7container { 
 width: 640px; 
 height: 480px; 
}
```

<!-- The following demo page shows the viewer behavior with a fixed main view size. Notice that when you switch between sets, the main view remains static and the web page content moves vertically. -->

<!--

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html?lang=ja](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html?lang=ja)

-->

`stagesize` 修飾子は、Dynamic Media Classicのビューアプリセットレコードで設定できます。 または、以下に示すように、`params` コレクションを使用して、または API 呼び出しとして、ビューア初期化コードを使用して明示的に渡すこともできます。

```html {.line-numbers}
 zoomViewer.setParam("stagesize", 
"640,480");
```

この例では、CSS ベースのアプローチをお勧めします。

1. ビューアの作成と初期化。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報 `s7viewers.ZoomViewer` そのコンストラクターに渡して、ビューアインスタンスのメソッド `init()` 呼び出します。

   設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには `containerId` ビューアコンテナ ID の名前を保持するフィールドと、ビューアがサポートする設定パラメーター `params` 含むネストされた JSON オブジェクトが必要です。 この場合、`params` オブジェクトには、少なくとも画像サービング URL がプロパティとして渡され、初期アセットがパラメーター `serverUrl` して渡されてい `asset` 必要があります。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成して開始できます。

   ビューアコードが ID でコンテナ要素を見つけられるように、ビューアコンテナを DOM に追加することが重要です。 一部のブラウザーでは、web ページの最後まで DOM の構築が遅れます。 互換性を最大限に高めるには、終了 `init()` タグの直前または body `BODY` イベントで `onload()` メソッドを呼び出します。

   同時に、コンテナ要素は、まだ web ページレイアウトの一部である必要はありません。 例えば、割り当てられたスタイルを使用して非表示 `display:none` する場合があります。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで、初期化プロセスを遅延します。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

   以下に、ビューアインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡して、`init()` メソッドを呼び出す例を示します。 この例では、`zoomViewer` がビューアインスタンス、`s7viewer` がプレースホルダー DIV の名前、`http://s7d1.scene7.com/is/image/` は画像サービング URL、`Scene7SharedAssets/ImageSet-Views-Sample` はアセットであると想定しています。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、ビデオビューアを固定サイズで埋め込む単純な web ページの完全な例です。

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
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

## 高さが制限されないレスポンシブデザインの埋め込み {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

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

このようなページにビューアを追加する手順は、固定サイズの埋め込みを行う手順と似ています。 唯一の違いは、ビューアのサイズを明示的に定義する必要がないことです。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ DIV の定義。
1. ビューアの作成と初期化。

上記の手順はすべて、固定サイズの埋め込みと同じです。 コンテナ DIV を既存の `"holder"` DIV に追加します。 次のコードは完全な例です。 ブラウザーのサイズを変更するとビューアのサイズがどのように変化するか、ビューアの縦横比がアセットとどのように一致するかを確認します。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
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

以下の例では、高さが制限されないレスポンシブデザインの埋め込みを使用した実際の使用例を示しています。

[&#x200B; ライブデモ &#x200B;](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## 幅と高さが定義された柔軟なサイズの埋め込み {#section-3674e6c032594441a6576b7fb1de6e64}

幅と高さが定義されたフレキシブルサイズの埋め込みがある場合、web ページのスタイル設定は異なります。 `"holder"` DIV のサイズとブラウザーウィンドウの中央に合わせたサイズの両方が提供されます。 また、web ページでは、`HTML` と `BODY` 要素のサイズが 100% に設定されます。

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
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

## セッターベースの API を使用した埋め込み {#section-44e014925f24418b900696003855c0a9}

JSON ベースの初期化を使用する代わりに、setter ベースの API および no-args コンストラクターを使用することができます。 この API コンストラクターを使用すると、パラメーターは取得されず、`setContainerId()`、`setParam()`、`setAsset()` の API メソッドを使用して、個別のJavaScript呼び出しで設定パラメーターが指定されます。

次の例は、setter ベースの API を使用した固定サイズの埋め込みの使用を示しています。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 
```
