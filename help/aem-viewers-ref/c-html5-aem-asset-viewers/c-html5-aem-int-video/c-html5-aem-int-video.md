---
title: インタラクティブビデオ
description: Interactive Video Viewerは、H.264形式でエンコードされたストリーミングおよびプログレッシブビデオを再生するビデオプレーヤーです。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
TQID: 'https://experienceleague.adobe.com/H3e7HZb3M8vz338CV6xNjROxITz0HLLHz1B5fIiDfWo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 2224
ht-degree: 0%

---

# インタラクティブビデオ{#interactive-video}

Interactive Video Viewerは、H.264形式でエンコードされたストリーミングおよびプログレッシブビデオを再生するビデオプレーヤーです。

ビューアには、ビデオコンテンツの横にインタラクティブな商品スウォッチも表示されます。 シングルビデオとアダプティブビデオセットの両方がサポートされています。 HTML5 ビデオをサポートするデスクトップとモバイルの両方のWeb ブラウザーで動作するように設計されています。 ビューアは、ビデオコンテンツ、ビデオチャプターのナビゲーション、ソーシャル共有ツールの上に表示されるオプションのクローズドキャプションをサポートしています。 このビューアの目的は、「ショッパブルビデオ」エクスペリエンスの実装を支援することです。 つまり、特定のビデオ時間領域に関連付けられたスウォッチを選択すると、顧客のweb サイトのクイックビューまたは製品詳細ページにリダイレクトされます。

ビューアータイプは510です。


## デモ URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--
[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html?lang=ja](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html?lang=ja)
-->

## システム要件 {#section-b7270cc4290043399681dc504f043609}

[必要システム構成](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

## インタラクティブビデオビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

インタラクティブビデオビューアは、メインのJavaScript ファイルと、実行時にビューアがダウンロードした一連のヘルパーファイルを表します。 1つのJavaScriptには、この特定のビューア、アセット、CSSで使用されるすべてのビューア SDK コンポーネントが含まれています。

インタラクティブビデオビューアは、画像サービングビューアが提供する実稼動対応のHTML ページを使用して、ポップアップモードで使用できます。 また、埋め込みモードで使用することもできます。このモードでは、文書化されたAPIを使用して、ターゲットとなるweb ページに統合されます。

設定とスキニングは、このガイドで説明する他のビューアと同様です。 すべてのスキニングは、カスタム（CSS）カスケーディングスタイルシートを使用して実行されます。

すべてのビューアに共通する[&#x200B; コマンド参照 – 構成属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通するコマンド参照 – URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください

## インタラクティブビデオビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

インタラクティブビデオビューアは、再生/一時停止ボタン、ビデオスクラバー、ビデオタイムバブル、再生時間/合計時間インジケーター、ボリュームコントロール、フルスクリーンボタン、クローズドキャプショントグルなど、ビデオ再生のための一連の標準ユーザーインターフェイスコントロールを提供します。 これらのコントロールはすべて、メインビューの直下にあるコントロールバーにグループ化されます。

タッチデバイスでは、ボリューム制御はユーザーインターフェイスから非表示になります。これは、デバイスのハードウェアボタンを使用してのみボリュームを制御できるためです。

ビューアがポップアップモードで動作している場合、ユーザーインターフェイスで全画面ボタンを使用することはできません。

ビューアは、ビデオの表示領域の右側に、インタラクティブなスウォッチを含むパネルを表示します。 スウォッチのリストは、ビデオの再生に合わせて自動的に進むため、現在のビデオ領域に対応するスウォッチが表示されます。 スウォッチをクリックまたはタップすると、オーサー時にそのようなスウォッチに関連付けられたアクションがトリガーされます。 設定方法によっては、トリガーがweb サイトの別のページにリダイレクトされる場合があります。 また、商品データをweb ページロジックに渡して、関連する商品コンテンツを表示するクイックビューをトリガーすることもできます。

ビデオチャプターがアクティブ化されると、ビデオコンテンツを素早くナビゲートできます。 ビデオチャプターは、ビデオスクラブラートラックにマーカーとして表示され、ロールオーバー時（またはタッチシステム上のシングルタップ時）にチャプターのタイトルと説明が表示されます。 お客様は、章マーカーをクリックするか、章説明バブルをタップすることで、特定の章を「シーク」できます。

ビューアは、様々なソーシャルメディア共有ツールもサポートしています。 ユーザーインターフェイスの単一のボタンとして使用でき、ユーザーが共有ツールバーをクリックまたはタップすると、共有ツールバーに展開されます。 共有ツールバーには、Facebook、Twitter、メール共有、埋め込みコード共有、リンク共有など、サポートされている共有チャネルのタイプごとにアイコンが含まれています。 メール共有、埋め込み共有またはリンク共有ツールがアクティブ化されると、対応するデータ入力フォームを含むモーダルダイアログボックスがビューアに表示されます。 FacebookまたはTwitterが呼び出されると、ビューアはソーシャルメディアサービスから標準の共有ダイアログボックスにユーザーをリダイレクトします。 また、共有ツールが有効になっている場合、ビデオの再生は自動的に一時停止されます。 Web ブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは利用できません。

ビューアは完全にキーボードアクセス可能です。 [&#x200B; キーボードのアクセシビリティとナビゲーション &#x200B;](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## インタラクティブビデオビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

インタラクティブビデオビューアは、ホスティングページに埋め込まれています。 このようなweb ページは、静的なレイアウトを持つ場合もあれば、異なるデバイスや異なるブラウザーウィンドウのサイズに対して「レスポンシブ」で異なる表示を行う場合もあります。

これらのニーズに対応するために、ビューアでは、固定サイズ埋め込みとレスポンシブ埋め込みの2つの主要な操作モードをサポートしています。

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアが既存のweb ページに追加されます。このweb ページには、ビューアに関連しない顧客コンテンツが既に含まれている可能性があります。 通常、閲覧者はweb ページの不動産の一部しか占めていません。

主なユースケースは、デスクトップ PCやタブレットデバイス向けのweb ページです。デバイスの種類に応じてレイアウトを自動的に調整する、レスポンシブデザインのページも使用できます。

初期読み込み後にビューアのサイズが変更されない場合は、固定サイズ埋め込みが使用されます。 この機能は、静的レイアウトを持つweb ページに最適です。

レスポンシブデザイン埋め込みは、コンテナ `DIV`のサイズ変更に応じて、実行時にビューアのサイズを変更する必要があることを前提としています。 最も一般的なユースケースは、柔軟性の高いページレイアウトを使用するweb ページにビューアを追加することです。

レスポンシブデザイン埋め込みモードでは、web ページのサイズとコンテナ `DIV`のサイズによって、ビューアの動作が異なります。 Web ページがコンテナ `DIV`の幅のみを設定し、高さを制限しない場合、ビューアは使用されるアセットの縦横比に応じて自動的に高さを選択します。 この機能により、側面にパディングすることなく、アセットをビューに完全に収めることができます。 このユースケースは、BootstrapやFoundationなどのレスポンシブ web デザインレイアウトフレームワークを使用するweb ページで最も一般的です。

それ以外の場合、web ページがビューアのコンテナ `DIV`の幅と高さの両方を設定すると、ビューアはその領域だけを塗りつぶし、web ページレイアウトが提供するサイズに従います。 良い例は、ビューアをモーダルオーバーレイに埋め込むことです。このオーバーレイは、web ブラウザーのウィンドウサイズに応じてサイズが調整されます。

**固定サイズ埋め込み**

次の操作を実行して、ビューアをweb ページに追加します。

1. ビューアのJavaScript ファイルをweb ページに追加します。
1. コンテナ `DIV`を定義しています。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. ビューアのJavaScript ファイルをweb ページに追加します。

   ビューアを作成するには、HTML ヘッドにスクリプトタグを追加する必要があります。 ビューアーAPIを使用する前に、[!DNL InterativeVideoViewer.js]を含めることを確認してください。 [!DNL InteractiveVideoViewer.js] ファイルは、標準のIS-Viewers デプロイメントの[!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

ビューアがAdobe Dynamic Media Classic サーバーのいずれかにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-ViewersがインストールされているAdobe Dynamic Media Classic サーバーの1つにフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメイン ビューア JavaScript `include` ファイルのみを参照してください。 実行時にビューアのロジックによってダウンロードされる可能性があるweb ページコード内の他のJavaScript ファイルを参照しないでください。 特に、`/s7viewers` コンテキストパス（いわゆる統合SDK `include`）からビューアによって読み込まれたHTML5 SDK `Utils.js` ライブラリを直接参照しないでください。 その理由は、`Utils.js`または類似のランタイムビューアーライブラリの場所が、ビューアーのロジックによって完全に管理され、ビューアーリリース間で場所が変更されるためです。 Adobeは、古いバージョンのセカンダリビューア `includes`をサーバー上に保持しません。
>
>
>その結果、ビューアがページ上で使用するセカンダリ JavaScript `include`を直接参照すると、新しい製品バージョンがデプロイされる際に、将来的にビューア機能が破損します。

1. コンテナ `DIV`を定義しています。

   ビューアを表示するページに、空の`DIV`要素を追加します。 このIDは後でビューア APIに渡されるので、`DIV`要素にはIDが定義されている必要があります。 DIVのサイズはCSSで指定します。

   プレースホルダー`DIV`は配置された要素です。`position` CSS プロパティが`relative`または`absolute`に設定されていることを意味します。

   Internet Explorerでフルスクリーン機能が正しく機能するには、プレースホルダー`DIV`よりも高い重ね順を持つ要素がDOMにないことを確認してください。

   次に、定義済みのプレースホルダー`DIV`要素の例を示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアサイズの設定

   ビューアの静的サイズは、`.s7interactivevideoviewer` トップレベル CSS クラスを絶対単位で宣言するか、`stagesize`修飾子を使用することで設定できます。

   CSSで直接HTML ページにサイズを設定できます。 または、カスタムのビューア CSS ファイルに配置して、後でAdobe Experience Manager Assets オンデマンドのビューアプリセットレコードに割り当てるか、`style` コマンドを使用して明示的に渡すことができます。

   CSSを使用したビューアのスタイル設定について詳しくは、[&#x200B; インタラクティブビデオビューアのカスタマイズ &#x200B;](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)を参照してください。

   次に、HTML ページで静的ビューアサイズを定義する例を示します。

   ```html {.line-numbers}
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Experience Manager Assets - オンデマンドのビューアプリセットレコードで`stagesize`修飾子を設定できます。 または、`params` コレクションを持つビューアの初期化コードを使用して明示的に渡すことも、コマンドリファレンスの節で説明されているようにAPI呼び出しとして渡すこともできます。例えば、次のようになります。

   ```html {.line-numbers}
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   CSS ベースのアプローチを推奨し、この例で使用します。

1. ビューアの作成と初期化。

   上記の手順を完了したら、`s7viewers.InteractiveVideoViewer` クラスのインスタンスを作成し、すべての構成情報をそのコンストラクターに渡し、ビューアーインスタンスで`init()` メソッドを呼び出します。 構成情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアコンテナ IDの名前を保持する`containerId` フィールドと、ビューアでサポートされている設定パラメーターを含むネストされた`params` JSON オブジェクトが必要です。

   この場合、`params` オブジェクトには、少なくとも`serverUrl` プロパティとして渡された画像サービング URLと、`asset` パラメーターとして最初のアセットが必要です。 JSON ベースの初期化APIを使用すると、1行のコード、ビデオサーバーのURLが`videoserverurl` プロパティとして渡され、初期アセットが`asset` パラメーターとして渡され、インタラクティブデータが`interactivedata` プロパティとしてビューアを作成および開始できます。 JSON ベースの初期化APIを使用すると、1行のコードでビューアを作成および開始できます。

   ビューアコードがIDでコンテナ要素を見つけられるように、ビューアコンテナをDOMに追加することが重要です。 一部のブラウザーは、Web ページの最後までDOMの構築を遅らせます。 互換性を最大限に高めるには、終了`BODY` タグの直前または本文`onload()` イベントで`init()` メソッドを呼び出します。

   同時に、コンテナ要素はまだ必ずしもweb ページレイアウトの一部ではありません。 例えば、割り当てられた`display:none` スタイルを使用して非表示にすることができます。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで初期化プロセスを遅らせます。 何が起こっても、ビューアの読み込みは自動的に再開されます。

   次に、ビューアインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡して`init()` メソッドを呼び出す例を示します。 この例では、次の条件が適用されます。

   * ビューアーインスタンスは`interactiveVideoViewer`です。
   * プレースホルダー`DIV`の名前は`s7viewer`です。
   * 画像サービング URLは`https://aodmarketingna.assetsadobe.com/is/image/`です。
   * ビデオサーバーのURLは`https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`です。
   * コンテンツ URLは`https://aodmarketingna.assetsadobe.com/`です。
   * アセットは`/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`です。
   * インタラクティブ データは`is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`です。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、インタラクティブビデオビューアを固定サイズで埋め込む面倒なweb ページの完全な例です。

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;"></div> 
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高さの制限のないレスポンシブデザイン埋め込み**

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
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

次のサンプルページでは、高さの制限のないレスポンシブデザイン埋め込みをより実際に使用する方法を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--

[Alternate demo location](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=ja)

-->

**幅と高さが定義されたレスポンシブ埋め込み**

幅と高さが定義されたレスポンシブ埋め込みがある場合、web ページのスタイル設定は異なります。 `"holder"` DIVに両方のサイズを提供し、ブラウザーウィンドウの中央に配置します。 また、web ページでは、`HTML`要素と`BODY`要素のサイズが100%に設定されています。

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

残りの埋め込み手順は、高さの制限のないレスポンシブ埋め込みに使用する手順と同じです。 結果として得られる例は次のとおりです。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Setter ベースのAPIを使用した埋め込み**

JSON ベースの初期化を使用する代わりに、セッターベースのAPIとno-args コンストラクターを使用できます。 このAPI コンストラクターを使用すると、パラメーターは受け取られず、設定パラメーターは`setContainerId()`、`setParam()`、`setAsset()`のAPI メソッドを使用して指定され、別々のJavaScript呼び出しが行われます。

次の例は、セッターベースのAPIで固定サイズの埋め込みを使用する方法を示しています。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactivevideoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer(); 
interactiveVideoViewer.setContainerId("s7viewer"); 
interactiveVideoViewer.setParam("config", "/etc/dam/presets/viewer/Shoppable_Video_Dark"); 
interactiveVideoViewer.setParam("serverurl", "https://aodmarketingna.assetsadobe.com/is/image/"); 
interactiveVideoViewer.setParam("videoserverurl", "https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna"); 
interactiveVideoViewer.setParam("contenturl", "https://aodmarketingna.assetsadobe.com/"); 
interactiveVideoViewer.setParam("interactivedata", "is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt"); 
interactiveVideoViewer.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4"); 
interactiveVideoViewer.init(); 
</script> 
</body> 
</html>
```
