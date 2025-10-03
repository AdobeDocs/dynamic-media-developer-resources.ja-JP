---
title: eCatalog
description: eCatalog Viewer は、電子パンフレットをスプレッド別またはページ別にスプレッド別に表示するカタログ ビューアです。 eCatalog を使用すると、ユーザーは追加のユーザーインターフェイス要素または専用のサムネールモードを使用してカタログ内を移動できます。 ユーザーは、すべてのページをズームインして詳細を確認することもできます。
keywords: 応答
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 8e243fa5-e375-41ce-8b49-2571023130c1
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '2134'
ht-degree: 0%

---

# eCatalog{#ecatalog}

eCatalog Viewer は、電子パンフレットをスプレッド別またはページ別にスプレッド別に表示するカタログ ビューアです。 eCatalog を使用すると、ユーザーは追加のユーザーインターフェイス要素または専用のサムネールモードを使用してカタログ内を移動できます。 ユーザーは、すべてのページをズームインして詳細を確認することもできます。

>[!NOTE]
>
>画像レンダリング（IR）またはユーザー生成コンテンツ（UGC）を使用する画像は、このビューアではサポートされていません。

ビューアのタイプは 507 です。

[&#x200B; システム要件と前提条件 &#x200B;](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842) を参照してください。

このビューアは ecatalog で機能し、オプションの画像マップとソーシャル共有ツールをサポートしています。 ズームツール、カタログナビゲーションツール、全画面表示のサポート、サムネール、オプションの「閉じる」ボタンを備えています。 このビューアでは、ソーシャル共有ツール、印刷、ダウンロード、お気に入りもサポートされています。 デスクトップおよびモバイルデバイスで動作するように設計されています。


## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist](https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist)


## eCatalog ビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalog ビューアは、実行時にビューアによってダウンロードされるメインのJavaScript ファイルと一連のヘルパーファイル（1 つのJavaScriptに、この特定のビューアで使用されるすべてのビューア SDK コンポーネント、アセット、CSS が含まれます）を表します

eCatalog ビューアは、IS-Viewers に付属する実稼動用のHTML ページを使用してポップアップモードで使用することも、ドキュメント化された API を使用して対象の web ページに統合する埋め込みモードで使用することもできます。

設定とスキニングは、他のビューアと同様です。 すべてのスキニングは、カスタム CSS を使用して行います。

[&#x200B; すべてのビューアに共通のコマンドリファレンス – 設定属性 &#x200B;](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [&#x200B; すべてのビューアに共通のコマンドリファレンス - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) を参照してください

## eCatalog ビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

eCatalog ビューアでは、他のモバイルアプリケーションに共通する次のタッチジェスチャーをサポートしています。

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
   <td colname="col2"> <p> スウォッチの新しいサムネールを選択します。 </p> </td> 
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
   <td colname="col2"> <p> スライド フレームの切り替えを使用している場合は、カタログ ページのリストをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p>画像がリセット状態の場合は、ネイティブページのスクロールが実行されます。 </p> <p>サムネールがアクティブの場合は、サムネールのリストがスクロールします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

カタログページ間を移動するための現実的なページ反転アニメーション効果を有効にすることができます。 このような場合、ユーザーはページの隅を長押ししてドラッグし、ページを反転させることができます。

このビューアは、タッチスクリーンとマウスを備えた Windows デバイスでのタッチ入力とマウス入力の両方もサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11、Edgeの web ブラウザーのみに制限されます。

このビューアは、[&#x200B; キーボードのアクセシビリティとナビゲーション &#x200B;](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861) で説明されているように、完全にキーボードでアクセスできます。

## eCatalog ビューアを使用したソーシャルメディア共有ツール {#section-eb575084a99647c3a9591f439f40b412}

eCatalog ビューアでは、ソーシャル共有ツールをサポートしています。 これらは、ユーザーがクリックまたはタップすると共有ツールバーに展開されるメインコントロールバーのボタンとして使用できます。

共有ツールバーには、サポートされている共有チャネルのタイプ（Facebook、Twitter、メール共有、埋め込みコード共有、リンク共有など）ごとのアイコンが含まれています。 メール共有、埋め込み共有、リンク共有の各ツールがアクティベートされると、ビューアは対応するデータ入力フォームを含むモーダルダイアログボックスを表示します。 Facebook または Twitter が呼び出されると、ビューアはソーシャルサービスからの標準の共有ダイアログにユーザーをリダイレクトします。 Web ブラウザーのセキュリティ制限により、共有ツールは全画面表示モードでは使用できません。

## eCatalog ビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

Web ページによって、ビューアの動作に対するニーズは異なります。 選択するとビューアが別のブラウザーウィンドウで開くリンクが、web ページに表示される場合があります。 それ以外の場合は、ホスティングページにビューアを直接埋め込む必要があります。 後者の場合、web ページが静的なページレイアウトになっている可能性や、異なるデバイスや異なるブラウザーウィンドウサイズに異なる表示を行うレスポンシブデザインが使用されている可能性があります。 これらのニーズに対応するために、ビューアでは 3 つの主要な操作モード（ポップアップ、固定サイズの埋め込み、レスポンシブデザインの埋め込み）をサポートしています。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別の web ブラウザーウィンドウまたはタブで開きます。 ブラウザーのサイズが変更された場合や、モバイルデバイスの向きが変更された場合に、ブラウザーウィンドウ領域全体を使用して調整が行われます。

ポップアップモードは、モバイルデバイスで最も一般的です。 Web ページは、JavaScript呼び出し、HTML要素 `window.open()` の適切な設定、またはその他の適切なメソッド `A` 使用して、ビューアを読み込みます。

ポップアップ操作モードには、標準のHTML ページを使用することをお勧めします。 この場合、[!DNL eCatalogViewer.html] という名前で、標準の IS-Viewers デプロイメントの [!DNL html5/] サブフォルダー内に配置されます。

[!DNL <s7viewers_root>/html5/eCatalogViewer.html]

カスタム CSS を適用すると、視覚的にカスタマイズできます。

次に、新しいウィンドウでビューアを開くHTML コードの例を示します。

```html {.line-numbers}
<a href="https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアが既存の web ページに追加されます。これには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 閲覧者は通常、Web ページの不動産の一部のみを占有します。

主なユースケースは、デスクトップまたはタブレットデバイス向けの web ページと、デバイスタイプに応じて自動的にレイアウトを調整するレスポンシブデザインのページです。

固定サイズの埋め込みは、初回読み込み後にビューアのサイズが変更されない場合に使用されます。 この方法は、静的なレイアウトを持つ web ページに最適です。

レスポンシブデザインの埋め込みは、コンテナコンポー `DIV` ントのサイズ変更に応じて、実行時にビューアのサイズを変更する必要があることを前提としています。 最も一般的なユースケースは、柔軟なページレイアウトを使用する web ページにビューアを追加する場合です。

レスポンシブデザインの埋め込みモードでは、web ページのコンテナコンポー `DIV` ントのサイズがどのように調整されるかに応じて、ビューアの動作が異なります。 Web ページでコンテナ `DIV` の幅のみが設定され、高さが制限されない場合、ビューアは、使用されるアセットの縦横比に応じて自動的に高さを選択します。 この機能により、アセットが側面にパディングを入れずに、ビューに完全に収まります。 このユースケースは、Bootstrapや Foundation などのレスポンシブレイアウトフレームワークを使用した web ページで最も一般的です。

そうでない場合、web ページでビューアのコンテナ `DIV` の幅と高さの両方が設定されていると、ビューアはその領域だけを埋め、web ページレイアウトが提供するサイズに従います。 良い例は、ビューアをモーダルオーバーレイに埋め込む場合です。この場合、オーバーレイは web ブラウザーのウィンドウサイズに応じてサイズが調整されます。

**固定サイズ埋め込み**

Web ページにビューアを追加するには、次の手順を実行します。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ DIV の定義。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. Web ページへのビューアJavaScript ファイルの追加

   ビューアを作成するには、HTMLのヘッドにスクリプトタグを追加する必要があります。 ビューア API を使用する前に、必ず [!DNL eCatalogViewer.js] を含めてください。 [!DNL eCatalogViewer.js] ファイルは、標準の IS-Viewers デプロイメントの [!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/eCatalogViewer.js]

ビューアがAdobe Dynamic Media Classic サーバーの 1 つにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-Viewers がインストールされているAdobe Dynamic Media Classic サーバーの 1 つへのフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogViewer.js"></script>
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

1. ビューアサイズの設定

   ビューアの静的サイズは、トップレベル CSS クラスに対して絶対単位で宣言す `.s7ecatalogviewer` か、修飾子を使用して設定 `stagesize` きます。

   HTMLページに直接 CSS でサイズ設定を指定できます。 または、サイズ設定をカスタムビューアの CSS ファイルに入れます。この CSS ファイルは、後でDynamic Media Classicのビューアプリセットレコードに割り当てられたり、style コマンドを使用して明示的に渡されたりします。

   CSS を使用したビューアのスタイル設定について詳しくは、[eCatalog ビューアのカスタマイズ &#x200B;](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) を参照してください。

   HTML ページで静的ビューアサイズを定義する例を以下に示します。

   ```html {.line-numbers}
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   `stagesize` 修飾子は、Dynamic Media Classicのビューアプリセットレコードで設定できます。 または、次のように、コレクションを使用して、ビューア初期化コードで明示的 `params` 渡すか、コマンドリファレンスの節で説明されているように API 呼び出しとして渡すことができます。

   ```html {.line-numbers}
   eCatalogViewer.setParam("stagesize", 
   "640,480");
   ```

1. ビューアの初期化。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報 `s7viewers.eCatalogViewer` そのコンストラクターに渡して、ビューアインスタンスのメソッド `init()` 呼び出します。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトにはビューアコンテナ ID の名前を保持する `containerId` フィールドと、ビューアでサポートされてい `params` 設定パラメーターを含んだネストされた JSON オブジェクトが含まれています。 この場合、`params` オブジェクトには、少なくとも画像サービング URL がプロパティとして渡され、初期アセット `serverUrl` パラメーターとして渡されてい `asset` 必要があります。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成して開始できます。

   ビューアコードが ID でコンテナ要素を見つけられるように、ビューアコンテナを DOM に追加することが重要です。 一部のブラウザーでは、web ページの最後まで DOM の構築が遅れます。 ただし、互換性を最大限に高めるには、終了 `init()` タグの直前または body `BODY` イベントで `onload()` メソッドを呼び出します。

   同時に、コンテナ要素は、まだ web ページレイアウトの一部である必要はありません。 例えば、割り当てられたスタイルを使用して非表示 `display:none` する場合があります。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで、初期化プロセスを遅延します。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

   以下に、ビューアインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡して、`init()` メソッドを呼び出す例を示します。 この例では、`eCatalogViewer` がビューアインスタンス、`s7viewer` がプレースホルダー `DIV` の名前、`https://s7d1.scene7.com/is/image/` が画像サービング URL、`Viewers/Pluralist` がアセットであることを前提としています。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、eCatalog ビューアを固定サイズで埋め込む単純な web ページの完全な例です。

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高さが制限されないレスポンシブデザインの埋め込み**

レスポンシブデザインの埋め込みを使用すると、通常、web ページには、ビューアのコンテナ `DIV` ージの実行時サイズを指定する何らかの柔軟なレイアウトが配置されます。 この例では、web ページで、ビューアのコンテナ `DIV` ージの高さを制限せずに、web ブラウザーのウィンドウサイズの 40% を使用するとします。 生成される web ページのHTML コードは次のようになります。

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

このようなページにビューアを追加する方法は、固定サイズの埋め込みに似ています。唯一の違いは、ビューアのサイズを明示的に定義する必要がないことです。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ DIV の定義。
1. ビューアの作成と初期化。

上記の手順はすべて、固定サイズの埋め込みと同じです。 コンテナ `DIV` を既存の「holder」 `DIV` に追加します。 次のコードは完全な例です。 ブラウザーのサイズを変更したときのビューアのサイズの変化や、ビューアの縦横比がアセットにどのように一致するかを確認できます。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

次のページの例では、高さが制限されないレスポンシブデザインの埋め込みについて、より現実的なユースケースを示します。

[&#x200B; ライブデモ &#x200B;](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**幅と高さが定義された柔軟なサイズの埋め込み**

幅と高さが定義されたフレキシブルサイズの埋め込みでは、web ページのスタイル設定が異なります。 つまり、「ホルダー」 `DIV` ージに両方のサイズを提供し、ブラウザーウィンドウの中央に配置します。 また、Web ページでは、`HTML` 要素と `BODY` 要素のサイズが 100% に設定されます。

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

残りの埋め込みステップは、高さが制限されないレスポンシブデザインの埋め込みと同じです。 結果の例を次に示します。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Setter ベースの API を使用した埋め込み**

JSON ベースの初期化を使用する代わりに、設定ベースの API および no-args コンストラクターを使用することができます。 この API コンストラクターはパラメーターを取らず、`setContainerId()`、`setParam()`、`setAsset()` の API メソッドを使用して、個別のJavaScript呼び出しで設定パラメーターを指定します。

次の例は、setter ベースの API を使用した固定サイズの埋め込みを示しています。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogViewer = new s7viewers.eCatalogViewer(); 
eCatalogViewer.setContainerId("s7viewer"); 
eCatalogViewer.setParam("serverurl", "https://s7d1.scene7.com/is/image/"); 
eCatalogViewer.setAsset("Viewers/Pluralist"); 
eCatalogViewer.init(); 
</script> 
</body> 
</html>
```
