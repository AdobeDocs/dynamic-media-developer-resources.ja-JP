---
title: ズーム
description: Zoom Viewerは、ズーム可能な画像を表示する画像ビューアです。 このビューアは画像セットで機能し、ナビゲーションはスウォッチを使用して行われます。 ズームツール、フルスクリーンサポート、スウォッチ、オプションの閉じるボタンがあります。 デスクトップやモバイルデバイスで動作するように設計されています。
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
TQID: 'https://experienceleague.adobe.com/L-Dy2JpWs29wOU5v-sAqS2DO9uAtbo93hNLDWThMAmk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 2337
ht-degree: 0%

---

# ズーム{#zoom}

Zoom Viewerは、ズーム可能な画像を表示する画像ビューアです。 このビューアは画像セットで機能し、ナビゲーションはスウォッチを使用して行われます。 ズームツール、フルスクリーンサポート、スウォッチ、オプションの閉じるボタンがあります。 デスクトップやモバイルデバイスで動作するように設計されています。

>[!NOTE]
>
>IR （画像レンダリング）またはUGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアータイプ 502。

[必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Zoom Viewerの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

Zoom Viewerは、メインのJavaScript ファイルと一連のヘルパーファイルを表します（1つのJavaScriptには、この特定のビューアで使用されるすべてのViewer SDK コンポーネント、assets、CSSが含まれています）。実行時にビューアがダウンロードします。

ポップアップモードでは、IS-Viewersを備えた実稼動対応のHTML ページを使用するか、ドキュメント化されたAPIを使用してターゲット web ページに統合する埋め込みモードでZoom Viewerを使用できます。

設定とスキニングは、他のビューアと同様です。 すべてのスキニングは、カスタム CSSを使用して実行できます。

すべてのビューアに共通する[ コマンド参照 – 構成属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通するコマンド参照 – URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください

## Zoom Viewerの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

Zoom Viewerは、他のモバイルアプリケーションで一般的な次のタッチジェスチャーをサポートしています。 ビューアがユーザーのスワイプジェスチャーを処理できない場合、ネイティブページスクロールを実行するようにイベントをweb ブラウザーに転送します。 この種類の機能により、ビューアがデバイスの画面領域のほとんどを占めている場合でも、ユーザーはページ内を移動できます。

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
   <td colname="col2"> <p> スウォッチで新しいサムネールを選択します。 メインビューでは、ユーザーインターフェイス要素が表示または非表示になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ダブルタップ </p> </td> 
   <td colname="col2"> <p> 最大の倍率に達するまで1 レベルでズームします。 次のダブルタップジェスチャーは、ビューアを初期表示状態にリセットします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ピンチ </p> </td> 
   <td colname="col2"> <p>ズームインまたはズームアウト </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> スウォッチバーのスウォッチのリストをスクロールします。 </p> <p> 画像がリセット状態で、<span class="codeph"> frametransition </span> パラメーターがスライドに設定されている場合、アセットはスライドアニメーションで変更されます。 その他<span class="codeph"> frametransition </span> モードの場合、ジェスチャーはネイティブページスクロールを実行します。 </p> <p> 画像をズームインすると、画像が水平方向に移動します。 画像をビューエッジに移動し、スワイプを同じ方向に実行すると、ジェスチャーはネイティブページスクロールを実行します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>縦方向スワイプ </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態の場合、ジェスチャーはネイティブページスクロールを実行します。 </p> <p> 画像をズームインすると、画像が垂直方向に移動します。 画像をビューエッジに移動し、スワイプを同じ方向に実行すると、ジェスチャーはネイティブページスクロールを実行します。 </p> <p> ジェスチャーがスウォッチ領域内で行われた場合、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビューアは、タッチスクリーンとマウスを使用したWindows デバイスでのタッチ入力とマウス入力の両方をサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11、およびEdgeのweb ブラウザーのみに限定されます。

このビューアにはキーボードから完全にアクセス可能です。

[ キーボードのアクセシビリティとナビゲーション ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## Zoom Viewerの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

web ページごとに、閲覧者の行動に対するニーズは異なります。 Web ページでリンクが提供される場合があります。このリンクを選択すると、別のブラウザーウィンドウでビューアが開きます。 それ以外の場合は、ビューアをホスティングページに直接埋め込む必要があります。 後者の場合、web ページは静的なレイアウトを使用するか、異なるデバイスまたは異なるブラウザーウィンドウのサイズに対して異なる表示を行うレスポンシブデザインを使用します。 これらのニーズに対応するために、ビューアでは、ポップアップ、固定サイズの埋め込み、レスポンシブデザインの埋め込みという3つの主要な操作モードをサポートしています。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別のweb ブラウザーウィンドウまたはタブで開きます。 ブラウザーのウィンドウ領域全体を使用し、ブラウザーのサイズが変更されたり、デバイスの向きが変更されたりした場合に備えて調整します。

このモードは、モバイルデバイスで最も一般的です。 Web ページは、`window.open()` JavaScript呼び出し、`A` HTML要素の適切な設定、またはその他の適切なメソッドを使用してビューアを読み込みます。

ポップアップ操作モードには、標準のHTML ページを使用することをお勧めします。 標準のHTML ページは`ZoomViewer.html`と呼ばれ、次のように、標準のIS-Viewers デプロイメントの`html5/` サブフォルダーにあります。

`<s7viewers_root>/html5/ZoomViewer.html`

カスタム CSSを適用して、ページのカスタマイズされた外観を実現します。

次に、新しいウィンドウでビューアを開くHTML コードの例を示します。

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存のweb ページに追加されます。このページには、ビューアに関連しない顧客コンテンツが既に含まれている可能性があります。 通常、閲覧者はweb ページの不動産の一部しか占めていません。

主なユースケースは、デスクトップ PCやタブレットデバイス向けのweb ページです。デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインのページも使用できます。

初期読み込み後にビューアのサイズが変更されない場合は、固定サイズ埋め込みが使用されます。 このオプションは、静的レイアウトを持つweb ページに最適です。

レスポンシブデザイン埋め込みモードは、コンテナ `DIV`のサイズ変更により、実行時にビューアのサイズ変更が必要であると仮定します。 最も一般的なユースケースは、柔軟性の高いレイアウトを使用するweb ページにビューアを追加することです。

レスポンシブデザイン埋め込みモードでは、web ページのサイズとコンテナ `DIV`のサイズによって、ビューアの動作が異なります。 Web ページでコンテナ `DIV`の幅のみを設定し、高さを制限しない場合、ビューアは使用するアセットの縦横比に応じて自動的に高さを選択します。 このロジックにより、側面にパディングすることなく、アセットをビューに完全に収めることができます。 このユースケースは、BootstrapやFoundationなどのレスポンシブレイアウトフレームワークを使用するweb ページで最も一般的です。

Web ページがビューアのコンテナ `DIV`の幅と高さの両方を設定すると、ビューアはその領域に入力し、web ページが提供するサイズに従います。 例えば、ビューアをモーダルオーバーレイに埋め込むと、オーバーレイのサイズがweb ブラウザーのウィンドウサイズに応じて調整されます。

## 固定サイズ埋め込み {#section-44f365e6c0dd40709467a459afa82a7f}

次の操作を実行して、ビューアをweb ページに追加します。

1. ビューアのJavaScript ファイルをweb ページに追加します。
1. コンテナ DIVの定義。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. ビューアのJavaScript ファイルをweb ページに追加します。

   ビューアを作成するには、HTML ヘッドにスクリプトタグを追加する必要があります。 ビューアーAPIを使用する前に、[!DNL ZoomViewer.js]を含めることを確認してください。 [!DNL ZoomViewer.js] ファイルは、標準のIS-Viewers デプロイメントの[!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

ビューアがAdobe Dynamic Media Classic サーバーのいずれかにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-ViewersがインストールされているAdobe Dynamic Media Classic サーバーの1つにフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメイン ビューア JavaScript `include` ファイルのみを参照してください。 実行時にビューアのロジックによってダウンロードされる可能性があるweb ページコード内の他のJavaScript ファイルを参照しないでください。 特に、`/s7viewers` コンテキストパス（いわゆる統合SDK `include`）からビューアによって読み込まれたHTML5 SDK `Utils.js` ライブラリを直接参照しないでください。 その理由は、`Utils.js`または類似のランタイムビューアーライブラリの場所が、ビューアーのロジックによって完全に管理され、ビューアーリリース間で場所が変更されるためです。 Adobeは、古いバージョンのセカンダリビューア `includes`をサーバー上に保持しません。
>
>
>その結果、ビューアがページ上で使用するセカンダリ JavaScript `include`を直接参照すると、新しい製品バージョンがデプロイされる際に、将来的にビューア機能が破損します。

1. コンテナ DIVの定義。

   ビューアを表示するページに、空のDIV エレメントを追加します。 このIDは後でビューア APIに渡されるので、DIV要素にはIDが定義されている必要があります。

   プレースホルダーDIVは配置された要素です。`position` CSS プロパティが`relative`または`absolute`に設定されていることを意味します。

   次に、定義済みのプレースホルダーDIV要素の例を示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアサイズの設定。

   このビューアは、複数の項目セットを操作する際にサムネールを表示します。デスクトップシステムでは、サムネールがメインビューの下に配置されます。 同時に、ビューアでは、`setAsset()` APIを使用してランタイムでメインアセットを入れ替えることができます。 開発者は、新しいアセットが1つのアイテムしか持たない場合に、ビューアが下部のサムネール領域をどのように管理するかを制御できます。 外のビューアのサイズを維持し、メインビューの高さを上げてサムネール領域を占有することができます。 または、メインビューサイズを静的に保ち、外側のビューア領域を折りたたんで、web ページのコンテンツを上に移動させ、サムネールから残った空き画面の不動産を使用することもできます。

   外部ビューアの境界を維持するには、`.s7zoomviewer` トップレベル CSS クラスのサイズを絶対単位で定義します。 CSSのサイズは、HTML ページに配置できます。 または、カスタムのビューア CSS ファイルに配置して、後でDynamic Media Classicのビューアプリセットレコードに割り当てるか、スタイルコマンドを使用して明示的に渡すことができます。

   CSSを使用したビューアのスタイル設定について詳しくは、[Zoom ビューアのカスタマイズ ](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)を参照してください。

   次に、HTML ページで静的な外部ビューアサイズを定義する例を示します。

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

<!-- You can see the behavior with a fixed outer viewer in the following example. Notice that when you switch between sets, the outer viewer size does not change: -->

<!--

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html)

-->

メインビューのディメンションを静的にするには、`.s7zoomviewer` `.s7container` CSS セレクターを使用するか、`stagesize`修飾子を使用して、内部`Container` SDK コンポーネントのビューアーサイズを絶対単位で定義します。

次に、アセットを切り替える際にメインビュー領域のサイズが変更されないように、内部`Container` SDK コンポーネントのビューアーサイズを定義する例を示します。

```html {.line-numbers}
#s7viewer.s7zoomviewer .s7container { 
 width: 640px; 
 height: 480px; 
}
```

<!-- The following demo page shows the viewer behavior with a fixed main view size. Notice that when you switch between sets, the main view remains static and the web page content moves vertically. -->

<!--

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html)

-->

Dynamic Media Classicのビューアプリセットレコードで`stagesize`修飾子を設定できます。 または、`params` コレクションを使用してビューアの初期化コードを使用して明示的に渡すか、このヘルプの「コマンドリファレンス」セクションで説明されているように、API呼び出しとして渡すことができます。次に示します。

```html {.line-numbers}
 zoomViewer.setParam("stagesize", 
"640,480");
```

CSS ベースのアプローチを推奨し、この例で使用します。

1. ビューアの作成と初期化。

   上記の手順を完了したら、`s7viewers.ZoomViewer` クラスのインスタンスを作成し、すべての構成情報をそのコンストラクターに渡し、ビューアーインスタンスで`init()` メソッドを呼び出します。

   構成情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアコンテナ IDの名前を保持する`containerId` フィールドと、ビューアがサポートする設定パラメーターを含むネストされた`params` JSON オブジェクトが必要です。 この場合、`params` オブジェクトには、少なくとも`serverUrl` プロパティとして渡されたImage Serving URLと`asset` パラメーターとして最初のアセットが必要です。 JSON ベースの初期化APIを使用すると、1行のコードでビューアを作成して開始できます。

   ビューアコードがIDでコンテナ要素を見つけられるように、ビューアコンテナをDOMに追加することが重要です。 一部のブラウザーは、Web ページの最後までDOMの構築を遅らせます。 互換性を最大限に高めるには、終了`BODY` タグの直前または本文`onload()` イベントで`init()` メソッドを呼び出します。

   同時に、コンテナ要素は必ずしもweb ページレイアウトの一部であってはなりません。 例えば、割り当てられた`display:none` スタイルを使用して非表示にすることができます。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで初期化プロセスを遅らせます。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

   次に、ビューアーインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡し、`init()` メソッドを呼び出す例を示します。 この例では、`zoomViewer`がビューアインスタンスで、`s7viewer`がプレースホルダーDIVの名前、`http://s7d1.scene7.com/is/image/`が画像サービング URL、`Scene7SharedAssets/ImageSet-Views-Sample`がアセットであると仮定します。

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

   次のコードは、ビデオビューアを固定サイズで埋め込む面倒なweb ページの完全な例です。

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

## 無制限の高さを持つレスポンシブデザイン埋め込み {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

レスポンシブデザインの埋め込みでは、通常、web ページには、ビューアのコンテナ `DIV`のランタイムサイズを決定する、ある種の柔軟なレイアウトが配置されています。 次の例では、web ページでビューアのコンテナ `DIV`がweb ブラウザーのウィンドウ サイズの40%を使用でき、高さは制限されないと仮定します。 Web ページのHTML コードは次のようになります。

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
1. コンテナ DIVの定義。
1. ビューアの作成と初期化。

上記のすべての手順は、固定サイズの埋め込みと同じです。 コンテナ DIVを既存の`"holder"` DIVに追加します。 次のコードは、完全な例です。 ブラウザーのサイズを変更するとビューアのサイズが変わり、ビューアの縦横比がアセットとどのように一致するかを確認します。

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

次のサンプルページでは、高さの制限のないレスポンシブデザイン埋め込みをより実際に使用する方法を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## 幅と高さが定義された柔軟なサイズの埋め込み {#section-3674e6c032594441a6576b7fb1de6e64}

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

残りの埋め込み手順は、高さの制限のないレスポンシブデザイン埋め込みに使用する手順と同じです。 結果として得られる例は次のとおりです。

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

## セッターベースのAPIを使用した埋め込み {#section-44e014925f24418b900696003855c0a9}

JSON ベースの初期化を使用する代わりに、セッターベースのAPIとno-args コンストラクターを使用できます。 このAPI コンストラクターを使用すると、パラメーターは受け取られず、設定パラメーターは`setContainerId()`、`setParam()`、`setAsset()`のAPI メソッドを使用して指定され、別々のJavaScript呼び出しが行われます。

次の例は、セッターベースのAPIを使用した固定サイズの埋め込みを使用する方法を示しています。

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

