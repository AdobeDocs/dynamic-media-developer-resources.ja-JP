---
description: HTML5 Video360ビューアは、Scene7 Publishing SystemまたはAEMダイナミックメディアから配信される、H.264形式でエンコードされたストリーミングビデオおよびプログレッシブ360ビデオを再生する360度のビデオプレーヤーです。
seo-description: HTML5 Video360ビューアは、Scene7 Publishing SystemまたはAEMダイナミックメディアから配信される、H.264形式でエンコードされたストリーミングビデオおよびプログレッシブ360ビデオを再生する360度のビデオプレーヤーです。
seo-title: Video360
solution: Experience Manager
title: Video360
topic: Dynamic media
uuid: b03e6289-e012-4c62-835f-814463a27774
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360{#video}

HTML5 Video360ビューアは、Scene7 Publishing SystemまたはAEMダイナミックメディアから配信される、H.264形式でエンコードされたストリーミングビデオおよびプログレッシブ360ビデオを再生する360度のビデオプレーヤーです。

360度のビデオは、イマーシブビデオまたは球形ビデオとも呼ばれ、あらゆる方向のビューが同時に記録されるビデオ録画で、全方向のカメラまたはカメラのコレクションを使用して撮影されます。 単一のビデオとアダプティブビデオセットの両方がサポートされています。 ビューアは、外部の場所でホストされているプログレッシブビデオおよびHLSストリームの操作もサポートします。

360ビデオの推奨される縦横比は2:1です。 空間サウンドはサポートされていません。 ビューアは、360ビデオのみで機能するように設計されています。360以外のビデオを再生しようとすると、ビデオの再生がゆがみます。

ビューアは、HTML5ビデオをサポートするデスクトップとモバイルの両方のWebブラウザーで機能するように設計されています。 Viewerでは、オプションのソーシャル共有ツールがサポートされています。

Video360ビューアは、基になるシステムがHLSをサポートしている場合は常に、HTML5ストリーミングビデオをHLS形式で初期設定で使用します。 HTML5ストリーミングをサポートしていないシステムでは、ビューアはHTML5プログレッシブビデオ配信にフォールバックします。

ビューアのタイプは517です。

## デモURL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## システム要件 {#section-b7270cc4290043399681dc504f043609}

必要システム [構成を参照してくださ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)い。

## ビデオ360ビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360ビューアは、メインのJavaScriptファイルとヘルパーファイルのセット（この特定のビューア、アセット、CSSで使用されるすべてのHTML5ビューアSDKコンポーネントを含む1つのJavaScriptが含まれる）を、ビューアが実行時にダウンロードします。

HTML5 Video360ビューアは、ISビューアに付属の実稼働用HTMLページを使用するポップアップモードでも、ドキュメントに記載されたAPIを使用してターゲットWebページに統合される埋め込みモードでも、両方で使用できます。

設定とスキン表示は、このガイドで説明する他のビューアと同様です。 スキン表示はすべて、カスタム(CSS)カスケーディングスタイルシートを使用して適用されます。

すべてのビ [ューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 、およびすべ [てのビューアに共通のコマンドリファレンス — URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

360ビデオコンテンツは、360以外の標準のビデオよりも高いエンコーディング設定が必要です。 つまり、360コンテンツは、同じ画質を得るために、360以外のビデオよりも高い解像度になる必要があります。 360ビデオについては、次のアダプティブビデオプリセット設定を考慮することをお勧めします。

* 720p、2500 kbps
* 1080p、5000 kbps
* 1440p、6600 kbps

ただし、このような高品質の設定でエンコードされたビデオを配信するには、エンドユーザーのデバイス上で高帯域幅の接続が必要になります。

## ビデオ360ビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5ビデオ360ビューアは、再生/一時停止ボタン、ビデオスクラバビデオの時間の吹き出し、再生時間/合計時間インジケーター、ボリュームコントロール、フルスクリーンボタンなど、ビデオ再生用の一連の標準ユーザーインターフェイスコントロールを提供します。 これらのコントロールはすべて、ビューアのユーザインターフェイスの最下部にあるコントロールバーにグループ化されています。

タッチデバイスでは、ボリュームコントロールはユーザーインターフェイスに表示されません。デバイスのハードウェアボタンを使用してのみボリュームを制御できるからです。

ビューアがポップアップモードで動作している場合、ユーザインターフェイスのフルスクリーンボタンは使用できません。

Viewerは、様々なソーシャルメディア共有ツールもサポートしています。 ユーザーインターフェイスの1つのボタンとして使用でき、ユーザーがクリックまたはタップすると共有ツールバーに展開されます。 共有ツールバーには、Facebook、Twitter、電子メール共有、埋め込みコード共有、リンク共有など、サポートされる共有チャネルの種類別のアイコンが含まれています。 電子メール共有、埋め込み共有またはリンク共有のツールをアクティブにすると、ビューアにモーダルダイアログボックスが表示され、対応するデータ入力フォームが表示されます。 FacebookまたはTwitterを呼び出すと、ソーシャルメディアサービスの標準の共有ダイアログボックスにリダイレクトされます。 また、共有ツールがアクティブになると、ビデオ再生が自動的に一時停止されます。 Webブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは使用できません。

ビューアは、VRヘッドセット（Oculus GoやOculus Riftなど）での360個のビデオ再生、VR HMD（ヘッドマウントディスプレイ）のマウント（Googleダンボールなど）およびVR非対応のデバイス（VR HMDマウントに接続されていないデスクトップブラウザ、タブレット、携帯電話など）をサポートします。

VRヘッドセットで360個のビデオコンテンツを表示する場合、追加の設定は必要ありません。 ビューアは、VRヘッドセットの存在を自動的に検出し、ビデオコンテンツの上に「VR」ボタンを表示します。 この「VR」ボタンをアクティブにすると、ビデオレンダリングがVRモードに切り替わります。 ビューアは、WebVRがサポートされているブラウザでのみVRレンダリングをサポートします。

VR HMDマウントを使用するには、モディファイヤをビ `Video360Player.vrrender` ューアの設定でに設定し、ステレオスコ `1` ピックレンダリングを強制する必要があります。

VRヘッドセットおよびVR HMDマウントの視点変更は、ヘッドセットの移動に応じて発生し、VRモードで他の再生制御が提供されるわけではありません。

VR非対応デバイスで360ビデオを視聴する場合、エンドユーザーはマウス、タッチ、またはキーボードを使用して、ビデオの再生と視点を制御できます。

Viewerは、タッチスクリーンとマウスを搭載したWindowsデバイスでタッチ入力とマウス入力の両方をサポートしていますが、Chrome、Internet Explorer 11およびEdge Webブラウザーのみに対応しています。

ビューアは完全にキーボードでアクセスできます。 詳しくは、キーボ [ードのアクセシビリティとナビゲーションを参照してくださ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)い。

## ビデオ360ビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

Webページが異なると、ビューアの動作に対するニーズが異なります。 Webページをクリックすると、別のブラウザーウィンドウでビューアが開くリンクが表示される場合があります。 ホストページに直接ビューアを埋め込む必要がある場合もあります。 後者の場合は、Webページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するため、ビューアでは、次の3つの主要な操作モードがサポートされています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

複数のビデオを同じページに埋め込む機能は、タブレットおよびモバイルデバイスでサポートされています。 ほとんどの場合、一度に1つのビデオしか再生できません。 あるビデオの再生を開始し、次に別のビデオの再生を試みると、最初のビデオは自動的に一時停止します。 自動一時停止されたビデオは、現在の再生時間を記憶するので、ユーザーはいつでもビデオに戻って再生を再開できます。 唯一の例外は、Android 4.xデバイスのChromeブラウザーでビデオを並行して再生できる点です。

**ポップアップモードについて**

ポップアップモードでは、ビューアはWebブラウザーの別のウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやデバイスの向きが変更された場合は調整されます。

このモードは、モバイルデバイスで最も一般的なモードです。 Webページでは、JavaScript呼び出し、適切に設定された `window.open()` HTML要素、またはその他の適切な方法を使用し `A` てビューアを読み込みます。

ポップアップ操作モードには、標準搭載されたHTMLページを使用することをお勧めします。 これはとい [!DNL Video360Viewer.html] う名前で、標準のISビューアのデ [!DNL html5/] プロイ先のサブフォルダーにあります。

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

カスタムCSSを適用すると、視覚的なカスタマイズを行うことができます。

次の例は、ビューアを新しいウィンドウで開くHTMLコードの例です。

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存のWebページに追加されます。このWebページには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 ビューアは通常、Webページの一部のスペースのみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けのWebページ、また、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用されます。 これは、静的レイアウトのWebページに最適な選択肢です。

レスポンシブデザイン埋め込みは、コンテナのサイズ変更に対応して実行時にビューアのサイズを変更する可能性がある場合を想定していま `DIV`す。 最も一般的な使用例は、柔軟なページレイアウトを使用するWebページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Webページによるコンテナのサイズ変更の方法に応じて、ビューアの動作が異なりま `DIV`す。 Webページでコンテナの幅のみが設定され、高さは無制限のままの場合、 `DIV`ビューアは、使用されるアセットの縦横比に従って高さを自動的に選択します。 この機能により、両側のパディングなしで、アセットが表示範囲にぴったりと収まるようになります。 この使用例は、Bootstrap、FoundationなどのレスポンシブWebデザインレイアウトフレームワークを使用するWebページで最も一般的です。

それ以外の場合は、Webページでビューアのコンテナの幅と高さの両方が設定されている場合、ビューアはその領域のみを占め、Webページのレイアウトで指定されているサイズに従います。 `DIV`良い例は、ビューアをモーダルオーバーレイに埋め込み、オーバーレイがWebブラウザーのウィンドウサイズに従ってサイズ設定される場合です。

**固定サイズ埋め込み**

ビューアをWebページに追加するには、次の手順を実行します。

1. ビューアのJavaScriptファイルをWebページに追加する。
1. コンテナの定義を参照してくだ `DIV`さい。
1. ビューアのサイズの設定
1. ビューアを作成し、初期化する。

1. ビューアのJavaScriptファイルをWebページに追加する。

   ビューアを作成するには、HTMLのheadにスクリプトタグを追加する必要があります。 ビューアのAPIを使用する前に、を必ず含めてくださ [!DNL Video360Viewer.js]い。 このフ [!DNL Video360Viewer.js] ァイルは、次に示すように、 [!DNL html5/js/] 標準のISビューアのデプロイ先のサブフォルダーにあります。

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

ビューアがAdobe Dynamic Media Classicサーバーの1つにデプロイされ、同じドメインから供給されている場合は、相対パスを使用できます。 それ以外の場合は、ISビューアがインストールされているAdobe Dynamic Media Classicサーバーの1つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScriptファイルのみ `include` を参照する必要があります。 Webページコード内の追加のJavaScriptファイルを参照してはなりません。Webページコードは、ビューアのロジックによって実行時にダウンロードされる可能性があります。 特に、ビューアによって読み込まれたHTML5 SDKライブラリを、コ `Utils.js` ンテキストパス(いわゆる統合SDK `/s7viewers` ) `include`から直接参照しないでください。 この理由は、実行時のViewerライブラリの場 `Utils.js` 所がビューアのロジックで完全に管理され、ビューアのリリース間で位置が変わるからです。 アドビでは、古いバージョンのセカンダリViewerをサーバーに保 `includes` 持していません。
>
>
>その結果、新しい製品バージョンがデプロイされると、ビューアで使用さ `include` れるセカンダリJavaScriptへの直接参照をページに配置すると、将来、ビューアの機能が機能しなくなります。

1. コンテナの定義を参照してくだ `DIV`さい。

   ビューアを表 `DIV` 示するページに空の要素を追加します。 このID `DIV` は後でビューアのAPIに渡されるので、要素のIDが定義されている必要があります。 DIVのサイズはCSSで指定されます。

   プレースホル `DIV` ダーは、位置固定要素です。つまり、 `position` CSSプロパティがまたはに設定さ `relative` れていま `absolute`す。

   Internet Explorerでフルスクリーン機能を正しく機能させるには、DOM内に、プレースホルダーよりも重ね順の高い要素がないことを確認しま `DIV`す。

   次に、定義済みのプレースホルダー要素の例を示 `DIV` します。

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. ビューアのサイズの設定

   ビューアの静的サイズを設定するには、最上位CSSクラスに対して絶 `.s7video360viewer` 対単位で宣言するか、修飾子を使用し `stagesize` ます。

   サイズ調整は、CSS内でHTMLページ上に直接、またはカスタムビューアのCSSファイル内に直接配置し、後でAEM Assetsのビューアプリセットレコード（オンデマンド）に割り当てるか、コマンドを使用して明示的に渡すことがで `style` きます。

   CSSを使用し [たビューアのスタイル設定について詳しくは](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 、「ビデオ360ビューアのカスタマイズ」を参照してください。

   HTMLページで静的ビューアサイズを定義する例を次に示します。

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   修飾子は、AEM Assetsのビ `stagesize` ューアプリセットレコード（オンデマンド）で設定できます。 または、次のように、ビューアの初期化コードと共にコレクションを使用して、またはコ `params` マンドリファレンスの節で説明するAPI呼び出しとして、明示的に渡すことができます。

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   CSSベースのアプローチを推奨し、この例で使用します。

1. ビューアを作成し、初期化する。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報をコ `s7viewers.Video360Viewer` ンストラクターに渡し、ビューアインスタンスでメソッド `init()` を呼び出します。 設定情報は、JSONオブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアの `containerId` コンテナIDの名前と、ビューアでサポートされている設定パラメータを含むネストされた `params` JSONオブジェクトを保持するフィールドが必要です。

   この場合、オブジェクトに `params` は、プロパティとして渡された画像サービングURLが少なくとも含まれて `serverUrl` おり、最初のアセットがパラメーターとして含まれている必要が `asset` あります。 JSONベースの初期化APIを使用すると、1行のコード、プロパティとして渡されたビデオサーバのURL、パラメーターとしての初期アセット、プロパティとしてのインタラクティブデータを使用して、ビ `videoserverurl` ューアを作成し、起動することが `asset``interactivedata` できます。 JSONベースの初期化APIを使用すると、1行のコードでビューアを作成し、起動できます。

   ビューアのコンテナをDOMに追加し、ビューアのコードがIDでコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Webページの最後までDOMの構築が遅れます。 互換性を最大にするには、終了 `init()` タグの直前、またはbodyイベ `BODY` ントでメソッドを呼び出す必要があ `onload()` ります。

   同時に、コンテナ要素は、まだWebページレイアウトの一部ではない必要があります。 例えば、割り当てられたスタイルを使用して非表 `display:none` 示にすることができます。 この場合、Webページがコンテナ要素をレイアウトに戻す瞬間まで、ビューアは初期化処理を遅延します。 その場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、必要最小限の設定オプションをコンストラクターに渡して、メソッドを呼び出 `init()` します。 この例では、次の点を想定しています。

   * ビューアインスタンスはで `video360Viewer`す。
   * プレースホルダの名前は `DIV` です `s7viewer`。
   * 画像サービングのURLはで `https://s7d9.scene7.com/is/image`す。
   * ビデオサーバーのURLはで `https://s7d9.scene7.com/is/content`す。
   * アセットはで `Viewers/space_station_360-AVS`す。

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

幅と高さが定義されたレスポンシブ埋め込みの場合、Webページのスタイルは異なります。 DIVに両方のサイズを提供し `"holder"` 、ブラウザーウィンドウの中央に配置します。 また、Webページでは、要素と要素のサイズを100% `HTML` に設 `BODY` 定しています。

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

残りの埋め込み手順は、高さ無制限のレスポンシブ埋め込みで使用された手順と同じです。 結果の例を次に示します。

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

JSONベースの初期化を使用する代わりに、セッターベースのAPIとno-argsコンストラクターを使用できます。 このAPIを使用する場合、コンストラクターはパラメーターを受け取りません。設定パラメーターは、、、および `setContainerId()`APIメソッド `setParam()`を使用して、個別のJavaScript呼び出し `setAsset()` で指定されます。

次の例は、固定サイズ埋め込みとセッターベースのAPIの使用を示しています。

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

