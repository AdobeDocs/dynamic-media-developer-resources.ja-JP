---
title: ビデオ
description: ビデオビューアは、H.264 形式でエンコードされたストリーミングおよびプログレッシブビデオを再生するビデオプレーヤーです。 Dynamic Mediaと共にDynamic Media ClassicまたはAdobe Experience Managerから配信されます。
keywords: 応答
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2333'
ht-degree: 0%

---

# ビデオ{#video}

ビデオビューアは、H.264 形式でエンコードされたストリーミングおよびプログレッシブビデオを再生するビデオプレーヤーです。 Dynamic Mediaは、Dynamic Media ClassicまたはExperience Managerから提供されます。

[ システム要件と前提条件 ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842) を参照してください。

単一のビデオとアダプティブビデオセットの両方がサポートされています。 また、ビューアでは、外部の場所でホストされているプログレッシブビデオおよび HLS ストリームの操作もサポートされています。 HTML5 ビデオをサポートするデスクトップとモバイルの両方の web ブラウザーで動作するように設計されています。 このビューアでは、ビデオコンテンツ、ビデオチャプターナビゲーションおよびソーシャルメディア共有ツールの上に表示されるオプションのクローズドキャプションもサポートされます。

ビデオビューアは、基になるシステムでサポートされている場合は常に、デフォルト設定で HLS 形式のHTML5 ストリーミングビデオ再生を使用します。 HTML5 ストリーミングをサポートしていないシステムでは、ビューアはHTML5 プログレッシブビデオ配信にフォールバックします。

ビューアのタイプは 506 です。

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## ビデオビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

ビデオビューアは、メインのJavaScript ファイルとヘルパーファイルのセットを表します。1 つのJavaScriptには、この特定のビューア、アセットおよび実行時にビューアによってダウンロードされる CSS で使用されるすべての Viewer SDK コンポーネントが含まれます。

IS-Viewers に用意されている実稼動用のHTMLーページを使用して、ポップアップモードでビデオビューアを使用できます。 または、埋め込みモードでビューアを使用し、ドキュメントに記載されている API を使用してターゲット web ページに統合することもできます。

ビューアの設定とスキニングのタスクは、他のビューアと似ています。 すべてのスキニングは、カスタム CSS を使用して行います。

[ すべてのビューアに共通のコマンドリファレンス – 設定属性 ](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [ すべてのビューアに共通のコマンドリファレンス - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) を参照してください

## ビデオビューアの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

ビデオビューアには、再生/一時停止ボタン、ビデオスクラバーのビデオのタイムバブル、再生時間/合計時間インジケーター、ボリュームコントロール、フルスクリーンボタン、クローズドキャプションの切り替えなど、ビデオ再生用の標準のユーザーインターフェイスコントロールのセットが用意されています。 これらのコントロールはすべて、ビューアのユーザーインターフェイスの下部にあるコントロールバーにグループ化されます。

タッチデバイスでは、ハードウェアボタンを使用してのみ音量を制御できるため、ボリュームコントロールはユーザーインターフェイスに表示されません。

ビューアがポップアップモードで動作している場合、ユーザーインターフェイスでフルスクリーンボタンを使用できません。

ビデオチャプターがアクティベートされたときに、ビデオのコンテンツをすばやく移動できます。 ビデオチャプターは、ビデオスクラバートラックにマーカーとして表示され、チャプタータイトルと関連する説明が、マウスのロールオーバーやタッチシステムでのシングルタップで表示されます。 チャプターマーカーを選択するか、チャプター説明のバブルを選択すると、特定のチャプターをシークできます。

ビューアは、タッチスクリーンとマウスを備えた Windows デバイスでのタッチ入力とマウス入力の両方をサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11、Edgeの web ブラウザーのみに制限されます。

このビューアは完全にキーボードでアクセス可能です。

詳しくは [ キーボードアクセシビリティとナビゲーション ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861) を参照してください。

## ビデオビューアを使用したソーシャルメディア共有ツール {#section-907d316fe1da4b87abb9775f02464704}

ビデオビューアでは、ソーシャルメディア共有ツールをサポートしています。 ユーザーインターフェイスでは 1 つのボタンとして使用でき、ユーザーがクリックまたはタップすると、共有ツールバーに展開されます。

共有ツールバーには、サポートされている共有チャネルのタイプ（Facebook、Twitter、メール共有、埋め込みコード共有、リンク共有など）ごとのアイコンが表示されます。 メール共有、埋め込み共有、リンク共有の各ツールがアクティベートされると、ビューアは対応するデータ入力フォームを含むモーダルダイアログボックスを表示します。 facebookまたはTwitterが呼び出されると、ビューアはソーシャルメディアサービスから標準の共有ダイアログボックスにリダイレクトします。 また、共有ツールがアクティブになると、ビデオの再生は自動的に一時停止します。

Web ブラウザーのセキュリティ制限により、共有ツールは全画面表示モードでは使用できません。

## ビデオビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

Web ページによって、ビューアの動作に対するニーズは異なります。 選択すると別のブラウザーウィンドウでビューアが開くリンクが、web ページに表示される場合があります。 それ以外の場合は、ホスティングページにビューアを直接埋め込む必要があります。 後者の場合、web ページが静的なページレイアウトになっている可能性や、異なるデバイスや異なるブラウザーウィンドウサイズに異なる表示を行うレスポンシブデザインが使用されている可能性があります。 これらのニーズに対応するために、ビューアでは 3 つの主要な操作モード（ポップアップ、固定サイズの埋め込み、レスポンシブデザインの埋め込み）をサポートしています。

同じページへの複数のビデオの埋め込みは、タブレットやモバイルデバイスでサポートされています。 通常、一度に再生できるビデオは 1 つだけです。 ユーザーがあるビデオの再生を開始してから、別のビデオを再生しようとすると、最初のビデオは自動的に一時停止されます。 自動一時停止されたビデオは現在の再生時間を記憶しているので、ユーザーはいつでも元に戻って再生を再開できます。 唯一の例外は、ビデオを並行して再生できるAndroid™ 4.x デバイスのChrome ブラウザーです。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別の web ブラウザーウィンドウまたはタブで開きます。 ブラウザーのウィンドウ領域全体を使用し、ブラウザーのサイズが変更された場合や、デバイスの向きが変更された場合に備えて調整されます。

このモードは、モバイルデバイスで最も一般的です。 Web ページは、JavaScript呼び出し、HTML要素 `window.open()` の適切な設定、またはその他の適切なメソッド `A` 使用して、ビューアを読み込みます。

ポップアップ操作モードには、標準のHTMLページを使用することをお勧めします。 このフォルダーは [!DNL VideoViewer.html] と呼ばれ、標準の IS-Viewers デプロイメントの [!DNL html5/] サブフォルダーに配置されています。

[!DNL <s7viewers_root>/html5/VideoViewer.html]

カスタム CSS を適用すると、視覚的にカスタマイズできます。

次に、ビューアを新しいウィンドウで開くHTMLコードの例を示します。

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブ埋め込みモードについて**

埋め込みモードでは、ビューアが既存の web ページに追加されます。これには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 閲覧者は通常、Web ページの領域の一部のみを占有します。

主なユースケースは、デスクトップやタブレットデバイス向けの web ページと、デバイスタイプに応じて自動的にレイアウトを調整するレスポンシブデザインページです。

固定サイズの埋め込みは、初回読み込み後にビューアがサイズを変更しない場合に使用されます。 この選択は、静的なページレイアウトを持つ web ページに最適です。

レスポンシブデザインの埋め込みは、コンテナコンポー `DIV` ントのサイズ変更に応じて、実行時にビューアのサイズを変更する必要があることを前提としています。 最も一般的なユースケースは、柔軟なページレイアウトを使用する web ページにビューアを追加する場合です。

レスポンシブデザインの埋め込みモードでは、web ページのコンテナ `DIV` ージのサイズがどのように調整されるかによってビューアの動作が異なります。 Web ページでコンテナ `DIV` の幅のみが設定され、高さが制限されない場合、ビューアは、使用されるアセットの縦横比に応じて自動的に高さを選択します。 この方法では、アセットが側面にパディングを入れずに、ビューに完全に収まります。 このユースケースは、Bootstrapや基盤などのレスポンシブデザインレイアウトフレームワークを使用する web ページで最も一般的です。

そうでない場合、web ページでビューアのコンテナ `DIV` の幅と高さの両方が設定されていると、ビューアはその領域だけを埋め、web ページレイアウトで指定されているサイズに従います。 良い例は、ビューアをモーダルオーバーレイに埋め込む場合です。この場合、オーバーレイは web ブラウザーウィンドウのサイズに合わせてサイズが調整されます。

**固定サイズ埋め込み**

Web ページにビューアを追加するには、次の手順を実行します。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ `DIV` を定義します。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. Web ページへのビューアJavaScript ファイルの追加

   ビューアを作成するには、HTMLの先頭にスクリプトタグを付ける必要があります。 ビューア API を使用する前に、必ず [!DNL FlyoutViewer.js] を含めてください。 [!DNL FlyoutViewer.js] ファイルは、標準の IS-Viewers デプロイメントの [!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

ビューアがAdobe Dynamic Media Classic サーバーの 1 つにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-Viewers がインストールされているAdobe Dynamic Media Classic サーバーの 1 つへのフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScript `include` ファイルのみを参照します。 実行時にビューアのロジックによってダウンロードされる可能性がある web ページコード内の追加のJavaScript ファイルを参照しないでください。 特に、ビューアによって読み込まれるHTML5 SDK `Utils.js` ライブラリをコンテキストパス（いわゆる統合 SDK `include`）から直接参照 `/s7viewers` ないでください。 これは、`Utils.js` や類似のランタイム・ビューア・ライブラリの場所はビューアのロジックによって完全に管理され、ビューア・リリース間で場所が変更されるためです。 Adobeは、古いバージョンのセカンダリ・ビューア `includes` をサーバ上に保持しません。
>
>
>その結果、ビューアが使用するセカンダリ JavaScript `include` ージをページ上で直接参照すると、今後、新しい製品バージョンがデプロイされた際に、ビューアの機能が損なわれます。

1. コンテナ DIV の定義。

   ビューアを表示するページに、空の DIV 要素を追加します。 DIV 要素には ID が定義されている必要があります。これは、この ID が後でビューア API に渡されるためです。 DIV のサイズは CSS で指定します。

   プレースホルダー DIV が配置済み要素です（つまり、`position` CSS プロパティが `relative` または `absolute` に設定されています）。

   Internet Explorer で全画面表示モードが正しく機能することを確認します。 プレースホルダー DIV よりも重ね順が大きい要素が DOM に他にないことを確認します。

   定義されたプレースホルダー DIV 要素の例を以下に示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. ビューアサイズの設定

   ビューアの静的サイズは、最上位の CSS クラスに対して絶対単位で宣言す `.s7videoviewer` か、修飾子 `stagesize` を使用して設定できます。

   サイズ設定は、HTMLページの直接の CSS、またはカスタムビューアの CSS ファイルに入れることができます。 その後、コンテンツフラグメントはDynamic Media Classicのビューアプリセットレコードに割り当てられるか、スタイルコマンドを使用して明示的に渡されます。

   CSS を使用したビューアのスタイル設定について詳しくは、[ ビデオビューアのカスタマイズ ](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) を参照してください。

   HTMLページで静的ビューアのサイズを定義する例を以下に示します。

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   修飾子 `stagesize`、Dynamic Media Classicのビューアプリセットレコードで設定するか、コレクションを使用してビューア初期化コードで明示的に渡 `params` ことができます。 または、コマンドリファレンスの節で説明したように、API 呼び出しとして、次に示します。

   ```html {.line-numbers}
   videoViewer.setParam("stagesize", "640,480");
   ```

   この例では、CSS ベースのアプローチをお勧めします。

1. ビューアの作成と初期化。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報 `s7viewers.VideoViewer` そのコンストラクターに渡し、ビューアインスタンスのメソッド `init()` 呼び出します。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトにはビューアコンテナ ID の名前 `containerId` 保持するフィールドと、ビューアでサポートされ `params` 設定パラメーターを含むネストされた JSON オブジェクトが必要です。 この場合、オブジェクト `params` は、少なくとも、プロパティとして画像サービング URL が渡され、プロパティとしてビデオサーバー URL`serverUrl` 渡され、パラメーターとして初期アセット `videoserverurl` 渡されてい `asset` 必要があります。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成して開始できます。

   ビューアコードが ID でコンテナ要素を見つけられるように、ビューアコンテナを DOM に追加することが重要です。 一部のブラウザーでは、web ページの最後まで DOM の構築が遅れます。 互換性を最大限に高めるには、終了 `BODY` タグの直前または body `onload()` イベントで `init()` メソッドを呼び出します。

   同時に、コンテナ要素は、まだ web ページレイアウトの一部である必要はありません。 例えば、割り当てられたスタイルを使用して非表示 `display:none` する場合があります。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで、初期化プロセスを遅延します。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

   次に、ビューアインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡して、`init()` メソッドを呼び出す例を示します。 この例では、`videoViewer` がビューアインスタンス、`s7viewer` がプレースホルダー `DIV` の名前、[!DNL http://s7d1.scene7.com/is/image/] が画像サービング URL、[!DNL http://s7d1.scene7.com/is/content/] がビデオサーバーの URL、[!DNL Scene7SharedAssets/Glacier_Climber_MP4] がアセットであると想定しています。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   次のコードは、ビデオビューアを固定サイズで埋め込む単純な web ページの完全な例です。

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**高さが制限されないレスポンシブデザインの埋め込み**

レスポンシブデザインの埋め込みを使用すると、通常、web ページには、ビューアのコンテナ `DIV` ージの実行時サイズを指示する何らかの柔軟なレイアウトが配置されます。 この例では、web ページで、ビューアのコンテナ `DIV` ージの高さを制限せずに、web ブラウザーのウィンドウサイズの 40% を使用するとします。 Web ページのHTMLコードは次のようになります。

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

このようなページにビューアを追加する方法は、固定サイズの埋め込みと似ています。唯一の違いは、ビューアのサイズを明示的に定義する必要がない点です。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ DIV の定義。
1. ビューアの作成と初期化。

上記の手順はすべて、固定サイズの埋め込みと同じです。 コンテナ `DIV` を既存の「ホルダー」 `DIV` に追加します。 次のコードは完全な例です。 ブラウザーのサイズを変更したときのビューアのサイズの変化や、ビューアの縦横比がアセットにどのように一致するかを確認できます。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

次のページの例では、高さが制限されないレスポンシブデザインの埋め込みを使用した実際の使用例を示しています。

[ ライブデモ ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[ 代替デモの場所 ](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=ja)

**幅と高さが定義されたレスポンシブデザインの埋め込み**

幅と高さが定義されたレスポンシブデザインの埋め込みがある場合、web ページのスタイルは異なります。これは、「ホルダー」 `DIV` ージのサイズと、ブラウザーウィンドウの中央にあるサイズの両方を提供します。 また、Web ページでは、`HTML` 要素と `BODY` 要素のサイズが 100% に設定されます。

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Setter ベースの API を使用した埋め込み**

JSON ベースの初期化を使用する代わりに、setter ベースの API および no-args コンストラクターを使用することができます。 この API を使用する場合、コンストラクターはパラメーターを取らず、`setContainerId()`、`setParam()`、`setAsset()` の API メソッドを使用して、個別のJavaScript呼び出しで設定パラメーターを指定します。

次の例は、setter ベースの API を使用した固定サイズの埋め込みを示しています。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var videoViewer = new s7viewers.VideoViewer(); 
videoViewer.setContainerId("s7viewer"); 
videoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
videoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
videoViewer.setAsset("Scene7SharedAssets/Glacier_Climber_MP4"); 
videoViewer.init(); 
</script> 
</body> 
</html> 
```
