---
title: スマート切り抜きビデオビューア
description: スマート切り抜きビデオビューアは、ストリーミングビデオとプログレッシブビデオを H.264 形式でエンコードし、スマート切り抜きのサポートが追加された状態で再生します。 Dynamic Mediaと共にDynamic Media ClassicまたはAdobe Experience Managerから配信されます。
keywords: レスポンシブ
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 937be8a2-307e-47bb-9fc8-d354f780a214
source-git-commit: fbc7d7394614c0c22ab70207f2b55cd062bcd4e7
workflow-type: tm+mt
source-wordcount: '2408'
ht-degree: 0%

---

# スマート切り抜きビデオ{#smart-crop-video}

スマート切り抜きビデオビューアは、H.264 形式でエンコードされたストリーミングビデオとプログレッシブビデオを再生し、スマート切り抜きのサポートが追加されました。 Dynamic Media Classicから、またはDynamic MediaとのExperience Managerから配信されます。

詳しくは、 [必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

単一のビデオとアダプティブビデオセットの両方がサポートされています。 また、ビューアでは、外部でホストされているプログレッシブビデオおよび HLS ストリームの操作もサポートされています。 デスクトップとモバイル Web ブラウザーの両方で動作し、HTML5 ビデオをサポートするように設計されています。 このビューアは、ビデオコンテンツの上部に表示されるオプションのクローズドキャプション、ビデオチャプターナビゲーションおよびソーシャルメディア共有ツールもサポートしています。

スマート切り抜きビデオビューアは、基になるシステムが HLS 形式をサポートしている場合は常に、デフォルト設定で HLS 形式のHTML5 ストリーミングビデオ再生を使用します。 HTML5 ストリーミングをサポートしていないシステムでは、ビューアはHTML5 プログレッシブビデオ配信にフォールバックします。

ビューアタイプ 518

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS](https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS)

## スマート切り抜きビデオビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

スマート切り抜きビデオビューアは、メインの JavaScript ファイルとヘルパーファイルのセットです。1 つの JavaScript インクルードには、この特定のビューア、アセットおよびビューアが実行時にダウンロードするすべての Viewer SDK コンポーネントが含まれます。

IS ビューアに付属の実稼動用HTMLページを使用して、スマート切り抜きビデオビューアをポップアップモードで使用できます。 または、ビューアを埋め込みモードで使用し、ドキュメントに記載されている API を使用してターゲット Web ページに統合することもできます。

ビューアの設定とスキニングのタスクは、他のビューアと同様です。 スキニングはすべて、カスタム CSS を使用して行います。

詳しくは、 [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## スマート切り抜きビデオビューアの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

スマート切り抜きビデオビューアは、ビデオ再生用の一連の標準的なユーザーインターフェイスコントロールを提供します。次に例を示します。

* 再生/一時停止ボタン。
* ビデオスクラバーのビデオの時間の吹き出し。
* 再生時間/合計時間インジケーター。
* ボリューム制御
* 全画面表示ボタン。
* クローズドキャプションの切り替え。

これらのコントロールはすべて、ビューアユーザインターフェイスの下部にあるコントロールバーにグループ化されています。

タッチデバイスでは、ハードウェアボタンを使用してのみボリュームを制御できるので、ボリューム制御はユーザーインターフェイスに表示されません。

ビューアがポップアップモードで動作している場合、ユーザーインターフェイスではフルスクリーンボタンを使用できません。

ビデオチャプターが有効になっている場合は、ビデオのコンテンツをすばやく移動できます。 ビデオチャプターは、ビデオスクラバートラック内にマーカーとして表示され、マウスのロールオーバー時、またはタッチシステムで 1 回タップしたときに、チャプタータイトルと関連する説明が表示されます。 チャプターマーカーを選択するか、チャプターの説明の吹き出しを選択することで、特定のチャプターを探すことができます。

タッチスクリーンとマウスを備えた Windows デバイスでは、タッチ入力とマウス入力の両方がサポートされます。 ただし、このサポートは、Chrome、Internet Explorer 11 および Edge Web ブラウザーにのみ制限されます。

このビューアは完全にキーボードでアクセス可能です。

詳しくは、 [キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## スマート切り抜きビデオビューアを使用したソーシャルメディア共有ツール {#section-907d316fe1da4b87abb9775f02464704}

スマート切り抜きビデオビューアは、ソーシャルメディア共有ツールをサポートしています。 これらは、ユーザーインターフェイスで 1 つのボタンとして使用でき、ユーザーがクリックまたはタップすると、共有ツールバーに展開されます。

共有ツールバーには、Facebook、Twitter、電子メール共有、埋め込みコード共有、リンク共有など、サポートされる共有チャネルの各タイプ用のアイコンが表示されます。 電子メール共有、埋め込み共有またはリンク共有のツールをアクティブにすると、ビューアにモーダルダイアログボックスが表示され、対応するデータ入力フォームが表示されます。 facebookまたはTwitterを呼び出すと、ソーシャルメディアサービスの標準の共有ダイアログボックスにリダイレクトされます。 また、共有ツールが有効になると、ビデオ再生が自動的に一時停止します。

Web ブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは使用できません。

## スマート切り抜きビデオビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Web ページごとに異なります。 Web ページにリンクが表示され、このリンクを選択すると、別のブラウザーウィンドウでビューアが開く場合があります。 ホスティングページに直接ビューアを埋め込む必要がある場合もあります。 後者の場合は、Web ページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは次の 3 つの主要な操作モードがサポートされています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

同じページへの複数のビデオの埋め込みは、タブレットとモバイルデバイスでサポートされています。 通常、一度に 1 つのビデオのみ再生できます。 ユーザーが 1 つのビデオの再生を開始し、別のビデオの再生を試みると、最初のビデオが自動的に一時停止します。 自動一時停止されたビデオは現在の再生時間を記憶するので、ユーザーはいつでも元に戻って再生を再開できます。 ただし、Android™ 4.x デバイスの Chrome ブラウザーでは、ビデオを並行して再生できます。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別の Web ブラウザーウィンドウまたはタブで開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやデバイスの向きが変更された場合は調整されます。

このモードは、モバイルデバイスで最も一般的なモードです。 Web ページでは、 `window.open()` JavaScript 呼び出し（適切に設定） `A` HTML要素、またはその他の適切な方法。

ポップアップ操作モードには、標準のHTMLページを使用することをお勧めします。 これは、と呼ばれます。 [!DNL SmartCropVideoViewer.html] そしてそれは以下の場所にある [!DNL html5/] 標準の IS-Viewers デプロイメントのサブフォルダー

[!DNL <s7viewers_root>/html5/SmartCropVideoViewer.html]

カスタム CSS を適用することで、視覚的なカスタマイズを実現できます。

以下は、ビューアを新しいウィンドウでHTMLする開封コードの例です。

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブ埋め込みモードについて**

埋め込みモードでは、ビューアは既存の Web ページに追加されます。ビューアに関連しない顧客コンテンツが既に存在する場合があります。 ビューアは、通常、Web ページの一部の領域のみを占有します。

主な使用例は、デスクトップやタブレットデバイス向けの Web ページと、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 この選択は、静的ページレイアウトの Web ページに最適です。

レスポンシブデザイン埋め込みは、コンテナのサイズ変更に応じて実行時にビューアのサイズを変更する必要がある場合を想定しています `DIV`. 最も一般的な使用例は、柔軟なページレイアウトを使用する Web ページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Web ページによるコンテナのサイズ変更の方法によって、ビューアの動作が異なります `DIV`. Web ページでコンテナの幅のみが設定される場合 `DIV`で選択し、高さは無制限のままにし、使用するアセットの縦横比に従って、ビューアによって高さが自動的に選択されます。 この方法を使用すると、両側のパディングなしで、アセットが表示に完全に収まります。 この使用例は、Web ページで最も一般的なもので、Bootstrapや Foundation などのレスポンシブデザインレイアウトフレームワークを使用します。

それ以外の場合は、Web ページでビューアのコンテナの幅と高さの両方が設定されている場合 `DIV`を指定した場合、ビューアはその領域だけを埋め、Web ページレイアウトで指定されたサイズに従います。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイが Web ブラウザーウィンドウのサイズに従ってサイズ変更される場合があります。

**固定サイズ埋め込み**

ビューアを Web ページに追加するには、次の手順を実行します。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナの定義 `DIV`.
1. ビューアのサイズを設定します。
1. ビューアを作成および初期化する。

1. ビューアの JavaScript ファイルを Web ページに追加する。

   ビューアを作成するには、HTMLhead にスクリプトタグを追加する必要があります。 ビューア API を使用する前に、 [!DNL SmartCropVideoViewer.js]. この [!DNL SmartCropVideoViewer.js] ファイルは [!DNL html5/js/] 標準の IS-Viewers デプロイメントのサブフォルダー

[!DNL <s7viewers_root>/html5/js/SmartCropVideoViewer.js]

ビューアがいずれかのAdobe Dynamic Media Classicサーバーにデプロイされ、同じドメインから提供されている場合は、相対パスを使用できます。 それ以外の場合は、IS-Viewers がインストールされているAdobe Dynamic Media Classicのいずれかのサーバーへのフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SmartCropVideoViewer.js"></script>
```

>[!NOTE]
>
>メインビューアの JavaScript のみを参照します。 `include` ファイルをページに貼り付けます。 実行時にビューアのロジックによってダウンロードされる可能性のある、Web ページコード内の追加の JavaScript ファイルは参照しないでください。 特に、HTML5 SDK を直接参照しないでください `Utils.js` からビューアによって読み込まれたライブラリ `/s7viewers` コンテキストパス（いわゆる統合 SDK） `include`) をクリックします。 理由は、 `Utils.js` または同様のランタイムビューアライブラリは、ビューアのロジックによって完全に管理され、ビューアのリリースによって位置が変わります。 Adobeは古いバージョンのセカンダリビューアを保持しません `includes` をサーバー上に置きます。
>
>
>その結果、セカンダリ JavaScript への直接参照を配置する `include` ページ上でビューアが使用すると、新しい製品バージョンがデプロイされると、将来ビューア機能が機能しなくなります。

1. コンテナ DIV を定義する。

   ビューアを表示するページに空の DIV 要素を追加します。 DIV 要素の ID は、後でビューア API に渡されるので、定義する必要があります。 DIV のサイズは CSS で指定されます。

   プレースホルダ DIV は配置された要素です。つまり、 `position` CSS プロパティがに設定されている `relative` または `absolute`.

   Internet Explorer で全画面表示機能が正しく機能することを確認します。 DOM 内に、プレースホルダー DIV よりも重ね順の高い要素が他にないことを確認します。

   次に、定義済みのプレースホルダ DIV 要素の例を示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. ビューアサイズの設定

   ビューアの静的サイズを設定するには、次のように宣言します `.s7videoviewer` トップレベルの CSS クラス（絶対単位）、または修飾子を使用 `stagesize`.

   サイズ調整は、HTMLページの CSS で、またはカスタムビューアの CSS ファイルで指定できます。 後でDynamic Media Classic内のビューアプリセットレコードに割り当てられるか、スタイルコマンドを使用して明示的に渡されます。

   詳しくは、 [スマート切り抜きビデオビューアのカスタマイズ](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) を参照してください。

   次に、HTMLページで静的ビューアサイズを定義する例を示します。

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次の設定が可能です。 `stagesize` 修飾子をDynamic Media Classicのビューアプリセットレコードで指定するか、を使用してビューア初期化コードで明示的に渡します。 `params` コレクション。 または、次に示すように、コマンドリファレンスの節で説明する API 呼び出しとして使用できます。

   ```html {.line-numbers}
   smartCropVideoViewer.setParam("stagesize", "640,480");
   ```

   CSS ベースのアプローチを推奨します。この例では、を使用します。

1. ビューアを作成および初期化する。

   上記の手順を完了したら、のインスタンスを作成します。 `s7viewers.SmartCropVideoViewer` クラス、すべての設定情報をコンストラクタに渡し、を呼び出します。 `init()` メソッドを使用して、ビューアインスタンス上に配置できます。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには `containerId` ビューアのコンテナ ID とネストされたコンテナの名前が格納されるフィールド `params` ビューアでサポートされている設定パラメーターを持つ JSON オブジェクト。 この場合、 `params` オブジェクトには、少なくとも `serverUrl` プロパティ、ビデオサーバの URL `videoserverurl` プロパティとして、最初のアセットを `asset` パラメーター。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成し、起動できます。

   ビューアのコンテナを DOM に追加して、ビューアのコードが ID でコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Web ページの終わりまで DOM の構築が遅れます。 互換性を最大限に高めるには、 `init()` 終了直前の方法 `BODY` タグ、または本文 `onload()` イベント。

   同時に、コンテナ要素は必ずしも Web ページレイアウトに含まれているとは限りません。 例えば、 `display:none` スタイルが割り当てられています。 この場合、Web ページでコンテナ要素がレイアウトに戻るまで、ビューアは初期化プロセスを遅延します。 この操作を行うと、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、 `init()` メソッド。 この例では、次の点を前提としています。 `smartCropVideoViewer` はビューアインスタンスです。 `s7viewer` はプレースホルダーの名前です `DIV`, [!DNL http://s7d1.scene7.com/is/image/] は画像サービングの URL で、 [!DNL http://s7d1.scene7.com/is/content/] はビデオサーバーの URL で、 [!DNL html5automation/frisbee-AVS] はアセットです。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   次のコードは、固定サイズのスマート切り抜きビデオビューアを埋め込んだ簡単な Web ページの例です。

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**高さ無制限のレスポンシブデザイン埋め込み**

レスポンシブデザイン埋め込みでは、Web ページには通常、ビューアのコンテナの実行時のサイズを指示する柔軟なレイアウトが指定されています `DIV`. この例では、Web ページがビューアのコンテナを許可しているとします。 `DIV` を使用すると、web ブラウザーのウィンドウサイズの 40%を占め、高さは無制限のままになります。 Web ページのHTMLコードは次のようになります。

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

このようなページにビューアを追加する方法は、固定サイズ埋め込みの場合と似ています。唯一の違いは、ビューアのサイズを明示的に定義する必要がない点です。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナ DIV を定義する。
1. ビューアを作成および初期化する。

上記の手順はすべて、固定サイズ埋め込みの場合と同じです。 コンテナを追加 `DIV` 既存の「所有者」に `DIV`. 次のコードは完全な例です。 ブラウザーのサイズ変更時にビューアのサイズがどのように変化するか、およびビューアの縦横比がアセットとどのように一致するかを確認できます。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実際に使用される例を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[代替のデモの場所](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**幅と高さが定義されたレスポンシブデザイン埋め込み**

幅と高さが定義されたレスポンシブデザイン埋め込みがある場合、Web ページのスタイル設定は異なります。&quot;holder&quot;に両方のサイズを提供します `DIV` ブラウザーウィンドウの中央に配置します。 また、Web ページでは `HTML` および `BODY` 要素を 100%に変更：

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

残りの埋め込み手順は、高さ無制限のレスポンシブデザイン埋め込みと同じです。 結果の例は次のようになります。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**セッターベースの API を使用した埋め込み**

JSON ベースの初期化を使用する代わりに、セッターベースの API と no-args コンストラクターを使用できます。 この API では、コンストラクターはパラメーターを受け取らず、設定パラメーターは `setContainerId()`, `setParam()`、および `setAsset()` API メソッドを個別の JavaScript 呼び出しで使用できます。

次の例は、セッターベースの API を使用した固定サイズ埋め込みを示しています。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer(); 
smartCropVideoViewer.setContainerId("s7viewer"); 
smartCropVideoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
smartCropVideoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
smartCropVideoViewer.setAsset("html5automation/frisbee-AVS"); 
smartCropVideoViewer.init(); 
</script> 
</body> 
</html> 
```
