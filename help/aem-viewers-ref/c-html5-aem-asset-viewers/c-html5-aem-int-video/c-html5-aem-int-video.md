---
title: インタラクティブビデオ
description: インタラクティブビデオビューアは、H.264 形式でエンコードされたストリーミングビデオとプログレッシブビデオを再生するビデオプレーヤーです。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2212'
ht-degree: 0%

---

# インタラクティブビデオ{#interactive-video}

インタラクティブビデオビューアは、H.264 形式でエンコードされたストリーミングビデオとプログレッシブビデオを再生するビデオプレーヤーです。

ビューアでは、ビデオコンテンツの横にインタラクティブな製品スウォッチが表示されます。 単一のビデオとアダプティブビデオセットの両方がサポートされています。 デスクトップとモバイル Web ブラウザーの両方で動作し、HTML5 ビデオをサポートするように設計されています。 ビューアは、ビデオコンテンツ、ビデオチャプターナビゲーションおよびソーシャル共有ツールの上に表示されるオプションのクローズドキャプションをサポートしています。 このビューアの目的は、「ショッパブルビデオ」エクスペリエンスを実装する際に役立つことです。 つまり、ユーザーは特定のビデオ時間領域に関連付けられたスウォッチを選択し、顧客の Web サイトのクイックビューまたは製品の詳細ページにリダイレクトされます。

ビューアのタイプは 510 です。

## デモ URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

および

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html)

## システム要件 {#section-b7270cc4290043399681dc504f043609}

詳しくは、 [必要システム構成](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## インタラクティブビデオビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

インタラクティブビデオビューアは、メインの JavaScript ファイルと、ビューアによって実行時にダウンロードされるヘルパーファイルのセットです。 この特定のビューア、アセットおよび CSS で使用されるすべての Viewer SDK コンポーネントには、1 つの JavaScript が含まれています。

インタラクティブビデオビューアは、画像サービングビューアに付属する、実稼動用のHTMLページを使用して、ポップアップモードで使用できます。 また、ドキュメント化された API を使用してターゲット Web ページに統合される埋め込みモードでも使用できます。

設定とスキニングは、このガイドで説明する他のビューアと同様です。 スキニングは、すべてカスタム (CSS) カスケーディングスタイルシートを使用して行います。

詳しくは、 [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## インタラクティブビデオビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

インタラクティブビデオビューアには、再生/一時停止ボタン、ビデオスクラバー、ビデオ時間の吹き出し、再生時間/合計時間インジケーター、ボリューム制御、フルスクリーンボタン、クローズドキャプションの切り替えなど、ビデオ再生用の一連の標準的なユーザーインターフェイスコントロールが用意されています。 これらのコントロールはすべて、メインビューのすぐ下のコントロールバーにグループ化されています。

タッチデバイスでは、デバイスのハードウェアボタンを使用してのみボリュームを制御できるので、ボリュームコントロールはユーザーインターフェイスに表示されません。

ビューアがポップアップモードで動作している場合、ユーザーインターフェイスでフルスクリーンボタンを使用することはできません。

ビューアでは、ビデオ表示領域の右側にインタラクティブスウォッチが表示されるパネルが表示されます。 ビデオの再生時にスウォッチのリストが自動的に進み、現在のビデオ領域に対応するスウォッチが表示されます。 スウォッチをクリックまたはタップすると、トリガー時にそのスウォッチに関連付けられたアクションが作成されます。 設定に応じて、トリガーは Web サイト上の別のページにリダイレクトされる場合があります。 または、製品情報を Web ページロジックに渡す場合もあります。その結果、関連する製品コンテンツを表示するクイックビューを開くトリガーを設定できます。

ビデオチャプターがアクティブになっている場合は、ビデオコンテンツ間をすばやく移動できます。 ビデオチャプターは、ビデオスクラバートラック内にマーカーとして表示され、ロールオーバー時（またはタッチシステムでのシングルタップ時）にチャプタータイトルと説明を表示します。 顧客は、チャプターマーカーをクリックするか、チャプター説明の吹き出しをタップすることで、特定のチャプターを「シーク」できます。

ビューアは、様々なソーシャルメディア共有ツールもサポートしています。 これらは、ユーザーインターフェイスで 1 つのボタンとして使用でき、ユーザーがクリックまたはタップすると、共有ツールバーに展開されます。 共有ツールバーには、Facebook、Twitter、電子メール共有、埋め込みコード共有、リンク共有など、サポートされる共有チャネルの各タイプ用のアイコンが表示されます。 電子メール共有、埋め込み共有またはリンク共有のツールをアクティブにすると、ビューアにモーダルダイアログボックスが表示され、対応するデータ入力フォームが表示されます。 facebookまたはTwitterを呼び出すと、ソーシャルメディアサービスの標準の共有ダイアログボックスにリダイレクトされます。 また、共有ツールが有効になると、ビデオ再生が自動的に一時停止します。 Web ブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは使用できません。

ビューアが完全にキーボードでアクセス可能になる。 詳しくは、 [キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## インタラクティブビデオビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

インタラクティブビデオビューアは、ホスティングページに埋め込まれます。 このような Web ページは、静的レイアウトの場合や、「レスポンシブ」で、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わる場合があります。

これらのニーズに対応するために、ビューアでは、固定サイズ埋め込みとレスポンシブ埋め込みの 2 つの主な操作モードをサポートしています。

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存の Web ページに追加されます。ビューアに関連しない顧客コンテンツが既に存在する場合があります。 ビューアは、通常、Web ページの一部の領域のみを占有します。

主な使用例は、デスクトップやタブレットデバイス向けの Web ページと、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 この機能は、静的レイアウトの Web ページに最適です。

レスポンシブデザイン埋め込みは、コンテナのサイズ変更に応じて実行時にビューアのサイズを変更する必要がある場合を想定しています `DIV`. 最も一般的な使用例は、柔軟なページレイアウトを使用する Web ページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Web ページによるコンテナのサイズ変更の方法によって、ビューアの動作が異なります `DIV`. Web ページでコンテナの幅のみが設定される場合 `DIV`で選択し、高さは無制限のままにし、使用するアセットの縦横比に従って、ビューアによって高さが自動的に選択されます。 この機能により、両側のパディングなしで、アセットが表示に完全に収まります。 この使用例は、Web や Foundation などのレスポンシブ Web デザインレイアウトフレームワークを使用する Web ページで最も一般的です。

それ以外の場合は、Web ページでビューアのコンテナの幅と高さの両方が設定されている場合 `DIV`を指定した場合、ビューアはその領域全体を占め、Web ページのレイアウトに従ってサイズが設定されます。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイが Web ブラウザーのウィンドウサイズに従ってサイズ変更される場合があります。

**固定サイズ埋め込み**

ビューアを Web ページに追加するには、次の手順を実行します。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナの定義 `DIV`.
1. ビューアのサイズを設定します。
1. ビューアを作成および初期化する。

1. ビューアの JavaScript ファイルを Web ページに追加する。

   ビューアを作成するには、HTMLhead にスクリプトタグを追加する必要があります。 ビューア API を使用する前に、必ず [!DNL InterativeVideoViewer.js]. The [!DNL InteractiveVideoViewer.js] ファイルは、 [!DNL html5/js/] 標準の IS-Viewers デプロイメントのサブフォルダー

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

ビューアがいずれかのAdobe Dynamic Media Classicサーバーにデプロイされ、同じドメインから提供されている場合は、相対パスを使用できます。 それ以外の場合は、IS-Viewers がインストールされているAdobe Dynamic Media Classicのいずれかのサーバーへのフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>メインビューアの JavaScript のみを参照します。 `include` ファイルをページに貼り付けます。 実行時にビューアのロジックによってダウンロードされる可能性のある、Web ページコード内の追加の JavaScript ファイルは参照しないでください。 特に、HTML5 SDK を直接参照しないでください `Utils.js` からビューアによって読み込まれたライブラリ `/s7viewers` コンテキストパス（いわゆる統合 SDK） `include`) をクリックします。 理由は、 `Utils.js` または同様のランタイムビューアライブラリは、ビューアのロジックによって完全に管理され、ビューアのリリースによって位置が変わります。 Adobeは古いバージョンのセカンダリビューアを保持しません `includes` をサーバー上に置きます。
>
>
>その結果、セカンダリ JavaScript への直接参照を配置する `include` ページ上でビューアが使用すると、新しい製品バージョンがデプロイされると、将来ビューア機能が機能しなくなります。

1. コンテナの定義 `DIV`.

   空の `DIV` 要素を追加します。 The `DIV` 要素は、その ID が定義されている必要があります。これは、この ID が後でビューア API に渡されるからです。 DIV のサイズは CSS で指定されます。

   プレースホルダー `DIV` は位置固定された要素で、 `position` CSS プロパティがに設定されている `relative` または `absolute`.

   フルスクリーン機能を Internet Explorer で正しく機能させるには、DOM 内に、プレースホルダーよりも重ね順の高い要素が存在しないことを確認します。 `DIV`.

   次に、定義済みのプレースホルダーの例を示します `DIV` 要素：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアサイズの設定

   ビューアの静的サイズを設定するには、次のように宣言します `.s7interactivevideoviewer` トップレベルの CSS クラス ( 絶対単位で、または `stagesize` 修飾子

   サイズ調整は、HTMLページで直接 CSS に配置できます。 または、カスタムビューアの CSS ファイルに配置し、その後、Adobe Experience Manager Assets（オンデマンド）のビューアプリセットレコードに割り当てるか、 `style` コマンドを使用します。

   詳しくは、 [インタラクティブビデオビューアのカスタマイズ](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) を参照してください。

   次に、HTMLページで静的ビューアサイズを定義する例を示します。

   ```html {.line-numbers}
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   次の設定が可能です。 `stagesize` 修飾子がExperience Manager Assets - On-demand のビューアプリセットレコードに表示されます。 または、を使用して、ビューア初期化コードで明示的に渡すこともできます。 `params` コレクション、またはコマンドリファレンスの節で説明されている API 呼び出しとして、次のように指定します。

   ```html {.line-numbers}
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   CSS ベースのアプローチを推奨します。この例では、を使用します。

1. ビューアを作成および初期化する。

   上記の手順を完了したら、のインスタンスを作成します。 `s7viewers.InteractiveVideoViewer` クラス、すべての設定情報をコンストラクタに渡し、を呼び出します。 `init()` メソッドを使用して、ビューアインスタンス上に配置できます。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには `containerId` ビューアのコンテナ ID と入れ子になっているコンテナの名前が格納されるフィールド `params` ビューアでサポートされている設定パラメーターを持つ JSON オブジェクト。

   この場合、 `params` オブジェクトには、少なくとも `serverUrl` プロパティとして、最初のアセットを `asset` パラメーター。 JSON ベースの初期化 API を使用すると、1 行のコードと、として渡されるビデオサーバ URL を使用して、ビューアを作成し、開始できます。 `videoserverurl` プロパティ、初期アセット `asset` パラメーターとしてのインタラクティブデータ `interactivedata` プロパティ。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成し、起動できます。

   ビューアのコンテナを DOM に追加して、ビューアのコードが ID でコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Web ページの終わりまで DOM の構築が遅れます。 互換性を最大限に高めるには、 `init()` 終了直前の方法 `BODY` タグ、または本文 `onload()` イベント。

   同時に、コンテナ要素は必ずしも Web ページレイアウトに含まれているとは限りません。 例えば、 `display:none` スタイルが割り当てられています。 この場合、Web ページでコンテナ要素がレイアウトに戻るまで、ビューアは初期化プロセスを遅延します。 その場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、 `init()` メソッド。 この例では、次のように想定しています。

   * ビューアインスタンスは、 `interactiveVideoViewer`.
   * プレースホルダーの名前 `DIV` 次に該当 `s7viewer`.
   * 画像サービングの URL は `https://aodmarketingna.assetsadobe.com/is/image/`.
   * ビデオサーバーの URL は `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * コンテンツ URL は `https://aodmarketingna.assetsadobe.com/`.
   * アセットは `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`.
   * インタラクティブデータは、 `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`.

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

   次のコードは、固定サイズのインタラクティブビデオビューアを埋め込んだ簡単な Web ページの例です。

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

**高さ無制限のレスポンシブデザイン埋め込み**

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

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実際に使用されている例を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[代替のデモの場所](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**幅と高さが定義されたレスポンシブ埋め込み**

幅と高さが定義されたレスポンシブ埋め込みがある場合、Web ページのスタイル設定は異なります。 次の両方のサイズを `"holder"` DIV を指定し、ブラウザーウィンドウの中央に配置します。 また、Web ページでは `HTML` および `BODY` 要素を 100%に設定します。

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

残りの埋め込み手順は、高さ無制限のレスポンシブ埋め込みに使用した手順と同じです。 結果の例は次のようになります。

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

**セッターベースの API を使用した埋め込み**

JSON ベースの初期化を使用する代わりに、セッターベースの API と no-args コンストラクターを使用できます。 この API コンストラクターを使用する場合は、パラメーターは必要ありません。設定パラメーターは、 `setContainerId()`, `setParam()`、および `setAsset()` API メソッドを個別の JavaScript 呼び出しで使用できます。

次の例は、固定サイズ埋め込みをセッターベースの API で使用する方法を示しています。

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
