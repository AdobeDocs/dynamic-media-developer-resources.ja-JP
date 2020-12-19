---
description: HTML5 Video360ビューアは、Scene7パブリッシングシステムまたはAEMDynamic Mediaから配信された、H.264形式でエンコードされたストリーミングおよびプログレッシブ360ビデオを再生する360度のビデオプレーヤーです。
seo-description: HTML5 Video360ビューアは、Scene7パブリッシングシステムまたはAEMDynamic Mediaから配信された、H.264形式でエンコードされたストリーミングおよびプログレッシブ360ビデオを再生する360度のビデオプレーヤーです。
seo-title: ビデオ360
solution: Experience Manager
title: ビデオ360
topic: Dynamic media
uuid: b03e6289-e012-4c62-835f-814463a27774
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '2613'
ht-degree: 0%

---


# ビデオ360{#video}

HTML5 Video360ビューアは、Scene7パブリッシングシステムまたはAEMDynamic Mediaから配信された、H.264形式でエンコードされたストリーミングおよびプログレッシブ360ビデオを再生する360度のビデオプレーヤーです。

360度ビデオ（イマーシブビデオまたは球状ビデオとも呼ばれる）は、あらゆる方向の表示を同時に記録し、全方位カメラまたはカメラの集まりを使用して撮影したビデオ録画です。 単一のビデオとアダプティブビデオセットの両方がサポートされています。 ビューアでは、外部の場所にホストされているプログレッシブビデオおよびHLSストリームの操作もサポートされています。

360ビデオの推奨される縦横比は2:1です。 空間サウンドはサポートされていません。 ビューアは、360ビデオのみで機能します。360以外のビデオを再生しようとすると、ビデオの歪んだ再生が行われます。

ビューアは、HTML5ビデオをサポートするデスクトップとモバイルのWebブラウザーの両方で動作するように設計されています。 Viewerでは、オプションのソーシャル共有ツールがサポートされます。

Video360ビューアは、基になるシステムがHLSをサポートしている場合は常に、初期設定でHLS形式のHTML5ストリーミングビデオ再生を使用します。 HTML5ストリーミングをサポートしていないシステムでは、ビューアはHTML5プログレッシブビデオ配信にフォールバックされます。

ビューアタイプ517

## デモURL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## システム要件 {#section-b7270cc4290043399681dc504f043609}

[必要システム構成](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

## ビデオ360ビューアの使用{#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360ビューアは、メインのJavaScriptファイルと、ビューアによって実行時にダウンロードされるヘルパーファイルのセット（この特定のビューア、アセット、CSSで使用されるすべてのHTML5ビューアSDKコンポーネントを含む1つのJavaScriptインクルード）です。

HTML5 Video360ビューアは、ISビューアに付属の運用に対応したHTMLページを使用するポップアップモードでも、ドキュメントに記述のあるAPIを使用してターゲットのWebページに統合される埋め込みモードでも、両方で使用できます。

設定とスキン表示は、このガイドで説明する他のビューアと同様です。 スキン表示はすべて、カスタム(CSS)カスケーディングスタイルシートを使用して適用されます。

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)と[すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください。

360ビデオコンテンツは、360以外の標準のビデオよりも高いエンコーディング設定が必要です。 つまり、同じ画質を実現するには、360コンテンツが360以外のビデオよりも高解像度になる必要があります。 360ビデオについては、次のアダプティブビデオプリセット設定を考慮することをお勧めします。

* 720p、2500 kbps
* 1080p、5000 kbps
* 1440p、6600 kbps

ただし、このような高品質の設定でエンコードされたビデオを配信するには、エンドユーザーのデバイスで高帯域幅の接続が必要になります。

## ビデオ360ビューアの操作{#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5ビデオ360ビューアには、再生/一時停止ボタン、ビデオスクラバービデオ時間の吹き出し、再生時間/合計時間インジケーター、ボリュームコントロール、フルスクリーンボタンなど、ビデオ再生用の一連の標準ユーザーインターフェイスコントロールが用意されています。 ビューアユーザインターフェイスの最下部にあるコントロールバーに、すべてのコントロールがグループ別に表示されます。

タッチデバイスでは、ボリュームコントロールはユーザーインターフェイスに表示されません。デバイスのハードウェアボタンを使用してのみボリュームを制御できるからです。

ビューアがポップアップモードで動作している場合は、ユーザインターフェイスのフルスクリーンボタンは使用できません。

Viewerは、様々なソーシャルメディア共有ツールもサポートしています。 これらのボタンは、ユーザーインターフェイスの1つのボタンとして使用でき、ユーザーがクリックまたはタップしたときに共有ツールバーに展開されます。 共有ツールバーには、Facebook、Twitter、電子メール共有、埋め込みコード共有、リンク共有など、サポートされる共有チャネルの種類別アイコンが表示されます。 電子メール共有、埋め込み共有またはリンク共有のツールをアクティブにすると、ビューアにモーダルダイアログボックスが開き、対応するデータ入力フォームが表示されます。 FacebookまたはTwitterを呼び出すと、ソーシャルメディアサービスの標準の共有ダイアログボックスにリダイレクトされます。 また、共有ツールがアクティブになると、ビデオ再生は自動的に一時停止します。 Webブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは使用できません。

ビューアは、VRヘッドセット（Oculus GoやOculus Riftなど）、VR HMD（ヘッドマウントディスプレイ）マウント（Googleのボール紙など）、VR非対応デバイス（VR HMDマウントに接続されていないデスクトップブラウザ、タブレット、携帯電話など）での360ビデオ再生をサポートします。

VRヘッドセットで360ビデオコンテンツを表示する場合、追加の設定は必要ありません。 ビューアは、VRヘッドセットの存在を自動的に検出し、ビデオコンテンツの上に「VR」ボタンを表示します。 この「VR」ボタンを有効にすると、ビデオレンダリングがVRモードに切り替わります。 ビューアは、WebVRがサポートされているブラウザでのみVRレンダリングをサポートします。

VR HMDマウントを使用するには、ビューアの設定で`Video360Player.vrrender`修飾子を`1`に設定する必要があります。これにより、立体レンダリングが強制されます。

VRヘッドセットおよびVR HMDでは、ヘッドセットの移動に応じて表示変更のマウントポイントが発生し、VRモードでは他の再生制御が提供されません。

VR非対応デバイスで360ビデオを視聴している場合、エンドユーザーはマウス、タッチ、またはキーボードを使用してビデオの再生と表示点を制御できます。

Viewerでは、タッチスクリーンとマウスの両方を搭載したWindowsデバイスでタッチ入力とマウス入力の両方がサポートされています。ただし、このサポート対象はChrome、Internet Explorer 11およびEdgeのWebブラウザーに限られます。

ビューアは完全にキーボードでアクセスできます。 [キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## ビデオ360ビューアの埋め込み{#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Webページごとに異なります。 Webページにリンクが表示される場合があります。リンクをクリックすると、別のブラウザーウィンドウでビューアが開きます。 ホストページ上に直接ビューアを埋め込む必要がある場合もあります。 後者の場合は、Webページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは主に次の3つの操作モードがサポートされています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

複数のビデオを同じページに埋め込む機能は、タブレットと携帯端末でサポートされています。 ほとんどの場合、一度に1つのビデオしか再生できません。 あるビデオの再生中に開始がを行い、次に別のビデオの再生を試みると、最初のビデオが自動的に一時停止します。 自動一時停止されたビデオは、現在の再生時間を記憶するので、ユーザーはいつでもビデオに戻って再生を再開できます。 唯一の例外は、Android 4.xデバイスのChromeブラウザーでビデオを並行して再生できる点です。

**ポップアップモードについて**

ポップアップモードでは、ビューアはWebブラウザーの別のウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやデバイスの向きが変更された場合は調整されます。

このモードは、モバイルデバイスで最も一般的です。 Webページでは、`window.open()` JavaScript呼び出し、適切に設定された`A` HTML要素またはその他の適切な方法を使用してビューアを読み込みます。

ポップアップ操作モードには、標準搭載されたHTMLページを使用することをお勧めします。 このページは[!DNL Video360Viewer.html]と呼ばれ、標準のIS-Viewersデプロイメントの[!DNL html5/]サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

カスタムCSSを適用すると、視覚的なカスタマイズを行うことができます。

次の例は、ビューアを新しいウィンドウに開くHTMLコードの例です。

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存のWebページに追加されます。このWebページには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 ビューアは通常、Webページの一部のスペースのみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、また、デバイスの種類に従ってレイアウトを自動調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 静的レイアウトのWebページには、これが最適です。

レスポンシブデザイン埋め込みは、コンテナ`DIV`のサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定しています。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナのサイズ変更の方法`DIV`によって、ビューアの動作が異なります。 Webページでコンテナ`DIV`の幅のみが設定され、高さは無制限のままの場合、ビューアでは、使用するアセットの縦横比に従って高さが自動的に選択されます。 この機能により、両側のパディングなしで、アセットは表示にぴったりと収まります。 この使用例は、Bootstrap、FoundationなどのレスポンシブWebデザインレイアウトフレームワークを使用するWebページで最も一般的です。

それ以外の場合は、Webページでビューアのコンテナ`DIV`の幅と高さの両方が設定されている場合、ビューアはその領域を占め、Webページのレイアウトに指定されているサイズに従います。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合があります。

**固定サイズ埋め込み**

ビューアは、次の操作を行ってWebページに追加します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナ`DIV`を定義しています。
1. ビューアのサイズを設定する。
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにスクリプトタグを追加する必要があります。 ビューアのAPIを使用するには、[!DNL Video360Viewer.js]を必ず含めます。 [!DNL Video360Viewer.js]ファイルは、次に示すように、IS-Viewersの標準のデプロイ先の[!DNL html5/js/]サブフォルダーにあります。

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

ビューアがAdobeのDynamic Mediaクラシックサーバの1つにデプロイされ、同じドメインから供給されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobeDynamic Mediaクラシックサーバの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScript `include`ファイルのみを参照してください。 Webページコード内で、ビューアのロジックによって実行時にダウンロードされる可能性のある追加のJavaScriptファイルは、参照しないでください。 特に、ビューアによって読み込まれたHTML5 SDK `Utils.js`ライブラリを`/s7viewers`コンテキストパスから直接参照しないでください（いわゆる統合SDK `include`）。 理由は、`Utils.js`や類似のランタイムビューアライブラリの場所がビューアのロジックで完全に管理され、ビューアのリリース間で場所が変化するからです。 Adobeでは、古いバージョンのセカンダリビューア`includes`はサーバに保持されません。
>
>
>その結果、新しい製品バージョンがデプロイされる際に、ビューアが使用する任意のセカンダリJavaScript `include`への直接参照をページ上に置くと、ビューアの機能が将来的に機能しなくなります。

1. コンテナ`DIV`を定義しています。

   ビューア追加を表示するページの空の`DIV`要素。 `DIV`要素は、IDが定義されている必要があります。このIDが後でビューアのAPIに渡されます。 DIVのサイズはCSSで指定します。

   プレースホルダー`DIV`は位置固定要素です。つまり、`position` CSSプロパティは`relative`または`absolute`に設定されます。

   Internet Explorerでフルスクリーン機能を正しく機能させるには、DOM内にプレースホルダー`DIV`よりも重ね順の高い要素がないことを確認してください。

   次に、定義済みのプレースホルダー`DIV`要素の例を示します。

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. ビューアのサイズの設定

   ビューアの静的サイズを設定するには、最上位CSSクラスに対して絶対単位で`.s7video360viewer`宣言するか、`stagesize`修飾子を使用します。

   サイズ調整は、CSS内で直接HTMLページまたはカスタムビューアのCSSファイルに配置できます。その後、カスタムビューアのCSSファイルが、AEM Assetsのオンデマンドでビューアプリセットレコードに割り当てられるか、`style`コマンドを使用して明示的に渡されます。

   CSSでのビューアのスタイル設定について詳しくは、[ビデオ360ビューアのカスタマイズ](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)を参照してください。

   以下は、HTMLページで静的ビューアサイズを定義する例です。

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   `stagesize`修飾子は、AEM Assetsのオンデマンドのビューアプリセットレコードに設定できます。 または、`params`コレクションを使用してビューア初期化コードを明示的に渡すか、次のように、コマンドリファレンスの節で説明するAPI呼び出しとして渡すこともできます。

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   CSSベースのアプローチを推奨し、この例では使用します。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、`s7viewers.Video360Viewer`クラスのインスタンスを作成し、すべての設定情報をコンストラクターに渡して、ビューアインスタンスで`init()`メソッドを呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 最低でも、このオブジェクトには`containerId`フィールドが存在し、ビューアのコンテナIDの名前と、ビューアでサポートされている設定パラメーターを含むネストされた`params` JSONオブジェクトが含まれている必要があります。

   この場合、`params`オブジェクトには、`serverUrl`プロパティとして渡された画像サービングURLが最低限必要で、初期アセットは`asset`パラメーターとして含まれている必要があります。 JSONベースの初期化APIを使用すると、1行のコード、`videoserverurl`プロパティとして渡されたビデオサーバーURL、`asset`パラメーターとしての初期アセット、`interactivedata`プロパティとしてのインタラクティブデータを使用してビューアを作成および開始できます。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、開始できます。

   ビューアのコンテナをDOMに追加して、ビューアのコードがIDでコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Webページが終わるまでDOMの構築が遅れます。 互換性を最大にするには、`init()`メソッドを終了`BODY`タグの直前、または本文`onload()`イベントで呼び出します。

   同時に、コンテナ要素がまだWebページレイアウトの一部である必要はありません。 例えば、`display:none`スタイルを割り当てて非表示にすることができます。 この場合、Webページからコンテナ要素がレイアウトに戻る瞬間まで、ビューアは初期化プロセスを遅延します。 この場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、`init()`メソッドを呼び出します。 この例では、次のことを前提としています。

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

   次のコードは、固定サイズのビデオ360ビューアを埋め込んだ簡単なWebページの例です。

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

幅と高さが定義されたレスポンシブ埋め込みの場合、Webページのスタイルは異なります。 `"holder"` DIVに両方のサイズを提供し、ブラウザーウィンドウの中央に配置します。 また、Webページでは、`HTML`要素と`BODY`要素のサイズを100%に設定します。

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

残りの埋め込み手順は、高さ無制限のレスポンシブ埋め込みで使用した手順と同じです。 結果の例を次に示します。

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

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合、コンストラクターにパラメーターは不要です。設定パラメーターは、`setContainerId()`、`setParam()`および`setAsset()`の各APIメソッドを別々のJavaScript呼び出しで使用して指定します。

以下の例は、固定サイズ埋め込みとセッターベースのAPIを使用する場合を説明しています。

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

