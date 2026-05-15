---
title: 混在メディア
description: Mixed Media Viewerは、メディアビューアです。 画像、スウォッチセット、スピンセット、ビデオ、アダプティブビデオセットを含むメディアセットをサポートしています。
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65a54308-f9db-4458-a9c3-ccb1433af43c
TQID: 'https://experienceleague.adobe.com/saAi4CXj7-PIhaQNp5edDBhMtDleYgAf0QbUPmlDExA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 2573
ht-degree: 0%

---

# 混在メディア{#mixed-media}

Mixed Media Viewerは、メディアビューアです。 画像、スウォッチセット、スピンセット、ビデオ、アダプティブビデオセットを含むメディアセットをサポートしています。

ビューアの下部にあるサムネールは、各メディアセット要素とそのアセットタイプインジケーターを表しています。 スウォッチセット要素を選択すると、スウォッチの2行目が表示され、スウォッチセット内のカラーバリエーションを選択できます。 画像とスウォッチセット要素は、連続モードまたはインラインモードでのズームをサポートします。スピンセットは、ズームとスピニングの両方をサポートします。 ビデオとアダプティブビデオセットは、オプションのクローズドキャプションがビデオコンテンツの上に表示されている限り、すべての基本的な再生コントロールをサポートします。 ユーザーは、フルスクリーンボタンをクリックすることで、いつでもフルスクリーンに切り替えることができます。 ビューアにはオプションの「閉じる」ボタンがあります。 デスクトップやモバイルデバイスで動作するように設計されています。

Mixed Media Viewerでは、基盤となるシステムがサポートしている場合は常に、HTML5 ストリーミングビデオ再生をHLS形式でデフォルト設定で使用します。 HTML5 ストリーミングをサポートしていないシステムでは、ビューアはHTML5 プログレッシブビデオ配信にフォールバックします。

>[!NOTE]
>
>IR （画像レンダリング）またはUGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアータイプ 505。

[必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## 混在メディアビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

Mixed Media Viewerは、メインのJavaScript ファイルと一連のヘルパーファイルを表します（1つのJavaScriptには、この特定のビューア、アセット、CSSで使用されるすべてのビューア SDK コンポーネントが含まれます）。実行時にビューアがダウンロードします。

IS-Viewersで提供される実稼動対応のHTML ページを使用して、Mixed Media Viewerをポップアップモードで使用できます。 または、ドキュメント化されたAPIを使用してターゲット web ページに統合する埋め込みモードでビューアを使用することもできます。

ビューアの設定とスキン処理の作業は、他のビューアと同様です。 すべてのスキニングは、カスタム CSSを使用して実行できます。

すべてのビューアに共通する[&#x200B; コマンド参照 – 構成属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通するコマンド参照 – URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください

## Mixed Media Viewerの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Mixed Media Viewerは、他のモバイルアプリケーションで一般的なシングルタッチおよびマルチタッチジェスチャーをサポートしています。 ビューアがユーザーのスワイプジェスチャーを処理できない場合、ネイティブページスクロールを実行するためにイベントをweb ブラウザーに転送します。 この機能を使用すると、ビューアがデバイスの画面領域のほとんどを占めている場合でも、ユーザーはページ内を移動できます。

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
   <td colname="col2"> <p> プライマリとセカンダリのズームレベル間のフライアウトビューまたは変更をアクティブにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ダブルタップ </p> </td> 
   <td colname="col2"> <p><span class="codeph">連続</span> ズームモードの場合、最大倍率に達するまで1 レベルでズームインすると、次のダブルタップジェスチャーが初期状態にリセットされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>タッチ＆ホールド </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> インライン </span> ズーム モードの場合、ズームされた画像がアクティブになります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ピンチ </p> </td> 
   <td colname="col2"> <p>連続ズームモードの場合、画像をズームインまたはズームアウトします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> 現在のアセットがスピンセットで、画像がリセット状態の場合、スピンセットを水平方向に回転します。 </p> <p> 現在のアセットがスピンセットまたは画像で、画像をズームインすると、画像が水平方向に移動します。 画像をビューエッジに移動しても、スワイプがその方向に行われている場合、ジェスチャーはネイティブページスクロールを実行します。 </p> <p> スウォッチバーのスウォッチのリストをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態の場合、多次元スピンセットを使用する場合に備えて、垂直方向の表示角度が変更されます。 1次元スピンセットの場合、または多次元スピンセットが最後または最初の軸にある場合、垂直方向のスワイプによって垂直方向の表示角度が変化しないようにすると、ジェスチャーはネイティブページスクロールを実行します。 </p> <p> 現在のアセットがスピンセットまたは画像で、画像をズームインすると、画像が垂直方向に移動します。 画像をビューエッジに移動しても、スワイプがその方向に行われている場合、ジェスチャーはネイティブページスクロールを実行します。 </p> <p> ジェスチャーがスウォッチ領域内で行われた場合、ネイティブページスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビューアは、タッチスクリーンとマウスを備えたWindows デバイスでのタッチ入力とマウス入力の両方をサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11、およびEdgeのweb ブラウザーのみに限定されます。

このビューアにはキーボードから完全にアクセス可能です。

[&#x200B; キーボードのアクセシビリティとナビゲーション &#x200B;](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## 混在メディアビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

web ページごとに、閲覧者の行動に対するニーズは異なります。 Web ページでリンクが提供される場合があります。このリンクを選択すると、別のブラウザーウィンドウでビューアが開きます。 それ以外の場合は、ビューアをホスティングページに直接埋め込む必要があります。 後者の場合、web ページは静的なページレイアウトを使用するか、異なるデバイスまたは異なるブラウザーウィンドウのサイズに対して異なる表示を行うレスポンシブデザインを使用します。 これらのニーズに対応するために、ビューアでは、ポップアップ、固定サイズの埋め込み、レスポンシブデザインの埋め込みという3つの主要な操作モードをサポートしています。

## ポップアップモードについて {#section-77d5aa03b8b94566958a179b1a2cd474}

ポップアップモードでは、ビューアは別のweb ブラウザーウィンドウまたはタブで開きます。 ブラウザーのサイズが変更されたり、モバイルデバイスの向きが変更されたりすると、ブラウザーのウィンドウ領域全体が調整されます。

ポップアップモードは、モバイルデバイスで最も一般的です。 Web ページは、`window.open()` JavaScript呼び出し、`A` HTML要素の適切な設定、またはその他の適切なメソッドを使用してビューアを読み込みます。

ポップアップ操作モードには、標準のHTML ページを使用することをお勧めします。 この場合は[!DNL MixedMediaViewer.html]と呼ばれ、標準のIS-Viewers デプロイメントの[!DNL html5/] サブフォルダー内にあります。

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

カスタム CSSを適用すると、視覚的なカスタマイズを実現できます。

次に、新しいウィンドウでビューアを開くHTML コードの例を示します。

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## 固定サイズとレスポンシブデザイン埋め込みについて {#section-ec86b100ba5943d0b16694268520bbde}

埋め込みモードでは、ビューアが既存のweb ページに追加されます。このweb ページには、ビューアに関連しない顧客コンテンツが既に含まれている可能性があります。 通常、閲覧者はweb ページの不動産の一部しか占めていません。

主なユースケースは、デスクトップ PCやタブレットデバイス向けのweb ページと、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

初期読み込み後にビューアのサイズが変更されない場合は、固定サイズ埋め込みが使用されます。 このアクションは、静的レイアウトを持つweb ページに最適です。

レスポンシブデザイン埋め込みは、コンテナ `DIV`のサイズ変更に応じて、実行時にビューアのサイズを変更する必要があることを前提としています。 最も一般的なユースケースは、柔軟性の高いページレイアウトを使用するweb ページにビューアを追加することです。

レスポンシブデザイン埋め込みモードでは、web ページのサイズとコンテナ `DIV`のサイズによって、ビューアの動作が異なります。 Web ページがコンテナ `DIV`の幅のみを設定し、高さを制限しない場合、ビューアは使用されるアセットの縦横比に応じて自動的に高さを選択します。 この機能により、側面にパディングすることなく、アセットをビューに完全に収めることができます。 このユースケースは、BootstrapやFoundationなどのレスポンシブデザインレイアウトフレームワークを使用するweb ページで最も一般的です。

それ以外の場合、web ページがビューアのコンテナ `DIV`の幅と高さの両方を設定すると、ビューアはその領域だけを塗りつぶし、web ページレイアウトが提供するサイズに従います。 良い例は、ビューアをモーダルオーバーレイに埋め込むことです。このオーバーレイは、web ブラウザーのウィンドウサイズに応じてサイズが調整されます。

## 固定サイズ埋め込み {#section-17d162f76ffa4804b27928f51e7bea1d}

次の操作を実行して、ビューアをweb ページに追加します。

1. ビューアのJavaScript ファイルをweb ページに追加します。
1. コンテナ `DIV`を定義しています。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. ビューアのJavaScript ファイルをweb ページに追加します。

   ビューアを作成するには、HTML ヘッドにスクリプトタグを追加する必要があります。 ビューアーAPIを使用する前に、[!DNL MixedMediaViewer.js]を含めることを確認してください。 [!DNL MixedMediaViewer.js] ファイルは、標準のIS-Viewers デプロイメントの[!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

ビューアがAdobe Dynamic Media Classic サーバーのいずれかにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-ViewersがインストールされているAdobe Dynamic Media Classic サーバーの1つにフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメイン ビューア JavaScript `include` ファイルのみを参照してください。 実行時にビューアのロジックによってダウンロードされる可能性があるweb ページコード内の他のJavaScript ファイルを参照しないでください。 特に、`/s7viewers` コンテキストパス（いわゆる統合SDK `include`）からビューアによって読み込まれたHTML5 SDK `Utils.js` ライブラリを直接参照しないでください。 その理由は、`Utils.js`または類似のランタイムビューアーライブラリの場所が、ビューアーのロジックによって完全に管理され、ビューアーリリース間で場所が変更されるためです。 Adobeは、古いバージョンのセカンダリビューア `includes`をサーバー上に保持しません。
>
>
>その結果、ビューアがページ上で使用するセカンダリ JavaScript `include`を直接参照すると、新しい製品バージョンがデプロイされる際に、将来的にビューア機能が破損します。

1. コンテナ DIVの定義。

   ビューアを表示するページに、空のDIV エレメントを追加します。 このIDは後でビューア APIに渡されるので、DIV要素にはIDが定義されている必要があります。 DIVのサイズはCSSで指定します。

   プレースホルダーDIVは配置された要素です。`position` CSS プロパティが`relative`または`absolute`に設定されていることを意味します。

   Internet Explorerでフルスクリーン機能が正しく機能することを確認します。 プレースホルダーDIVよりも高い重ね順を持つ要素がDOMにないことを確認します。

   次に、定義済みのプレースホルダーDIV要素の例を示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. ビューアサイズの設定

   このビューアは、複数の項目セットを操作する際にサムネールを表示します。 デスクトップシステムでは、サムネールはメインビューの下に配置されます。 同時に、ビューアでは、`setAsset()` APIを使用して、ランタイム中にメインアセットを入れ替えることができます。 開発者は、新しいアセットが1つのアイテムしか持たない場合に、ビューアが下部のサムネール領域をどのように管理するかを制御できます。 外のビューアのサイズを維持し、メインビューの高さを上げてサムネール領域を占有させることができます。 または、メインビューサイズを静的に保ち、外側のビューア領域を折りたたんで、web ページのコンテンツを上に移動させることもできます。 次に、サムネールから残っている無料ページの不動産を使用します。

   外部ビューアの境界を維持するには、`.s7mixedmediaviewer` トップレベル CSS クラスのサイズを絶対単位で定義します。 CSSでのサイズ変更は、HTML ページまたはカスタムビューア CSS ファイルに配置し、後でDynamic Media Classicのビューアプリセットレコードに割り当てるか、スタイルコマンドを使用して明示的に渡すことができます。

   CSSを使用したビューアのスタイル設定について詳しくは、[混在メディアビューアのカスタマイズ &#x200B;](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4)を参照してください。

   次に、HTML ページの静的外部ビューアサイズを定義する例を示します。

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

<!-- You can see the behavior with a fixed outer viewer area on the following sample page. Notice that when you switch between sets, the outer viewer size does not change:-->

<!--

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html?lang=ja](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html?lang=ja)

-->


メインビューのディメンションを静的にするには、`.s7mixedmediaviewer .s7container` CSS セレクターを使用するか、`stagesize`修飾子を使用して、内部`Container` SDK コンポーネントのビューアーサイズを絶対単位で定義します。

次に、アセットを切り替える際にメインビュー領域のサイズが変更されないように、内部`Container` SDK コンポーネントのビューアーサイズを定義する例を示します。

```html {.line-numbers}
#s7viewer.s7mixedmediaviewer .s7container { 
 width: 640px; 
 height: 480px; 
}
```

<!-- The following sample page shows viewer behavior with a fixed main view size. Notice that when you switch between sets, the main view remains static and the web page content moves vertically: -->

<!--

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html?lang=ja](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html?lang=ja)

   -->

Dynamic Media Classicのビューアプリセットレコードで`stagesize`修飾子を設定するか、`params` コレクションを使用してビューアの初期化コードで明示的に渡すことができます。 または、このヘルプの「コマンドリファレンス」セクションで説明されているように、次のようにAPI呼び出しとして使用します。

```html {.line-numbers}
mixedMediaViewer.setParam("stagesize", "640,480");
```

CSS ベースのアプローチを推奨し、この例で使用します。

1. ビューアの作成と初期化。

   上記の手順を完了したら、`s7viewers.MixedMediaViewer` クラスのインスタンスを作成し、すべての構成情報をそのコンストラクターに渡し、ビューアーインスタンスで`init()` メソッドを呼び出します。 構成情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアコンテナ IDの名前を保持する`containerId` フィールドと、ビューアがサポートする設定パラメーターを含むネストされた`params` JSON オブジェクトが必要です。 この場合、`params` オブジェクトには、少なくとも`serverUrl` プロパティとして渡された画像サービング URL、`videoserverurl` プロパティとして渡されたビデオサーバーURL、`asset` パラメーターとして初期アセットが必要です。 JSON ベースの初期化APIを使用すると、1行のコードでビューアを作成および開始できます。

   ビューアコードがIDでコンテナ要素を見つけられるように、ビューアコンテナをDOMに追加することが重要です。 一部のブラウザーは、Web ページの最後までDOMの構築を遅らせます。 互換性を最大限に高めるには、終了`BODY` タグの直前または本文`onload()` イベントで`init()` メソッドを呼び出します。

   同時に、コンテナ要素は必ずしもweb ページレイアウトの一部であってはなりません。 例えば、割り当てられた`display:none` スタイルを使用して非表示にすることができます。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで初期化プロセスを遅らせます。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

   次に、ビューアーインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡し、`init()` メソッドを呼び出す例を示します。 この例では、`mixedMediaViewer`がビューアーインスタンスであり、`s7viewer`はプレースホルダー`DIV`の名前、[!DNL http://s7d1.scene7.com/is/image/]は画像サービング URL、[!DNL http://s7d1.scene7.com/is/content/]はビデオサーバーのURL、[!DNL Scene7SharedAssets/Mixed_Media_Set_Sample]はアセットであると仮定しています。

```html {.line-numbers}
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

次のコードは、Mixed Media Viewerを固定サイズで埋め込む面倒なweb ページの完全な例です。

```html {.line-numbers}
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

## 高さが制限されないレスポンシブ埋め込み {#section-056cb574713c4d07be6d07cf3c598839}

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

次のサンプルページでは、高さの制限のないレスポンシブデザイン埋め込みをより実際に使用する方法を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--

[Alternate demo location](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=ja)

-->

## 幅と高さが定義された柔軟なサイズ埋め込み {#section-0a329016f9414d199039776645c693de}

幅と高さが定義された柔軟なサイズの埋め込みがある場合、web ページのスタイルが異なります。 `"holder"` DIVに両方のサイズを提供し、ブラウザーウィンドウに中央に配置します。 また、web ページでは、`HTML`要素と`BODY`要素のサイズが100%に設定されています。

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

## Setter ベースのAPIを使用した埋め込み {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

JSON ベースの初期化を使用する代わりに、セッターベースのAPIとno-args コンストラクターを使用できます。 このAPI コンストラクターを使用すると、パラメーターは受け取られず、設定パラメーターは`setContainerId()`、`setParam()`、および`setAsset()` API メソッドを使用して指定され、別々のJavaScript呼び出しが行われます。

次の例は、セッターベースのAPIを使用した固定サイズの埋め込みを使用する方法を示しています。

```html {.line-numbers}
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
