---
title: ズーム
description: ズームビューアは、ズーム可能な画像を表示する画像ビューアです。 このビューアは画像セットで機能し、ナビゲーションはスウォッチを使用しておこないます。 このビューアには、ズームツール、フルスクリーンのサポート、スウォッチおよびオプションの閉じるボタンがあります。 デスクトップおよびモバイルデバイスで動作するように設計されています。
keywords: レスポンシブ
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2393'
ht-degree: 0%

---

# ズーム{#zoom}

ズームビューアは、ズーム可能な画像を表示する画像ビューアです。 このビューアは画像セットで機能し、ナビゲーションはスウォッチを使用しておこないます。 このビューアには、ズームツール、フルスクリーンのサポート、スウォッチおよびオプションの閉じるボタンがあります。 デスクトップおよびモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR（画像レンダリング）または UGC（ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされません。

ビューアタイプ 502

詳しくは、 [必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## ズームビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

ズームビューアは、メインの JavaScript ファイルと、ヘルパーファイルのセット（この特定のビューア、アセット、CSS で使用されるすべての Viewer SDK コンポーネントが含まれる単一の JavaScript インクルード）で、ビューアが実行時にダウンロードします。

ズームビューアは、IS ビューアに付属する実稼動用HTMLページまたは埋め込みモードで、ドキュメント化された API を使用して target Web ページに統合され、ポップアップモードで使用できます。

設定とスキニングは、他のビューアと同様です。 スキニングはすべて、カスタム CSS を使用して行います。

詳しくは、 [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## ズームビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

ズームビューアでは、他のモバイルアプリケーションで一般的な以下のタッチジェスチャに対応しています。 ビューアがユーザーのスワイプジェスチャを処理できない場合、このイベントが Web ブラウザーに転送されて、ネイティブページスクロールが実行されます。 このような機能を使用すると、デバイスの画面領域のほとんどをビューアが占めている場合でも、ユーザーはページ内を移動できます。

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
   <td colname="col2"> <p> スウォッチ内の新しいサムネールを選択します。 メインビューでは、ユーザーインターフェイス要素の表示と非表示が切り替わります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ダブルタップ </p> </td> 
   <td colname="col2"> <p> 最大の拡大率に達するまで、1 レベルズームインします。 次のダブルタップジェスチャでは、ビューアが初期の表示状態にリセットされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ピンチ </p> </td> 
   <td colname="col2"> <p>ズームインまたはズームアウトします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平方向のスワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> スウォッチバーのスウォッチリストをスクロールします。 </p> <p> 画像がリセット状態で、 <span class="codeph"> frametransition </span> パラメータを slide に設定すると、アセットはスライドアニメーションで変更されます。 その他の場合 <span class="codeph"> frametransition </span> モード。このジェスチャはネイティブページスクロールを実行します。 </p> <p> 画像がズームインされると、画像は水平方向に移動されます。 画像を表示の端まで移動して、同じ方向でスワイプを実行すると、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直方向のスワイプ </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態の場合、このジェスチャではネイティブページスクロールが実行されます。 </p> <p> 画像がズームインされると、画像は垂直方向に移動します。 画像を表示の端まで移動し、同じ方向でスワイプを実行すると、ネイティブページスクロールが実行されます。 </p> <p> スウォッチ領域内でこのジェスチャを実行すると、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

タッチスクリーンとマウスを備えた Windows デバイスでは、タッチ入力とマウス入力の両方がサポートされます。 ただし、このサポートは、Chrome、Internet Explorer 11 および Edge Web ブラウザーにのみ制限されます。

このビューアは完全にキーボードでアクセス可能です。

詳しくは、 [キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## ズームビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Web ページごとに異なります。 Web ページにリンクが表示され、このリンクを選択すると、ビューアが別のブラウザーウィンドウで開かれる場合があります。 ホスティングページにビューアを直接埋め込む必要がある場合もあります。 後者の場合は、Web ページが静的レイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに異なる表示方法でレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは、ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込みの 3 つの主要な操作モードをサポートしています。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別の Web ブラウザーウィンドウまたはタブで開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやデバイスの向きが変更された場合は調整されます。

このモードは、モバイルデバイスで最も一般的なモードです。 Web ページでは、 `window.open()` JavaScript 呼び出し（適切に設定） `A` HTML要素、またはその他の適切な方法。

ポップアップ操作モードには、標準のHTMLページを使用することをお勧めします。 標準のHTMLページは、 `ZoomViewer.html` そしてそれは以下の場所にある `html5/` 次のように、標準の IS-Viewers デプロイメントのサブフォルダーに含めます。

`<s7viewers_root>/html5/ZoomViewer.html`

カスタム CSS を適用して、ページの外観をカスタマイズします。

次に、ビューアを新しいウィンドウでHTMLする開封コードの例を示します。

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存の Web ページに追加されます。ビューアに関連しない顧客コンテンツが既に存在する場合があります。 ビューアは、通常、Web ページの一部の領域のみを占有します。

主な使用例は、デスクトップやタブレットデバイス向けの Web ページと、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 このオプションは、静的レイアウトの Web ページに最適です。

レスポンシブデザイン埋め込みモードは、コンテナのサイズ変更により、実行時にビューアのサイズを変更する必要がある場合を想定しています `DIV`. 最も一般的な使用例は、柔軟なレイアウトを使用する Web ページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Web ページによるコンテナのサイズ変更の方法によって、ビューアの動作が異なります `DIV`. Web ページでコンテナの幅のみが設定される場合 `DIV`で選択し、高さは無制限のままにし、使用するアセットの縦横比に従って、ビューアによって高さが自動的に選択されます。 このロジックにより、両側のパディングなしで、アセットが表示に完全に収まります。 この使用例は、Web ページで、Bootstrapや Foundation などのレスポンシブレイアウトフレームワークを使用する Web ページで最も一般的です。

Web ページでビューアのコンテナの幅と高さの両方が設定されている場合 `DIV`を指定した場合、ビューアはその領域を埋め、Web ページに指定されているサイズに従います。 例えば、モーダルオーバーレイにビューアを埋め込み、オーバーレイが Web ブラウザーのウィンドウサイズに従ってサイズ変更される場合などです。

## 固定サイズ埋め込み {#section-44f365e6c0dd40709467a459afa82a7f}

ビューアを Web ページに追加するには、次の手順を実行します。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナ DIV を定義する。
1. ビューアのサイズを設定します。
1. ビューアを作成および初期化する。

1. ビューアの JavaScript ファイルを Web ページに追加する。

   ビューアを作成するには、HTMLhead にスクリプトタグを追加する必要があります。 ビューア API を使用する前に、必ず [!DNL ZoomViewer.js]. The [!DNL ZoomViewer.js] ファイルは、 [!DNL html5/js/] 標準の IS-Viewers デプロイメントのサブフォルダー

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

ビューアがいずれかのAdobe Dynamic Media Classicサーバーにデプロイされ、同じドメインから提供されている場合は、相対パスを使用できます。 それ以外の場合は、IS-Viewers がインストールされているAdobe Dynamic Media Classicのいずれかのサーバーへのフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
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

1. ビューアのサイズを設定します。

   複数項目セットを操作する場合、このビューアにはサムネールが表示されます。デスクトップシステムでは、サムネールはメインビューの下に配置されます。 同時に、ビューアでは実行時にメインアセットを入れ替えることができます。その際、 `setAsset()` API. 開発者は、新しいアセットに項目が 1 つだけある場合に、下部のサムネール領域をビューアがどのように管理するかを制御できます。 ビューアの外側のサイズはそのままにし、メインビューの高さを増やし、サムネール領域を表示させることができます。 また、メインビューのサイズを静的に保ち、ビューアの外側の領域を折りたたんで、Web ページのコンテンツを上に移動させ、サムネールから残された空きスクリーンの領域を使用することもできます。

   ビューアの外側の境界をそのままにしておくには、 `.s7zoomviewer` 最上位の CSS クラス（絶対単位）。 CSS のサイズ変更は、HTMLページで適切に設定できます。 または、カスタムビューアの CSS ファイルに追加し、それを後でDynamic Media Classicのビューアプリセットレコードに割り当てるか、スタイルコマンドを使用して明示的に渡すこともできます。

   詳しくは、 [ズームビューアのカスタマイズ](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) を参照してください。

   次の例では、ビューアページの外側の静的なサイズを定義します。HTML

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次の例では、ビューアの外側を固定した状態での動作を確認できます。 セットを切り替えても、ビューアの外側のサイズは変わりません。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html)

   メインビューのサイズを静的にするには、内側の絶対単位でビューアのサイズを定義します `Container` を使用する SDK コンポーネント `.s7zoomviewer` `.s7container` CSS セレクター、または `stagesize` 修飾子

   以下は、内部のビューアサイズを定義する例です `Container` アセットを切り替える際にメインビュー領域のサイズが変更されないようにする SDK コンポーネント：

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次のデモページは、メインビューのサイズを固定した場合のビューアの動作を示しています。 セットを切り替えても、メインビューは静的なままになり、Web ページのコンテンツは垂直方向に移動します。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html)

   次の設定が可能です。 `stagesize` 修飾子がDynamic Media Classicのビューアプリセットレコードに含まれていることを確認します。 または、を使用して、ビューア初期化コードで明示的に渡すこともできます。 `params` コレクションまたは API 呼び出しを使用できます（このヘルプの「コマンドリファレンス」の節で説明）。以下に例を示します。

   ```html {.line-numbers}
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   CSS ベースのアプローチを推奨します。この例では、を使用します。

1. ビューアを作成および初期化する。

   上記の手順を完了したら、のインスタンスを作成します。 `s7viewers.ZoomViewer` クラス、すべての設定情報をコンストラクタに渡し、を呼び出します。 `init()` メソッドを使用して、ビューアインスタンス上に配置できます。

   設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには `containerId` ビューアのコンテナ ID と入れ子になっているコンテナの名前が格納されるフィールド `params` ビューアがサポートする設定パラメーターを含む JSON オブジェクト。 この場合、 `params` オブジェクトには、少なくとも `serverUrl` プロパティと最初のアセットを次のように指定します。 `asset` パラメーター。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成し、起動できます。

   ビューアのコンテナを DOM に追加して、ビューアのコードが ID でコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Web ページの終わりまで DOM の構築が遅れます。 互換性を最大限に高めるには、 `init()` 終了直前の方法 `BODY` タグ、または本文 `onload()` イベント。

   同時に、コンテナ要素は必ずしも Web ページレイアウトに含まれているとは限りません。 例えば、 `display:none` スタイルが割り当てられています。 この場合、Web ページでコンテナ要素がレイアウトに戻るまで、ビューアは初期化プロセスを遅延します。 この操作を行うと、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、 `init()` メソッド。 この例では、次の点を前提としています。 `zoomViewer` はビューアインスタンスです。 `s7viewer` はプレースホルダ DIV の名前です。 `http://s7d1.scene7.com/is/image/` は画像サービングの URL で、 `Scene7SharedAssets/ImageSet-Views-Sample` はアセットです。

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

   次のコードは、固定サイズのビデオビューアを埋め込んだ簡単な Web ページの例です。

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

## 高さ無制限のレスポンシブデザイン埋め込み {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

レスポンシブデザイン埋め込みでは、Web ページには通常、ビューアのコンテナの実行時のサイズを指示する柔軟なレイアウトが指定されています `DIV`. 次の例では、Web ページがビューアのコンテナを許可しているとします。 `DIV` を使用すると、web ブラウザーのウィンドウサイズの 40%を占め、高さは無制限のままになります。 Web ページのHTMLコードは次のようになります。

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

このようなページにビューアを追加する手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、ビューアのサイズを明示的に定義する必要がない点です。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナ DIV を定義する。
1. ビューアを作成および初期化する。

上記の手順はすべて、固定サイズ埋め込みの場合と同じです。 コンテナ DIV を既存のに追加する `"holder"` DIV. 次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化すること、およびビューアの縦横比がアセットと一致することに注意してください。

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

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実際に使用されている例を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## 幅と高さが定義されたフレキシブルサイズ埋め込み {#section-3674e6c032594441a6576b7fb1de6e64}

幅と高さが定義されたフレキシブルサイズ埋め込みがある場合、Web ページのスタイル設定は異なります。 次の両方のサイズを `"holder"` DIV を指定し、ブラウザーウィンドウの中央に配置します。 また、Web ページでは `HTML` および `BODY` 要素を 100%に設定します。

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

残りの埋め込み手順は、高さ無制限のレスポンシブデザイン埋め込みで使用した手順と同じです。 結果の例は次のようになります。

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

JSON ベースの初期化を使用する代わりに、セッターベースの API と no-args コンストラクターを使用できます。 この API コンストラクターを使用する場合は、パラメーターは必要ありません。設定パラメーターは、 `setContainerId()`, `setParam()`、および `setAsset()` API メソッドを個別の JavaScript 呼び出しで使用できます。

次の例は、固定サイズ埋め込みをセッターベースの API で使用する方法を示しています。

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
