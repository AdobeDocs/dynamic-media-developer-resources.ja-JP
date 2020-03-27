---
description: 混在メディアビューアはメディアビューアです。 画像、スウォッチセット、スピンセット、ビデオおよびアダプティブビデオセットを含むメディアセットをサポートします。
keywords: responsive
seo-description: 混在メディアビューアはメディアビューアです。 画像、スウォッチセット、スピンセット、ビデオおよびアダプティブビデオセットを含むメディアセットをサポートします。
seo-title: 混在メディア
solution: Experience Manager
title: 混在メディア
topic: Dynamic media
uuid: b6028c54-7a3c-41eb-89f8-7b86bb0d0deb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 混在メディア{#mixed-media}

混在メディアビューアはメディアビューアです。 画像、スウォッチセット、スピンセット、ビデオおよびアダプティブビデオセットを含むメディアセットをサポートします。

ビューアの下部に表示されるサムネールは、各メディアセット要素と、そのアセットタイプインジケータを表します。 スウォッチセット要素を選択すると、スウォッチの別の行が表示され、スウォッチセット内でのカラーのバリエーションの選択が可能になります。 画像とスウォッチセットの要素は、連続モードまたはインラインモードでのズームをサポートしています。スピンセットは、ズームと回転の両方をサポートしています。 ビデオとアダプティブビデオセットは、オプションのクローズドキャプションがビデオコンテンツの上に表示される限り、すべての基本的な再生コントロールをサポートします。 ユーザーは、フルスクリーンボタンをクリックすると、いつでもフルスクリーンに切り替えることができます。 ビューアには、オプションで閉じるボタンがあります。 デスクトップや携帯端末で動作するように設計されています。

混在メディアビューアは、基になるシステムがHLS形式をサポートしている場合は常に、初期設定でHTML5ストリーミングビデオ再生をHLS形式で使用します。 HTML5ストリーミングをサポートしていないシステムでは、ビューアはHTML5プログレッシブビデオ配信にフォールバックします。

>[!NOTE]
>
>IR（画像レンダリング）またはUGC（ユーザ生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアタイプ505

必要システム [構成と前提条件を参照してくださ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)い。

## デモURL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## 混在メディアビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

混在メディアビューアは、メインのJavaScriptファイルと、ビューアによって実行時にダウンロードされるヘルパーファイルのセット（この特定のビューア、アセット、CSSで使用されるすべてのビューアSDKコンポーネントを含む1つのJavaScriptが含まれる）です。

混在メディアビューアは、ISビューアに付属の実稼働用HTMLページを使用して、ポップアップモードで使用できます。 または、ドキュメントに記載されているAPIを使用して、ビューアを埋め込みモードで使用し、ターゲットWebページに統合することもできます。

ビューアの設定とスキン表示のタスクは、他のビューアと同様です。 スキン表示は、すべてカスタムCSSを使用して適用されます。

すべてのビ [ューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 、およびすべ [てのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 混在メディアビューアの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

混在メディアビューアは、他のモバイルアプリケーションで一般的なシングルタッチとマルチタッチのジェスチャに対応しています。 ビューアは、ユーザのスワイプジェスチャを処理できない場合、このイベントをWebブラウザに転送して、ネイティブページスクロールを実行します。 この機能を使用すると、デバイスの画面領域のほとんどをビューアが占めている場合でも、ページ内を移動できます。

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
   <td colname="col2"> <p> フライアウトビューをアクティブにするか、プライマリズームレベルとセカンダリズームレベルを切り替えます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ダブルタップ </p> </td> 
   <td colname="col2"> <p>連続ズームモ <span class="codeph"> ード </span> の場合、最大倍率に達するまで1レベルズームインし、次のダブルタップジェスチャは初期状態にリセットされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>タッチ＆ホールド </p> </td> 
   <td colname="col2"> <p> インラインズーム <span class="codeph"> モード </span> の場合、ズームされた画像をアクティブにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ピンチ </p> </td> 
   <td colname="col2"> <p>連続ズームモードの場合、画像をズームインまたはズームアウトします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> 現在のアセットがスピンセットで、画像がリセット状態の場合、スピンセットを水平方向に回転します。 </p> <p> 現在のアセットがスピンセットまたは画像で、画像がズームインされると、画像が水平方向に移動します。 画像を表示の端まで移動して、その方向で引き続きスワイプを行うと、ネイティブページスクロールが実行されます。 </p> <p> スウォッチバーのスウォッチリストをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直方向のスワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態の場合、多次元スピンセットが使用されている場合は、垂直方向の表示角度が変更されます。 1次元のスピンセットの場合、または複数次元のスピンセットが最後または最初の軸にある場合、垂直方向のスワイプによって垂直方向の表示角度が変わらないように、ネイティブページスクロールが実行されます。 </p> <p> 現在のアセットがスピンセットまたは画像で、画像がズームインされている場合、画像を垂直方向に移動します。 画像を表示の端まで移動して、その方向で引き続きスワイプを行うと、ネイティブページスクロールが実行されます。 </p> <p> スウォッチ領域内でこのジェスチャを行うと、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

また、タッチスクリーンとマウスを使用したWindowsデバイスでは、タッチ入力とマウス入力の両方がサポートされます。 ただし、このサポートは、Chrome、Internet Explorer 11およびEdge Webブラウザーのみに限定されます。

このビューアは完全にキーボードでアクセスできます。

詳しくは、キーボ [ードのアクセシビリティとナビゲーションを参照してくださ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)い。

## 混在メディアビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

Webページが異なると、ビューアの動作に対するニーズが異なります。 Webページをクリックすると、別のブラウザーウィンドウでビューアを開くリンクが表示される場合があります。 ホストページにビューアを直接埋め込む必要がある場合もあります。 後者の場合は、Webページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するため、ビューアでは、次の3つの主要な操作モードがサポートされています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

## ポップアップモードについて {#section-77d5aa03b8b94566958a179b1a2cd474}

ポップアップモードでは、ビューアはWebブラウザーの別のウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやモバイルデバイスの向きが変更された場合は調整されます。

ポップアップモードは、モバイルデバイスで最も一般的なモードです。 Webページでは、JavaScript呼び出し、適切に設定された `window.open()` HTML要素、またはその他の適切な方法を使用し `A` てビューアを読み込みます。

ポップアップ操作モードには、標準搭載されたHTMLページを使用することをお勧めします。 この場合、このISビューアは、とい [!DNL MixedMediaViewer.html] う名前で、標準のISビューアのデプ [!DNL html5/] ロイ先のサブフォルダー内にあります。

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

カスタムCSSを適用すると、視覚的なカスタマイズを行うことができます。

次の例は、ビューアを新しいウィンドウで開くHTMLコードの例です。

```
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## 固定サイズ埋め込みとレスポンシブデザイン埋め込みについて {#section-ec86b100ba5943d0b16694268520bbde}

埋め込みモードでは、ビューアは既存のWebページに追加されます。このWebページには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 ビューアは通常、Webページの一部のスペースのみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、また、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用されます。 これは、静的レイアウトのWebページに最適な選択肢です。

レスポンシブデザイン埋め込みは、コンテナのサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定していま `DIV`す。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナのサイズ変更の方法に応じて、ビューアの動作が異なりま `DIV`す。 Webページでコンテナの幅のみが設定され、高さは無制限のままの場合、 `DIV`ビューアは、使用されるアセットの縦横比に従って高さを自動的に選択します。 この機能により、両側のパディングなしで、アセットが表示範囲にぴったりと収まるようになります。 この使用例は、Bootstrap、Foundationなどのレスポンシブデザインレイアウトフレームワークを使用するWebページで最も一般的です。

それ以外の場合は、Webページでビューアのコンテナの幅と高さの両方が設定されている場合、ビューアはその領域のみを占め、Webページのレイアウトで指定されているサイズに従います。 `DIV`良い例は、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合です。

## 固定サイズ埋め込み {#section-17d162f76ffa4804b27928f51e7bea1d}

ビューアをWebページに追加するには、次の手順を実行します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナの定義を参照してくだ `DIV`さい。
1. ビューアのサイズの設定
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにスクリプトタグを追加する必要があります。 ビューアのAPIを使用する前に、を必ず含めてくださ [!DNL MixedMediaViewer.js]い。 このフ [!DNL MixedMediaViewer.js] ァイルは、次に示すように、 [!DNL html5/js/] 標準のISビューアのデプロイ先のサブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

ビューアがAdobe Scene7サーバの1つにデプロイされ、同じドメインから供給されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobe Scene7サーバの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScriptファイルのみ `include` を参照する必要があります。 Webページコード内の追加のJavaScriptファイルを参照してはなりません。Webページコードは、ビューアのロジックによって実行時にダウンロードされる可能性があります。 特に、ビューアによって読み込まれたHTML5 SDKライブラリを、コ `Utils.js` ンテキストパス(いわゆる統合SDK `/s7viewers` ) `include`から直接参照しないでください。 この理由は、実行時のViewerライブラリの場 `Utils.js` 所がビューアのロジックで完全に管理され、ビューアのリリース間で位置が変わるからです。 アドビでは、古いバージョンのセカンダリViewerをサーバーに保 `includes` 持していません。
>
>
>その結果、新しい製品バージョンがデプロイされると、ビューアで使用さ `include` れるセカンダリJavaScriptへの直接参照をページに配置すると、将来、ビューアの機能が機能しなくなります。

1. コンテナDIVの定義を参照してください。

   ビューアを表示するページに空のDIV要素を追加します。 このIDは後でビューアのAPIに渡されるので、DIV要素のIDを定義する必要があります。 DIVのサイズはCSSで指定されます。

   プレースホルダDIVは、位置固定要素です。つまり、 `position` CSSプロパティがまたはに設定さ `relative` れていま `absolute`す。

   フルスクリーン機能がInternet Explorerで正しく機能することを確認します。 DOM内に、プレースホルダーDIVよりも重ね順の高い要素がないことを確認します。

   プレースホルダDIV要素の定義例を次に示します。

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. ビューアのサイズの設定

   複数項目セットを扱う場合、このビューアにはサムネールが表示されます。 デスクトップシステムでは、サムネールはメインビューの下に配置されます。 同時に、ビューアでは、実行時に `setAsset()` APIを使用してメインアセットを入れ替えることができます。 開発者は、新しいアセットに項目が1つだけ含まれる場合に、下部のサムネール領域をビューアがどのように管理するかを制御できます。 ビューアの外側のサイズはそのままにし、メインビューの高さを拡大して、サムネール領域を表示させることができます。 また、メインビューのサイズを静的に保ち、ビューアの外側の領域を折りたたみ、Webコンテンツを上に移動して、サムネールから残された空きページの領域を使用することもできます。

   ビューアの外側の境界をそのままに保つには、最上位CSSク `.s7mixedmediaviewer` ラスのサイズを絶対単位で定義します。 CSSのサイズ調整は、HTMLページまたはカスタムビューアのCSSファイルに適用できます。このファイルは、後でScene7 Publishing Systemのビューアプリセットレコードに割り当てられるか、styleコマンドを使用して明示的に渡されます。

   CSSを使用した [ビューアのスタイル設定について詳しくは](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) 、混在メディアビューアのカスタマイズを参照してください。

   HTMLページでビューアの外側の静的なサイズを定義する例を次に示します。

   ```
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   ビューアの外側の領域を固定した場合の動作は、次のサンプルページで確認できます。 セットを切り替えても、ビューアの外側のサイズは変わりません。

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html)

   メインビューのサイズを静的にするには、 `Container` SDKコンポーネントの内部のビューアサイズを、 `.s7mixedmediaviewer .s7container` CSSセレクターを使用するか、修飾子を使用して絶対単位で定義 `stagesize` します。

   次の例では、アセットを切り替えてもメインビュー領域のサイズが変わらないように、内部 `Container` SDKコンポーネントのビューアサイズを定義します。

   ```
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次のサンプルページは、メインビューのサイズを固定した場合のビューアの動作を示しています。 セットを切り替えても、メインビューは静的なままで、Webページのコンテンツは垂直方向に移動します。

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html)

   修飾子は、Scene7 Publishing Systemのビ `stagesize` ューアプリセットレコードで設定するか、コレクションを使用してビューア初期化コードで明示的に渡すか、次に示すように、このヘルプの「コマンドリファレンス」の節で説明する `params` API呼び出しとして渡すことができます。

   ```
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   CSSベースのアプローチを推奨し、この例で使用します。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報をコ `s7viewers.MixedMediaViewer` ンストラクターに渡して、ビューアインスタンスでメソッド `init()` を呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアのコンテ `containerId` ナIDの名前と、ビューアがサポートする設定パラメータを含むネストされた `params` JSONオブジェクトを保持するフィールドが必要です。 この場合、オブジェクトには、 `params` 少なくとも、プロパティとして渡された画像サービングURL、プロパティとして渡されたビデ `serverUrl` オサーバーURL、パラメーターとして最初のアセ `videoserverurl` ットが含まれている必要があ `asset` ります。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、起動できます。

   ビューアのコンテナをDOMに追加し、ビューアのコードがIDでコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Webページの最後までDOMの構築が遅れます。 互換性を最大にするには、終了 `init()` タグの直前、またはbodyイベ `BODY` ントでメソッドを呼び出す必要があ `onload()` ります。

   同時に、コンテナ要素は、まだWebページレイアウトの一部ではない必要があります。 例えば、割り当てられたスタイルを使用して非表 `display:none` 示にすることができます。 この場合、Webページがコンテナ要素をレイアウトに戻す瞬間まで、ビューアは初期化処理を遅延します。 この場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、必要最小限の設定オプションをコンストラクターに渡して、メソッドを呼び出 `init()` します。 この例では、がビューアイ `mixedMediaViewer` ンスタンスであると仮定しています。はプレ `s7viewer` ースホルダの名前で `DIV`す。は画 [!DNL http://s7d1.scene7.com/is/image/] 像サービングのURLです。はビ [!DNL http://s7d1.scene7.com/is/content/] デオサーバのURLです。とは [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] アセットです。

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

## 高さ無制限のレスポンシブ埋め込み {#section-056cb574713c4d07be6d07cf3c598839}

レスポンシブデザイン埋め込みでは、Webページには通常、ビューアのコンテナの実行時のサイズを指示する柔軟なレイアウトが指定されていま `DIV`す。 次の例では、WebページでビューアのコンテナがWebブラウザーのウィンドウサイズの40%を取ることを許可し、高さ `DIV` は無制限のままにしているとします。 WebページのHTMLコードは次のようになります。

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

このようなページへのビューアの追加手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、ビューアのサイズを明示的に定義する必要がないことです。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVの定義を参照してください。
1. ビューアを作成し、初期化する。

上記の手順は、固定サイズ埋め込みの場合と同じです。 コンテナDIVを既存の `"holder"` DIVに追加します。 次のコードは完全な例です。 ブラウザのサイズが変更された場合にビューアのサイズが変化し、ビューアの縦横比がアセットと一致することに注目してください。

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

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

## 幅と高さが定義されたフレキシブルサイズ埋め込み {#section-0a329016f9414d199039776645c693de}

幅と高さが定義されたフレキシブルサイズ埋め込みの場合、Webページのスタイルは異なります。 これは、両方のサイズを `"holder"` DIVに提供し、ブラウザーウィンドウの中央に配置します。 また、Webページでは、要素と要素のサイズを100% `HTML` に設 `BODY` 定しています。

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

## セッターベースのAPIを使用した埋め込み {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合、コンストラクターはパラメーターを受け取りません。設定パラメーターは、、、お `setContainerId()`よびAPI `setParam()`メソッドを使用して、 `setAsset()` 別々のJavaScript呼び出しで指定されます。

次の例は、固定サイズ埋め込みとセッターベースのAPIの使用を示しています。

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

