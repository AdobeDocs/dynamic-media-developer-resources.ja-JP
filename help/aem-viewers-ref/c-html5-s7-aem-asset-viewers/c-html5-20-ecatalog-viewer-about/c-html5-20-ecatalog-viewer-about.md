---
description: eCatalogビューアは、見開き別またはページ別の見開き別に電子パンフレットを表示するカタログビューアです。eCatalogを使用すると、ユーザーは追加のユーザーインターフェイス要素または専用のサムネールモードを使用してカタログ内を移動できます。 また、各ページでズームインして詳細を確認することもできます。
keywords: responsive
seo-description: eCatalogビューアは、見開き別またはページ別の見開き別に電子パンフレットを表示するカタログビューアです。eCatalogを使用すると、ユーザーは追加のユーザーインターフェイス要素または専用のサムネールモードを使用してカタログ内を移動できます。 また、各ページでズームインして詳細を確認することもできます。
seo-title: eCatalog
solution: Experience Manager
title: eCatalog
topic: Dynamic media
uuid: 6950306d-637e-4932-ae96-c5366e5477f3
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2212'
ht-degree: 0%

---


# eCatalog{#ecatalog}

eCatalogビューアは、見開き別またはページ別の見開き別に電子パンフレットを表示するカタログビューアです。eCatalogを使用すると、ユーザーは追加のユーザーインターフェイス要素または専用のサムネールモードを使用してカタログ内を移動できます。 また、各ページでズームインして詳細を確認することもできます。

>[!NOTE]
>
>画像レンダリング(IR)またはユーザ生成コンテンツ(UGC)を使用する画像は、このビューアではサポートされていません。

ビューアタイプ507

[必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

このビューアはeCatalogで機能します。また、オプションの画像マップとソーシャル共有ツールがサポートされます。 このビューアには、ズームツール、カタログナビゲーションツール、フルスクリーンのサポート、サムネール、およびオプションの閉じるボタンがあります。 Viewerは、ソーシャル共有ツール、印刷、ダウンロード、およびお気に入りもサポートしています。 デスクトップおよびモバイルデバイスで動作するように設計されています。

## デモURL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist](http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist)

## eCatalogビューアの使用{#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalogビューアは、メインのJavaScriptファイルと、ビューアによって実行時にダウンロードされるヘルパーファイルのセット（この特定のビューアで使用されるすべてのビューアSDKコンポーネントが含まれる1つのJavaScriptインクルード、アセット、CSS）です

eCatalogビューアは、ISビューアに付属の運用に対応しているHTMLページを使用するか、埋め込みモードで使用できます。このモードでは、ドキュメントに記述のあるAPIを使用してターゲットのWebページに統合されます。

設定とスキン表示は、他のビューアと同様です。 スキン表示はすべて、カスタムCSSを使用して適用します。

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)と[すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください。

## eCatalogビューアの操作{#section-642e66ca38cd4032992840ec6c0b0cd2}

eCatalogビューアでは、他のモバイルアプリケーションで一般的な以下のタッチジェスチャに対応しています。

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
   <td colname="col2"> <p> スウォッチ内で新しいサムネールを選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>重複タップ </p> </td> 
   <td colname="col2"> <p> 最大の倍率に達するまで、1レベルズームインします。 次の重複タップジェスチャを行うと、ビューアが初期の表示状態にリセットされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ピンチ </p> </td> 
   <td colname="col2"> <p>ズームインまたはズームアウトします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> スライドフレームトランジションを使用している場合に、カタログページのリストをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直方向のスワイプまたはフリック </p> </td> 
   <td colname="col2"> <p>画像がリセット状態の場合に、ネイティブページスクロールを実行します。 </p> <p>サムネールがアクティブな場合、サムネールのリストをスクロールします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

カタログページ間を移動する際のリアルなページフリップアニメーション効果を有効にすることができます。 このような場合、ユーザーはページの隅をドラッグしてページをめくることができます。

このビューアは、タッチスクリーンとマウスを備えたWindowsデバイスでも、タッチ入力とマウス入力の両方をサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11およびEdgeのWebブラウザーにのみ制限されます。

このビューアは、[キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)の説明に従って、完全にキーボードからアクセスできます。

## eCatalogビューアを使用したソーシャルメディア共有ツール{#section-eb575084a99647c3a9591f439f40b412}

eCatalogビューアでは、ソーシャルシェアツールがサポートされています。ソーシャルシェアツールは、メインコントロールバーのボタンとして使用でき、ユーザーがクリックまたはタップすると共有ツールバーに表示されます。

共有ツールバーには、サポートされる共有チャネルのタイプ別に、Facebook、Twitter、電子メール共有、埋め込みコード共有、リンク共有などのアイコンが表示されます。 電子メール共有、埋め込み共有またはリンク共有のツールをアクティブにすると、ビューアにモーダルダイアログボックスが開き、対応するデータ入力フォームが表示されます。 FacebookまたはTwitterを呼び出すと、ソーシャルサービスの標準の共有ダイアログにリダイレクトされます。 Webブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは使用できません。

## eCatalogビューアの埋め込み{#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Webページごとに異なります。 Webページにリンクが表示される場合があります。リンクをクリックすると、別のブラウザーウィンドウでビューアが開きます。 ホストページの右側にビューアを埋め込む必要がある場合もあります。 後者の場合は、Webページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは主に次の3つの操作モードがサポートされています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

**ポップアップモードについて**

ポップアップモードでは、ビューアはWebブラウザーの別のウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやモバイルデバイスの向きが変わった場合は調整されます。

ポップアップモードは、モバイルデバイスで最も一般的なモードです。 Webページでは、`window.open()` JavaScript呼び出し、適切に設定された`A` HTML要素またはその他の適切な方法を使用してビューアを読み込みます。

ポップアップ操作モードには、標準搭載されたHTMLページを使用することをお勧めします。 この場合、このページは[!DNL eCatalogViewer.html]という名前で、標準のIS-Viewersデプロイメントの[!DNL html5/]サブフォルダー内にあります。

[!DNL <s7viewers_root>/html5/eCatalogViewer.html]

カスタムCSSを適用すると、視覚的なカスタマイズを行うことができます。

次の例は、ビューアを新しいウィンドウに開くHTMLコードの例です。

```
<a href="http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存のWebページに追加されます。このWebページには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 ビューアは通常、Webページの一部のスペースのみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、また、デバイスの種類に従ってレイアウトを自動調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 静的レイアウトのWebページには、これが最適です。

レスポンシブデザイン埋め込みは、コンテナ`DIV`のサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定しています。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナのサイズ変更の方法`DIV`によって、ビューアの動作が異なります。 Webページでコンテナ`DIV`の幅のみが設定され、高さは無制限のままの場合、ビューアでは、使用するアセットの縦横比に従って高さが自動的に選択されます。 この機能により、両側のパディングなしで、アセットは表示にぴったりと収まります。 この使用例は、Bootstrap、Foundationなどのレスポンシブレイアウトフレームワークを使用するWebページで最も一般的です。

それ以外の場合は、Webページでビューアのコンテナ`DIV`の幅と高さの両方が設定されている場合、ビューアはその領域を占め、Webページのレイアウトに指定されているサイズに従います。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合があります。

**固定サイズ埋め込み**

ビューアは、次の操作を行ってWebページに追加します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVを定義する。
1. ビューアのサイズを設定する。
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにスクリプトタグを追加する必要があります。 ビューアのAPIを使用するには、[!DNL eCatalogViewer.js]を必ず含めます。 [!DNL eCatalogViewer.js]ファイルは、次に示すように、IS-Viewersの標準のデプロイ先の[!DNL html5/js/]サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/eCatalogViewer.js]

ビューアがAdobeのDynamic Mediaクラシックサーバの1つにデプロイされ、同じドメインから供給されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobeDynamic Mediaクラシックサーバの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScript `include`ファイルのみを参照してください。 Webページコード内で、ビューアのロジックによって実行時にダウンロードされる可能性のある追加のJavaScriptファイルは、参照しないでください。 特に、ビューアによって読み込まれたHTML5 SDK `Utils.js`ライブラリを`/s7viewers`コンテキストパスから直接参照しないでください（いわゆる統合SDK `include`）。 理由は、`Utils.js`や類似のランタイムビューアライブラリの場所がビューアのロジックで完全に管理され、ビューアのリリース間で場所が変化するからです。 Adobeでは、古いバージョンのセカンダリビューア`includes`はサーバに保持されません。
>
>
>その結果、新しい製品バージョンがデプロイされる際に、ビューアが使用する任意のセカンダリJavaScript `include`への直接参照をページ上に置くと、ビューアの機能が将来的に機能しなくなります。

1. コンテナDIVを定義する。

   ビューア追加を表示するページの空のDIV要素。 DIV要素は、IDが定義されている必要があります。このIDを、後でビューアのAPIに渡します。

   プレースホルダDIVは位置固定要素です。つまり、`position` CSSプロパティは`relative`または`absolute`に設定されます。

   プレースホルダDIV要素の定義例を次に示します。

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアのサイズの設定

   ビューアの静的サイズを設定するには、最上位CSSクラスに対して絶対単位で`.s7ecatalogviewer`宣言するか、`stagesize`修飾子を使用します。

   サイズ調整は、CSS内で直接HTMLページまたはカスタムビューアのCSSファイルに配置できます。このCSSファイルは、後でScene7パブリッシングシステムでビューアプリセットレコードに割り当てるか、styleコマンドを使用して明示的に渡します。

   CSSでのビューアのスタイル設定について詳しくは、[eCatalogビューアのカスタマイズ](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)を参照してください。

   以下は、HTMLページで静的ビューアサイズを定義する例です。

   ```
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   `stagesize`修飾子は、Scene7Publishing Systemのビューアプリセットレコードに設定するか、`params`コレクションを使用してビューア初期化コードで明示的に渡すか、次のように、コマンドリファレンスの節で説明するAPI呼び出しとして渡すことができます。

   ```
   eCatalogViewer.setParam("stagesize", 
   "640,480");
   ```

1. ビューアを初期化する。

   上記の手順を完了したら、`s7viewers.eCatalogViewer`クラスのインスタンスを作成し、すべての設定情報をコンストラクターに渡して、ビューアインスタンスで`init()`メソッドを呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 最低でも、このオブジェクトには`containerId`フィールドがあり、ビューアのコンテナIDの名前と、ビューアでサポートされている設定パラメーターを含むネストされた`params` JSONオブジェクトが含まれています。 この場合、`params`オブジェクトには、`serverUrl`プロパティとして渡された画像サービングURLが最低限必要で、初期アセットは`asset`パラメーターとして含まれている必要があります。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、開始できます。

   ビューアのコンテナをDOMに追加して、ビューアのコードがIDでコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Webページが終わるまでDOMの構築が遅れます。 互換性を最大限に高めるには、`init()`メソッドを終了する`BODY`タグの直前、または本文`onload()`イベントで呼び出します。

   同時に、コンテナ要素がまだWebページレイアウトの一部である必要はありません。 例えば、`display:none`スタイルを割り当てて非表示にすることができます。 この場合、Webページからコンテナ要素がレイアウトに戻る瞬間まで、ビューアは初期化プロセスを遅延します。 この場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、`init()`メソッドを呼び出します。 この例では、`eCatalogViewer`をビューアインスタンスと仮定しています。`s7viewer`はプレースホルダー`DIV`の名前です。`http://s7d1.scene7.com/is/image/`は画像サービングのURL、`Viewers/Pluralist`はアセットです。

   ```
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、固定サイズのeCatalogビューアを埋め込んだ簡単なWebページの例です。

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高さ無制限のレスポンシブデザイン埋め込み**

レスポンシブデザイン埋め込みでは、Webページには通常、ビューアのコンテナ`DIV`の実行時のサイズを指示する柔軟なレイアウトが指定されています。 この例では、Webページでビューアのコンテナ`DIV`がWebブラウザーのウィンドウサイズの40%を占めることを許可し、高さは無制限のままにすると仮定します。 結果のWebページのHTMLコードは次のようになります。

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

このようなページへのビューアの追加方法は、固定サイズ埋め込みの場合と似ていますが、唯一の違いは、ビューアサイズを明示的に定義する必要がないことです。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVを定義する。
1. ビューアを作成し、初期化する。

上記の手順はすべて、固定サイズ埋め込みの場合と同じです。 既存追加の&quot;holder&quot; `DIV`に対するコンテナ`DIV`。 次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化する様子、ビューアの縦横比がアセットと一致する様子を確認できます。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実用的な使用例を説明しています。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**幅と高さが定義されたフレキシブルサイズ埋め込み**

幅と高さが定義されたフレキシブルサイズ埋め込みの場合、Webページのスタイルは異なります。 つまり、&quot;holder&quot; `DIV`に両方のサイズを提供し、ブラウザーウィンドウの中央に配置します。 また、Webページでは、`HTML`要素と`BODY`要素のサイズを100%に設定します。

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

残りの埋め込み手順は、高さ無制限のレスポンシブデザイン埋め込みと同じです。 結果の例を次に示します。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**セッターベースのAPIを使用した埋め込み**

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIでは、コンストラクターにパラメーターは不要です。設定パラメーターは、`setContainerId()`、`setParam()`および`setAsset()`の各APIメソッドを別々のJavaScript呼び出しで使用して指定します。

次の例は、セッターベースのAPIを使用する固定サイズ埋め込みを示しています。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
eCatalogViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
eCatalogViewer.setAsset("Viewers/Pluralist"); 
eCatalogViewer.init(); 
</script> 
</body> 
</html>
```

