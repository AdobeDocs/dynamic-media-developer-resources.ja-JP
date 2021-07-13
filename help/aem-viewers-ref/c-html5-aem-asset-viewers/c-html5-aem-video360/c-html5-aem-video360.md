---
description: HTML5 Video360ビューアは、Dynamic Media ClassicまたはAEM Dynamic Mediaから配信され、H.264形式でエンコードされたストリーミングビデオとプログレッシブ360ビデオを再生する360度ビデオプレーヤーです。
solution: Experience Manager
title: ビデオ360
feature: Dynamic Media Classic，ビューア，SDK/API,360 VRビデオ
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '2590'
ht-degree: 0%

---

# ビデオ360{#video}

HTML5 Video360ビューアは、H.264形式でエンコードされたストリーミングビデオとプログレッシブ360ビデオを再生する360度ビデオプレーヤーで、Dynamic Media ClassicまたはAEM Dynamic Mediaから配信されます。

360度ビデオ（イマーシブビデオや球形ビデオとも呼ばれる）は、全方位カメラやカメラのコレクションを使用して撮影し、あらゆる方向のビューを同時に記録するビデオ録画です。 単一のビデオとアダプティブビデオセットの両方がサポートされています。 また、外部ロケーションでホストされるプログレッシブビデオおよびHLSストリームの操作もサポートされています。

360ビデオの推奨縦横比は2:1です。 空間音はサポートされていません。 このビューアは360ビデオでのみ機能するように設計されています。360以外のビデオを再生しようとすると、ビデオがゆがんで再生される。

このビューアは、HTML5ビデオをサポートするデスクトップとモバイルWebブラウザーの両方で動作するように設計されています。 ビューアは、オプションのソーシャル共有ツールをサポートしています。

Video360ビューアは、基になるシステムがHLSをサポートしている場合は常に、初期設定でHTML5ストリーミングビデオ再生をHLS形式で使用します。 HTML5ストリーミングをサポートしていないシステムでは、ビューアはHTML5プログレッシブビデオ配信にフォールバックされます。

ビューアタイプは517です。

## デモURL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## システム要件 {#section-b7270cc4290043399681dc504f043609}

[必要システム構成](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

## ビデオ360ビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5ビデオ360ビューアは、メインのJavaScriptファイルと、ヘルパーファイルのセット（この特定のビューア、アセット、CSSで使用されるすべてのHTML5ビューアSDKコンポーネントを含む単一のJavaScriptインクルード）を実行時にビューアによってダウンロードします。

HTML5ビデオ360ビューアは、ISビューアに付属する実稼動用HTMLページを使用するポップアップモードと、ドキュメント化されたAPIを使用してターゲットWebページに統合される埋め込みモードの両方で使用できます。

設定とスキン表示は、このガイドで説明する他のビューアと同様です。 スキンの適用はすべて、カスタム(CSS)カスケーディングスタイルシートを使用して行います。

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください。

360ビデオコンテンツは、標準の360以外のビデオよりも高いエンコーディング設定が必要です。 つまり、同じ知覚可能な画質を実現するには、360コンテンツが360ビデオ以外のビデオよりも高い解像度になる必要があります。 360ビデオに対しては、次のアダプティブビデオプリセット設定を考慮することをお勧めします。

* 720p、2500 kbps
* 1,080p、5,000 kbps
* 1440p、6600 kbps

ただし、このような高品質の設定でエンコードされたビデオを提供するには、エンドユーザーのデバイスで高帯域幅の接続が必要になります。

## ビデオ360ビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360ビューアは、再生/一時停止ボタン、ビデオスクラバビデオの時間の吹き出し、再生時間/合計時間のインジケーター、ボリューム制御、フルスクリーンボタンなど、ビデオ再生用の一連の標準的なユーザーインターフェイスコントロールを提供します。 ビューアのユーザインターフェイスの最下部にあるコントロールバーに、これらのコントロールがすべてグループ化されています。

タッチデバイスでは、デバイスのハードウェアボタンを使用してのみボリュームを制御できるので、ボリュームコントロールはユーザーインターフェイスに表示されません。

ビューアがポップアップモードで動作している場合、ユーザーインターフェイスでフルスクリーンボタンは使用できません。

このビューアは、様々なソーシャルメディア共有ツールもサポートしています。 これらは、ユーザーインターフェイスの単一のボタンとして使用でき、ユーザーがクリックまたはタップすると共有ツールバーに展開されます。 共有ツールバーには、Facebook、Twitter、電子メール共有、埋め込みコード共有、リンク共有など、サポートされる共有チャネルの各タイプ用のアイコンが表示されます。 電子メール共有、埋め込み共有またはリンク共有のツールをアクティブにすると、ビューアにモーダルダイアログボックスが表示され、対応するデータ入力フォームが表示されます。 facebookまたはTwitterを呼び出すと、ソーシャルメディアサービスの標準の共有ダイアログボックスにリダイレクトされます。 また、共有ツールが有効になると、ビデオ再生が自動的に一時停止します。 Webブラウザーのセキュリティ上の制約により、共有ツールはフルスクリーンモードでは使用できません。

ビューアは、VRヘッドセット（Oculus GoやOculus Riftなど）での360ビデオ再生、VR HMD（ヘッドマウントディスプレイ）マウント（Google Dalbooldなど）、VR非対応デバイス（VR HMDマウントに接続されていないデスクトップブラウザ、タブレット、携帯電話など）での再生をサポートします。

VRヘッドセットで360ビデオコンテンツを表示する場合、追加の設定は不要です。 ビューアは、VRヘッドセットの存在を自動的に検出し、ビデオコンテンツの上に「VR」ボタンを表示します。 この「VR」ボタンをオンにすると、ビデオのレンダリングがVRモードに切り替わります。 ビューアは、WebVRがサポートされているブラウザーでのみVRレンダリングをサポートします。

VR HMDをマウントするには、ビューアの設定で`Video360Player.vrrender`修飾子を`1`に設定し、立体視レンダリングを強制する必要があります。

VRヘッドセットとVR HMDマウントの視点の変更は、ヘッドセットの移動に応じて発生し、VRモードでは他の再生制御が提供されません。

VR非対応デバイスで360ビデオを視聴する場合、エンドユーザーはマウス、タッチ、キーボードを使用してビデオの再生と視点を制御できます。

ビューアは、タッチスクリーンとマウスを備えたWindowsデバイスでタッチ入力とマウス入力の両方をサポートしますが、このサポートは、Chrome、Internet Explorer 11およびEdge Webブラウザーに限られます。

ビューアは完全にキーボードでアクセス可能です。 [キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## Video360ビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Webページごとに異なります。 Webページにリンクが表示され、このリンクをクリックすると別のブラウザーウィンドウでビューアが開くことがあります。 ホスティングページに直接ビューアを埋め込む必要がある場合もあります。 後者の場合は、Webページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは次の3つの主要な操作モードがサポートされています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

同じページへの複数のビデオの埋め込みは、タブレットとモバイルデバイスでサポートされています。 ほとんどの場合、一度に1つのビデオのみ再生できます。 ユーザーが1つのビデオの再生を開始し、別のビデオの再生を試みると、最初のビデオが自動的に一時停止します。 自動一時停止になったビデオは現在の再生時間を記憶するので、ユーザーはいつでもビデオに戻って再生を再開できます。 このルールの唯一の例外は、Android 4.xデバイスのChromeブラウザーで、ビデオを並行して再生できます。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別のWebブラウザーウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやデバイスの向きが変更された場合は調整されます。

このモードは、モバイルデバイスで最も一般的なモードです。 Webページでは、`window.open()` JavaScript呼び出し、適切に設定された`A` HTML要素またはその他の適切な方法を使用してビューアを読み込みます。

ポップアップ操作モードには、標準提供のHTMLページを使用することをお勧めします。 このページは[!DNL Video360Viewer.html]と呼ばれ、標準のIS-Viewersデプロイメントの[!DNL html5/]サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

カスタムCSSを適用することで、視覚的なカスタマイズを実現できます。

以下は、ビューアを新しいウィンドウで開くHTMLコードの例です。

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存のWebページに追加されます。既に、ビューアに関連していない顧客コンテンツが含まれている場合があります。 ビューアは、通常、Webページの一部の領域のみを占有します。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、また、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 これは、静的レイアウトのWebページに最適です。

レスポンシブデザイン埋め込みは、コンテナ`DIV`のサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定しています。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナ`DIV`のサイズ変更の方法によって、ビューアの動作が異なります。 Webページでコンテナ`DIV`の幅のみが設定され、高さは無制限のままの場合、ビューアでは、使用するアセットの縦横比に従って高さが自動的に選択されます。 この機能により、側面のパディングなしで、アセットが表示にぴったりと収まります。 この使用例は、Bootstrap、FoundationなどのレスポンシブWebデザインレイアウトフレームワークを使用するWebページで最も一般的です。

それ以外の場合は、Webページでビューアのコンテナ`DIV`の幅と高さの両方が設定されている場合、ビューアはその領域を占め、Webページのレイアウトで指定されているサイズに従います。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合があります。

**固定サイズ埋め込み**

ビューアをWebページに追加するには、次の手順を実行します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナ`DIV`を定義します。
1. ビューアのサイズを設定する。
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにscriptタグを追加する必要があります。 ビューアのAPIを使用するには、必ず[!DNL Video360Viewer.js]を含めてください。 [!DNL Video360Viewer.js]ファイルは、次に示すように、IS-Viewersの標準のデプロイ先の[!DNL html5/js/]サブフォルダーにあります。

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

ビューアがDynamic Media ClassicAdobeのいずれかにデプロイされ、同じドメインから提供されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobeDynamic Media Classicサーバーの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>ページ上では、メインビューアのJavaScript `include`ファイルのみを参照する必要があります。 実行時にビューアのロジックによってダウンロードされる可能性のあるWebページコード内の追加のJavaScriptファイルは、参照しないでください。 特に、ビューアによって`/s7viewers`コンテキストパスから読み込まれたHTML5 SDK `Utils.js`ライブラリを直接参照しないでください（いわゆる統合SDK `include`）。 理由は、`Utils.js`や類似のランタイムビューアライブラリの場所は、ビューアのロジックによって完全に管理され、ビューアのリリースによって位置が変わるからです。 Adobeでは、セカンダリビューア`includes`の古いバージョンはサーバに保持されません。
>
>
>その結果、新しい製品バージョンがデプロイされると、ビューアが使用するセカンダリJavaScript `include`への直接参照をページに配置すると、将来ビューア機能が壊れます。

1. コンテナ`DIV`を定義します。

   ビューアを表示するページに空の`DIV`要素を追加します。 `DIV`要素のIDは、後でビューアのAPIに渡されるので、定義する必要があります。 DIVのサイズはCSSで指定します。

   プレースホルダー`DIV`は配置を指定する要素です。つまり、CSSの`position`プロパティを`relative`または`absolute`に設定します。

   Internet Explorerでフルスクリーン機能を正しく機能させるには、DOM内に、プレースホルダー`DIV`よりも重ね順の高い要素が存在しないことを確認します。

   次に、定義済みのプレースホルダー`DIV`要素の例を示します。

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. ビューアサイズの設定

   ビューアの静的サイズを設定するには、`.s7video360viewer`最上位CSSクラスに対して絶対単位で宣言するか、`stagesize`修飾子を使用します。

   サイズ調整は、HTMLページ上またはカスタムビューアのCSSファイルで直接設定できます。その後、CSSファイルをAEM Assetsのオンデマンドでビューアプリセットレコードに割り当てるか、`style`コマンドを使用して明示的に渡します。

   CSSでのビューアのスタイル設定について詳しくは、 [ビデオ360ビューアのカスタマイズ](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)を参照してください。

   以下は、HTMLページで静的ビューアサイズを定義する例です。

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   AEM Assets — オンデマンドで、ビューアプリセットレコードに`stagesize`修飾子を設定できます。 または、次のように、 `params`コレクションを使用してビューア初期化コードを明示的に渡すことも、コマンドリファレンスの節で説明するようにAPI呼び出しとして渡すこともできます。

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   CSSベースのアプローチを推奨し、この例で使用します。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、`s7viewers.Video360Viewer`クラスのインスタンスを作成し、すべての設定情報をコンストラクターに渡して、ビューアインスタンスで`init()`メソッドを呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 最低でも、このオブジェクトには`containerId`フィールドが必要です。このフィールドには、ビューアのコンテナIDの名前と、ビューアでサポートされている設定パラメーターを含むネストされた`params` JSONオブジェクトが含まれています。

   この場合、`params`オブジェクトには、`serverUrl`プロパティとして渡された画像サービングURLが少なくとも含まれ、最初のアセットが`asset`パラメーターとして含まれている必要があります。 JSONベースの初期化APIを使用すると、1行のコード、`videoserverurl`プロパティとして渡されたビデオサーバのURL、`asset`パラメーターとしての初期アセット、`interactivedata`プロパティとしてのインタラクティブデータを使用して、ビューアを作成して開始できます。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、起動できます。

   ビューアのコードがIDでコンテナ要素を見つけられるように、ビューアのコンテナをDOMに追加することが重要です。 一部のブラウザーは、Webページの終わりまでDOMの構築を遅らせます。 互換性を最大にするには、 `BODY`終了タグの直前、または本文の`onload()`イベントで`init()`メソッドを呼び出します。

   同時に、コンテナ要素は、必ずしもまだWebページレイアウトの一部ではない必要があります。 例えば、`display:none`スタイルを割り当てて非表示にすることができます。 この場合、Webページでコンテナ要素がレイアウトに戻るまで、ビューアの初期化プロセスが遅れます。 その場合、ビューアの読み込みが自動的に再開されます。

   以下の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して`init()`メソッドを呼び出します。 この例では、次の点を前提としています。

   * ビューアインスタンスは`video360Viewer`です。
   * プレースホルダー`DIV`の名前は`s7viewer`です。
   * 画像サービングのURLは`https://s7d9.scene7.com/is/image`です。
   * ビデオサーバーのURLは`https://s7d9.scene7.com/is/content`です。
   * アセットは`Viewers/space_station_360-AVS`です。

   ```
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、固定サイズのVideo360ビューアを埋め込んだ簡単なWebページの例です。

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高さ無制限のレスポンシブデザイン埋め込み**

レスポンシブデザイン埋め込みでは、Webページには通常、ビューアのコンテナ`DIV`の実行時のサイズを指示する柔軟なレイアウトが指定されています。 次の例では、Webページでビューアのコンテナ`DIV`がWebブラウザーのウィンドウサイズの40%を占めることを許可し、高さは無制限のままにするとします。 WebページのHTMLコードは次のようになります。

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

このようなページにビューアを追加する手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、ビューアのサイズを明示的に定義する必要がない点です。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナDIVを定義する。
1. ビューアを作成し、初期化する。

上記の手順は、固定サイズ埋め込みの場合と同じです。 コンテナDIVを既存の`"holder"` DIVに追加します。 次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化することと、ビューアの縦横比がアセットと一致することに注意してください。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**幅と高さが定義されたレスポンシブ埋め込み**

幅と高さが定義されたレスポンシブ埋め込みの場合、Webページのスタイル設定は異なります。 `"holder"` DIVに両方のサイズを提供し、ブラウザーウィンドウの中央に配置します。 また、Webページでは、`HTML`要素と`BODY`要素のサイズを100%に設定します。

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

残りの埋め込み手順は、高さ無制限のレスポンシブ埋め込みで使用する手順と同じです。 結果の例は次のようになります。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**セッターベースのAPIを使用した埋め込み**

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合は、コンストラクターにパラメーターは不要です。設定パラメーターは、 `setContainerId()`、 `setParam()`および`setAsset()`の各APIメソッドを別々のJavaScript呼び出しで使用して指定します。

次の例は、固定サイズ埋め込みをセッターベースのAPIと共に使用する方法を示しています。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```
