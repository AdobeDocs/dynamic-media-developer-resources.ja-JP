---
description: 混在メディアビューアはメディアビューアです。 このビューアは、画像、スウォッチセット、スピンセット、ビデオ、アダプティブビデオセットを含むメディアセットをサポートしています。
keywords: responsive
seo-description: 混在メディアビューアはメディアビューアです。 このビューアは、画像、スウォッチセット、スピンセット、ビデオ、アダプティブビデオセットを含むメディアセットをサポートしています。
seo-title: 混在メディア
solution: Experience Manager
title: 混在メディア
topic: Dynamic media
uuid: b6028c54-7a3c-41eb-89f8-7b86bb0d0deb
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2681'
ht-degree: 0%

---


# 混在メディア{#mixed-media}

混在メディアビューアはメディアビューアです。 このビューアは、画像、スウォッチセット、スピンセット、ビデオ、アダプティブビデオセットを含むメディアセットをサポートしています。

ビューアの下部に表示されるサムネールは、各メディアセット要素を表し、そのアセットタイプインジケータと共に表します。 スウォッチセット要素を選択すると、スウォッチの別の行が表示され、スウォッチセット内のカラーバリエーションを選択できるようになります。 画像とスウォッチセット要素は、連続モードまたはインラインモードでのズームをサポートしています。スピンセットでは、ズームと回転の両方がサポートされています。 ビデオとアダプティブビデオセットは、オプションのクローズドキャプションがビデオコンテンツの上部に表示される限り、すべての基本的な再生コントロールをサポートします。 ユーザーは、フルスクリーンボタンをクリックすると、いつでもフルスクリーンに切り替えることができます。 ビューアにはオプションの閉じるボタンがあります。 デスクトップおよびモバイルデバイスで動作するように設計されています。

混在メディアビューアは、基になるシステムがHLS形式をサポートしている場合は常に、初期設定でHLS形式のHTML5ストリーミングビデオ再生を使用します。 HTML5ストリーミングをサポートしていないシステムでは、ビューアはHTML5プログレッシブビデオ配信にフォールバックされます。

>[!NOTE]
>
>IR（画像レンダリング）またはUGC（ユーザ生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアタイプ505

[必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

## デモURL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## 混在メディアビューアの使用{#section-f21ac23d3f6449ad9765588d69584772}

混在メディアビューアは、メインのJavaScriptファイルと、ビューアによって実行時にダウンロードされるヘルパーファイルのセット（この特定のビューア、アセット、CSSで使用されるすべてのビューアSDKコンポーネントを含む1つのJavaScriptインクルード）です。

混在メディアビューアは、ISビューアに付属の、運用に対応しているHTMLページを使用して、ポップアップモードで使用できます。 または、ドキュメントに記載されているAPIを使用してターゲットのWebページに統合されたビューアを埋め込みモードで使用できます。

ビューアの設定とスキン表示のタスクは、他のビューアと同様です。 スキン表示はすべて、カスタムCSSを使用して適用します。

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)と[すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください。

## 混在メディアビューアの操作{#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

混在メディアビューアは、他のモバイルアプリケーションで一般的なシングルタッチとマルチタッチのジェスチャに対応しています。 ビューアでユーザーのスワイプジェスチャを処理できない場合、イベントはWebブラウザーに転送され、ネイティブページスクロールが実行されます。 この機能を使用すると、デバイスの画面領域のほとんどをビューアが占めている場合でも、ユーザーはページ内を移動できます。

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
   <td colname="col2"> <p> フライアウト表示をアクティブにするか、プライマリズームレベルとセカンダリズームレベルを切り替えます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>重複タップ </p> </td> 
   <td colname="col2"> <p><span class="codeph">連続</span>ズームモードで、最大倍率に達するまで1レベルズームインした場合、次の重複タップジェスチャは初期状態にリセットされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>タッチ＆ホールド </p> </td> 
   <td colname="col2"> <p> <span class="codeph">インライン</span>ズームモードの場合、ズームされた画像をアクティブにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ピンチ </p> </td> 
   <td colname="col2"> <p>連続ズームモードの場合、画像をズームインまたはズームアウトします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> 現在のアセットがスピンセットで、画像がリセット状態の場合、スピンセットを水平方向にスピンします。 </p> <p> 現在のアセットがスピンセットまたは画像で、画像がズームインされている場合、画像を水平方向に移動します。 画像を表示の端まで移動して、その方向で引き続きスワイプを実行すると、ネイティブページスクロールが実行されます。 </p> <p> スウォッチバー内のスウォッチのリストをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直方向のスワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> 多次元のスピンセットが使用されている場合は、画像がリセット状態の場合に垂直方向の表示角度が変更されます。 1次元のスピンセットの場合、または多次元のスピンセットが最後または最初の軸にある場合は、垂直方向のスワイプによって垂直方向の表示角度が変わらないように、ネイティブページスクロールが実行されます。 </p> <p> 現在のアセットがスピンセットまたは画像で、画像がズームインされている場合、画像を垂直方向に移動します。 画像を表示の端まで移動して、その方向で引き続きスワイプを実行すると、ネイティブページスクロールが実行されます。 </p> <p> スウォッチ領域内でこのジェスチャを行うと、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

また、タッチスクリーンとマウスを備えたWindowsデバイスでは、タッチ入力とマウス入力の両方がサポートされています。 ただし、このサポートは、Chrome、Internet Explorer 11およびEdgeのWebブラウザーにのみ制限されます。

このビューアは完全にキーボードでアクセスできます。

[キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## 混在メディアビューアの埋め込み{#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Webページごとに異なります。 Webページにリンクが表示される場合があります。リンクをクリックすると、別のブラウザーウィンドウでビューアが開きます。 ホストページの右側にビューアを埋め込む必要がある場合もあります。 後者の場合は、Webページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは主に次の3つの操作モードがサポートされています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

## ポップアップモードについて{#section-77d5aa03b8b94566958a179b1a2cd474}

ポップアップモードでは、ビューアはWebブラウザーの別のウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやモバイルデバイスの向きが変わった場合は調整されます。

ポップアップモードは、モバイルデバイスで最も一般的なモードです。 Webページでは、`window.open()` JavaScript呼び出し、適切に設定された`A` HTML要素またはその他の適切な方法を使用してビューアを読み込みます。

ポップアップ操作モードには、標準搭載されたHTMLページを使用することをお勧めします。 この場合、このページは[!DNL MixedMediaViewer.html]という名前で、標準のIS-Viewersデプロイメントの[!DNL html5/]サブフォルダー内にあります。

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

カスタムCSSを適用すると、視覚的なカスタマイズを行うことができます。

次の例は、ビューアを新しいウィンドウに開くHTMLコードの例です。

```
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## 固定サイズ埋め込みとレスポンシブデザイン埋め込みについて{#section-ec86b100ba5943d0b16694268520bbde}

埋め込みモードでは、ビューアは既存のWebページに追加されます。このWebページには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 ビューアは通常、Webページの一部のスペースのみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、また、デバイスの種類に従ってレイアウトを自動調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 静的レイアウトのWebページには、これが最適です。

レスポンシブデザイン埋め込みは、コンテナ`DIV`のサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定しています。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナのサイズ変更の方法`DIV`によって、ビューアの動作が異なります。 Webページでコンテナ`DIV`の幅のみが設定され、高さは無制限のままの場合、ビューアでは、使用するアセットの縦横比に従って高さが自動的に選択されます。 この機能により、両側のパディングなしで、アセットは表示にぴったりと収まります。 この使用例は、Bootstrap、Foundationなどのレスポンシブデザインレイアウトフレームワークを使用するWebページで最も一般的です。

それ以外の場合は、Webページでビューアのコンテナ`DIV`の幅と高さの両方が設定されている場合、ビューアはその領域を占め、Webページのレイアウトに指定されているサイズに従います。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合があります。

## 固定サイズ埋め込み{#section-17d162f76ffa4804b27928f51e7bea1d}

ビューアは、次の操作を行ってWebページに追加します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナ`DIV`を定義しています。
1. ビューアのサイズを設定する。
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにスクリプトタグを追加する必要があります。 ビューアのAPIを使用するには、[!DNL MixedMediaViewer.js]を必ず含めます。 [!DNL MixedMediaViewer.js]ファイルは、次に示すように、IS-Viewersの標準のデプロイ先の[!DNL html5/js/]サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

ビューアをAdobe Scene7サーバの1つにデプロイし、同じドメインから供給している場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobe Scene7サーバーの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScript `include`ファイルのみを参照してください。 Webページコード内で、ビューアのロジックによって実行時にダウンロードされる可能性のある追加のJavaScriptファイルは、参照しないでください。 特に、ビューアによって読み込まれたHTML5 SDK `Utils.js`ライブラリを`/s7viewers`コンテキストパスから直接参照しないでください（いわゆる統合SDK `include`）。 理由は、`Utils.js`や類似のランタイムビューアライブラリの場所がビューアのロジックで完全に管理され、ビューアのリリース間で場所が変化するからです。 Adobeでは、古いバージョンのセカンダリビューア`includes`はサーバに保持されません。
>
>
>その結果、新しい製品バージョンがデプロイされる際に、ビューアが使用する任意のセカンダリJavaScript `include`への直接参照をページ上に置くと、ビューアの機能が将来的に機能しなくなります。

1. コンテナDIVを定義する。

   ビューア追加を表示するページの空のDIV要素。 DIV要素は、IDが定義されている必要があります。このIDを、後でビューアのAPIに渡します。 DIVのサイズはCSSで指定します。

   プレースホルダDIVは位置固定要素です。つまり、`position` CSSプロパティは`relative`または`absolute`に設定されます。

   フルスクリーン機能がInternet Explorerで正しく機能することを確認します。 プレースホルダDIVよりも重ね順の高い他の要素がDOM内にないことを確認します。

   プレースホルダDIV要素の定義例を次に示します。

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. ビューアのサイズの設定

   複数項目セットを処理する場合、このビューアにはサムネールが表示されます。 デスクトップシステムでは、サムネールはメイン表示の下に配置されます。 同時に、ビューアでは、実行時に`setAsset()` APIを使用してメインアセットを入れ替えることができます。 開発者は、新しいアセットの項目が1つだけの場合に、下部のサムネール領域をビューアがどのように管理するかを制御できます。 ビューアの外側のサイズはそのままにし、メイン表示の高さを拡大して、サムネール領域を表示させることができます。 また、メイン表示のサイズを静的に保ってビューアの外側の領域を折りたたみ、Webコンテンツを上に移動して、サムネールから残されたページの空き領域を使用することもできます。

   ビューアの外側の境界をそのまま残すには、最上位CSSクラス`.s7mixedmediaviewer`のサイズを絶対単位で定義します。 CSS内のサイズ調整は、HTMLページまたはカスタムビューアのCSSファイルに適用できます。このCSSファイルは、後でScene7パブリッシングシステムでビューアプリセットレコードに割り当てるか、styleコマンドを使用して明示的に渡します。

   CSSでのビューアのスタイル設定について詳しくは、[混在メディアビューアのカスタマイズ](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4)を参照してください。

   以下は、HTMLページでビューアの外側の静的なサイズを定義する例です。

   ```
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   以下のサンプルページでは、ビューアの外側の領域を固定した場合の動作を確認できます。 セットを切り替えても、ビューアの外側のサイズは変わりません。

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html)

   メイン表示のサイズを静的にするには、`.s7mixedmediaviewer .s7container` CSSセレクターを使用するか、`stagesize`修飾子を使用して、内部の`Container` SDKコンポーネントのビューアサイズを絶対単位で定義します。

   次の例では、アセットを切り替えてもメイン表示領域のサイズが変更されないように、内部の`Container` SDKコンポーネントのビューアサイズを定義します。

   ```
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   以下のサンプルページは、メイン表示のサイズを固定した場合のビューアの動作を示しています。 セットを切り替えてもメイン表示は静的なままで、Webページのコンテンツは垂直方向に移動します。

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html)

   `stagesize`修飾子は、Scene7Publishing Systemのビューアプリセットレコードに設定するか、`params`コレクションを使用してビューア初期化コードで明示的に渡すか、次のように、このヘルプの「コマンドリファレンス」で説明するAPI呼び出しとして渡すことができます。

   ```
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   CSSベースのアプローチを推奨し、この例では使用します。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、`s7viewers.MixedMediaViewer`クラスのインスタンスを作成し、すべての設定情報をコンストラクターに渡して、ビューアインスタンスで`init()`メソッドを呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 最低でも、このオブジェクトには`containerId`フィールドが存在し、ビューアのコンテナIDの名前と、ビューアによってサポートされる設定パラメーターを含むネストされた`params` JSONオブジェクトが含まれている必要があります。 この場合、`params`オブジェクトには、`serverUrl`プロパティとして渡された画像サービングURL、`videoserverurl`プロパティとして渡されたビデオサーバーURL、および`asset`パラメーターとしての初期アセットが少なくとも含まれている必要があります。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、開始できます。

   ビューアのコンテナをDOMに追加して、ビューアのコードがIDでコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Webページが終わるまでDOMの構築が遅れます。 互換性を最大にするには、`init()`メソッドを終了`BODY`タグの直前、または本文`onload()`イベントで呼び出します。

   同時に、コンテナ要素がまだWebページレイアウトの一部である必要はありません。 例えば、`display:none`スタイルを割り当てて非表示にすることができます。 この場合、Webページからコンテナ要素がレイアウトに戻る瞬間まで、ビューアは初期化プロセスを遅延します。 この場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、`init()`メソッドを呼び出します。 この例では、`mixedMediaViewer`をビューアインスタンスと仮定しています。`s7viewer`はプレースホルダー`DIV`の名前です。[!DNL http://s7d1.scene7.com/is/image/]は画像サービングのURL;[!DNL http://s7d1.scene7.com/is/content/]はビデオサーバーのURLです。[!DNL Scene7SharedAssets/Mixed_Media_Set_Sample]はアセットです。

```
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
<script type="text/javascript"> 
mixedMediaViewer.init(); 
</script>
```

次のコードは、固定サイズの混在メディアビューアを埋め込んだ簡単なWebページの例です。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## 高さ無制限のレスポンシブ埋め込み{#section-056cb574713c4d07be6d07cf3c598839}

レスポンシブデザイン埋め込みでは、Webページには通常、ビューアのコンテナ`DIV`の実行時のサイズを指示する柔軟なレイアウトが指定されています。 次の例では、Webページでビューアのコンテナ`DIV`がWebブラウザーのウィンドウサイズの40%を占めることを許可し、高さは無制限のままにすると仮定します。 WebページのHTMLコードは次のようになります。

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

このようなページへのビューアの追加手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、ビューアサイズを明示的に定義する必要がないことです。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVを定義する。
1. ビューアを作成し、初期化する。

上記の手順はすべて、固定サイズ埋め込みの場合と同じです。 コンテナ追加DIVを既存の`"holder"` DIVに置きます。 次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化すること、ビューアの縦横比がアセットと一致することに注目してください。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用方法を説明しています。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## 幅と高さが定義されたフレキシブルサイズ埋め込み{#section-0a329016f9414d199039776645c693de}

幅と高さが定義されたフレキシブルサイズ埋め込みの場合、Webページのスタイルは異なります。 `"holder"` DIVに両方のサイズを提供し、ブラウザーウィンドウの中央に配置します。 また、Webページでは、`HTML`要素と`BODY`要素のサイズを100%に設定します。

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

残りの埋め込み手順は、高さ無制限のレスポンシブデザイン埋め込みで使用した手順と同じです。 結果の例を次に示します。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## セッターベースのAPIを使用した埋め込み{#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合、コンストラクターにパラメーターは不要です。設定パラメーターは、`setContainerId()`、`setParam()`および`setAsset()`の各APIメソッドを使用して、別々のJavaScript呼び出しで指定します。

以下の例は、固定サイズ埋め込みとセッターベースのAPIを使用する場合を説明しています。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer(); 
mixedMediaViewer.setContainerId("s7viewer"); 
mixedMediaViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
mixedMediaViewer.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample"); 
mixedMediaViewer.init(); 
</script> 
</body> 
</html>
```

