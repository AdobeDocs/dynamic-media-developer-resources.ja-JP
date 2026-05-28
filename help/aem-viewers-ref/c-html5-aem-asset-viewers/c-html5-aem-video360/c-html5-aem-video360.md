---
title: ビデオ 360
description: HTML5 Video360 Viewerは、Dynamic Media ClassicまたはAdobe Experience Manager Dynamic Mediaから配信されたH.264形式のストリーミングおよびプログレッシブ 360動画を再生する360度ビデオプレーヤーです。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
TQID: 'https://experienceleague.adobe.com/exFQtdLDWST-H5pFv3m-q7eGCgtjrYe-TgxQal6VA48'
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
source-wordcount: 2620
ht-degree: 0%

---

# ビデオ 360{#video}

HTML5 Video360 Viewerは、Dynamic Media ClassicまたはAdobe Experience Manager Dynamic Mediaから配信されたH.264形式のストリーミングおよびプログレッシブ 360動画を再生する360度ビデオプレーヤーです。

360度ビデオは、没入型ビデオまたは球状ビデオとも呼ばれ、全方向のビューを同時に記録し、全方向カメラまたはカメラのコレクションを使用して撮影するビデオ記録です。 シングルビデオとアダプティブビデオセットの両方がサポートされています。 ビューアは、外部の場所でホストされているプログレッシブビデオストリームとHLS ストリームの操作もサポートしています。

360 ビデオの推奨アスペクト比は2:1です。 空間音はサポートされていません。 ビューアは360 ビデオのみで動作するように設計されています。360 ビデオ以外のビデオを再生しようとすると、ビデオ再生が歪みます。

ビューアは、HTML5 ビデオをサポートするデスクトップとモバイルの両方のWeb ブラウザーで動作するように設計されています。 ビューアは、オプションのソーシャル共有ツールをサポートしています。

Video360 Viewerは、基盤となるシステムがサポートしている場合は常に、HTML5 ストリーミングビデオ再生をHLS形式でデフォルト設定で使用します。 HTML5 ストリーミングをサポートしていないシステムでは、ビューアはHTML5 プログレッシブビデオ配信にフォールバックします。

ビューアータイプは517です。

## デモ URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)


## システム要件 {#section-b7270cc4290043399681dc504f043609}

[必要システム構成](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

## Video360 Viewerの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 Viewerは、メインのJavaScript ファイルと一連のヘルパーファイルを表します（1つのJavaScriptには、このビューアで使用されるすべてのHTML 5 Viewer SDK コンポーネント、assets、CSSが含まれています）。実行時にビューアがダウンロードします。

HTML5 Video360 Viewerは、IS-Viewersを備えた実稼動対応のHTML ページを使用してポップアップモードで使用するか、ドキュメント化されたAPIを使用してターゲット web ページに統合する組み込みモードで使用できます。

設定とスキニングは、このガイドで説明する他のビューアと同様です。 すべてのスキニングは、カスタム（CSS）カスケーディングスタイルシートを使用して実行されます。

すべてのビューアに共通する[&#x200B; コマンド参照 – 構成属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通するコマンド参照 – URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください

360 ビデオコンテンツでは、標準の非360 ビデオよりも高いエンコード設定が必要です。 つまり、360 コンテンツは、同じ知覚可能な品質を達成するために、360以外のビデオよりも高解像度である必要があります。 360 ビデオの次のアダプティブビデオプリセット設定を検討することをお勧めします。

* 720p、2500 kbps
* 1080p、5,000 kbps
* 1440p、6600 kbps

ただし、このような高画質の設定でエンコードされたビデオを配信するには、エンドユーザーのデバイスで高帯域幅の接続が必要です。

## Video360 Viewerの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360 Viewerは、再生/一時停止ボタン、ビデオスクラバーのビデオタイムバブル、再生時間/合計時間インジケーター、ボリュームコントロール、フルスクリーンボタンなど、ビデオ再生のための一連の標準ユーザーインターフェイスコントロールを提供します。 これらのコントロールはすべて、ビューアのユーザーインターフェイスの下部にあるコントロールバーにグループ化されます。

タッチデバイスでは、ボリューム制御はユーザーインターフェイスから非表示になります。これは、デバイスのハードウェアボタンを使用してのみボリュームを制御できるためです。

ビューアがポップアップモードで動作している場合、ユーザーインターフェイスで全画面ボタンを使用することはできません。

ビューアは、様々なソーシャルメディア共有ツールもサポートしています。 ユーザーインターフェイスの単一のボタンとして使用でき、ユーザーが共有ツールバーをクリックまたはタップすると、共有ツールバーに展開されます。 共有ツールバーには、Facebook、Twitter、メール共有、埋め込みコード共有、リンク共有など、サポートされている共有チャネルのタイプごとにアイコンが含まれています。 メール共有、埋め込み共有またはリンク共有ツールがアクティブ化されると、対応するデータ入力フォームを含むモーダルダイアログボックスがビューアに表示されます。 FacebookまたはTwitterが呼び出されると、ビューアはソーシャルメディアサービスから標準の共有ダイアログボックスにユーザーをリダイレクトします。 また、共有ツールが有効になっている場合、ビデオの再生は自動的に一時停止されます。 Web ブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは利用できません。

ビューアは、次の場合に360 ビデオ再生をサポートします。

* VR ヘッドセット（Oculus GoやOculus Riftなど）
* VR HMD （ヘッドマウントディスプレイ）マウント（Google段ボールなど）
* VR対応でないデバイス（VR HMD マウントに接続されていないデスクトップブラウザー、タブレット、携帯電話など）

VR ヘッドセットで360 ビデオコンテンツを表示するために、追加の設定は必要ありません。 ビューアはVR ヘッドセットの存在を自動的に検出し、ビデオコンテンツの上に「VR」ボタンを表示します。 この「VR」ボタンをアクティブにすると、ビデオのレンダリングがVR モードに切り替わります。 ビューアは、WebVRをサポートするブラウザーでのみVR レンダリングをサポートします。

VR HMD マウントを使用するには、ビューアの設定で`Video360Player.vrrender`修飾子を`1`に設定する必要があります。これにより、立体視レンダリングが強制されます。

VR ヘッドセットとVR HMD マウントでは、ヘッドセットの動きに応じて視点の変化が発生しますが、VR モードでは他の再生制御は提供されません。

VRが有効になっていないデバイスで360 ビデオを視聴する場合、エンドユーザーはマウス、タッチ、またはキーボードを使用してビデオの再生と視点を制御できます。

ビューアは、タッチスクリーンとマウスを備えたWindows デバイスでタッチ入力とマウス入力の両方をサポートしていますが、このサポートはChrome、Internet Explorer 11、Edge web ブラウザーのみに限定されています。

ビューアは完全にキーボードアクセス可能です。 [&#x200B; キーボードのアクセシビリティとナビゲーション &#x200B;](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## Video360 ビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

web ページごとに、閲覧者の行動に対するニーズは異なります。 Web ページでリンクが提供される場合があります。このリンクを選択すると、別のブラウザーウィンドウでビューアが開きます。 それ以外の場合は、ホスティングページに直接ビューアを埋め込む必要があります。 後者の場合、web ページは静的なページレイアウトを使用するか、異なるデバイスまたは異なるブラウザーウィンドウのサイズに対して異なる表示を行うレスポンシブデザインを使用します。 これらのニーズに対応するために、ビューアでは、ポップアップ、固定サイズの埋め込み、レスポンシブデザインの埋め込みという3つの主要な操作モードをサポートしています。

同じページに複数のビデオを埋め込むことは、タブレットおよびモバイルデバイスでサポートされています。 通常、一度に再生できるビデオは1つだけです。 ユーザーが1つのビデオの再生を開始してから別のビデオの再生を試みると、最初のビデオは自動的に一時停止します。 自動一時停止されたビデオは現在の再生時間を記憶するので、ユーザーはいつでもビデオに戻って再生を再開できます。 このルールの唯一の例外は、ビデオを並行して再生できるAndroid™ 4.x デバイスのChrome ブラウザーです。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別のweb ブラウザーウィンドウまたはタブで開きます。 ブラウザーのウィンドウ領域全体を使用し、ブラウザーのサイズ変更やデバイスの向きの変更に応じて調整します。

このモードは、モバイルデバイスで最も一般的です。 Web ページは、`window.open()` JavaScript呼び出し、`A` HTML要素の適切な設定、またはその他の適切なメソッドを使用してビューアを読み込みます。

ポップアップ操作モードには、標準のHTML ページを使用することをお勧めします。 [!DNL Video360Viewer.html]と呼ばれ、標準のIS-Viewers デプロイメントの[!DNL html5/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

カスタム CSSを適用すると、視覚的なカスタマイズを実現できます。

次に、新しいウィンドウでビューアを開くHTML コードの例を示します。

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```


**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアが既存のweb ページに追加されます。このweb ページには、ビューアに関連しない顧客コンテンツが既に含まれている可能性があります。 通常、閲覧者はweb ページの不動産の一部しか占めていません。

主なユースケースは、デスクトップ PCやタブレットデバイス向けのweb ページです。デバイスの種類に応じてレイアウトを自動的に調整する、レスポンシブデザインのページも使用できます。

初期読み込み後にビューアのサイズが変更されない場合は、固定サイズ埋め込みが使用されます。 この方法は、静的レイアウトを持つweb ページに最適です。

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

   ビューアを作成するには、HTML ヘッドにスクリプトタグを追加する必要があります。 ビューアーAPIを使用する前に、[!DNL Video360Viewer.js]を含めることを確認してください。 [!DNL Video360Viewer.js] ファイルは、標準のIS-Viewers デプロイメントの[!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

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
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. ビューアサイズの設定

   ビューアの静的サイズは、`.s7video360viewer` トップレベル CSS クラスを絶対単位で宣言するか、`stagesize`修飾子を使用することで設定できます。

   CSSでは、HTML ページに直接、またはカスタムビューア CSS ファイルにサイズを割り当てることができます。このファイルは、後でAdobe Experience Manager Assets オンデマンドのビューアプリセットレコードに割り当てられるか、`style` コマンドを使用して明示的に渡されます。

   CSSを使用したビューアのスタイル設定について詳しくは、[Video360 ビューアのカスタマイズ &#x200B;](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)を参照してください。

   次に、HTML ページで静的ビューアサイズを定義する例を示します。

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   AEM Assetsのビューアプリセットレコードで`stagesize`修飾子をオンデマンドで設定できます。 または、`params` コレクションを持つビューアの初期化コードを使用して明示的に渡すことも、コマンドリファレンスの節で説明されているようにAPI呼び出しとして渡すこともできます。例えば、次のようになります。

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   CSS ベースのアプローチを推奨し、この例で使用します。

1. ビューアの作成と初期化。

   上記の手順を完了したら、`s7viewers.Video360Viewer` クラスのインスタンスを作成し、すべての構成情報をそのコンストラクターに渡し、ビューアーインスタンスで`init()` メソッドを呼び出します。 構成情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアコンテナ IDの名前を保持する`containerId` フィールドと、ビューアでサポートされている設定パラメーターを含むネストされた`params` JSON オブジェクトが必要です。

   この場合、`params` オブジェクトには、少なくとも`serverUrl` プロパティとして渡された画像サービング URLと、`asset` パラメーターとして最初のアセットが必要です。 JSON ベースの初期化APIを使用すると、1行のコード、ビデオサーバーのURLが`videoserverurl` プロパティとして渡され、初期アセットが`asset` パラメーターとして渡され、インタラクティブデータが`interactivedata` プロパティとしてビューアを作成および開始できます。 JSON ベースの初期化APIを使用すると、1行のコードでビューアを作成および開始できます。

   ビューアコードがIDでコンテナ要素を見つけられるように、ビューアコンテナをDOMに追加することが重要です。 一部のブラウザーは、Web ページの最後までDOMの構築を遅らせます。 互換性を最大限に高めるには、終了`BODY` タグの直前または本文`onload()` イベントで`init()` メソッドを呼び出します。

   同時に、コンテナ要素は必ずしもweb ページレイアウトの一部であってはなりません。 例えば、割り当てられた`display:none` スタイルを使用して非表示にすることができます。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで初期化プロセスを遅らせます。 その場合、ビューアの読み込みは自動的に再開されます。


   次に、ビューアインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡して`init()` メソッドを呼び出す例を示します。 この例では、次の条件が適用されます。

   * ビューアーインスタンスは`video360Viewer`です。
   * プレースホルダー`DIV`の名前は`s7viewer`です。
   * 画像サービング URLは`https://s7d9.scene7.com/is/image`です。
   * ビデオサーバーのURLは`https://s7d9.scene7.com/is/content`です。
   * アセットは`Viewers/space_station_360-AVS`です。


   ```html {.line-numbers}
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


   次のコードは、Video360 ビューアを固定サイズで埋め込む面倒なweb ページの完全な例です。


   ```html {.line-numbers}
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

上記のすべての手順は、固定サイズの埋め込みと同じです。 コンテナ DIVを既存の`"holder"` DIVに追加します。

次のコードは、完全な例です。 ブラウザーのサイズを変更するとビューアのサイズが変わり、ビューアの縦横比がアセットとどのように一致するかを確認します。

```html {.line-numbers}
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


残りの埋め込み手順は、高さの制限のないレスポンシブ埋め込みに使用する手順と同じです。

結果として得られる例は次のとおりです。

```html {.line-numbers}
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

**Setter ベースのAPIを使用した埋め込み**

JSON ベースの初期化を使用する代わりに、セッターベースのAPIとno-args コンストラクターを使用できます。 このAPI コンストラクターを使用すると、パラメーターは受け取られず、設定パラメーターは`setContainerId()`、`setParam()`、`setAsset()`のAPI メソッドを使用して指定され、別々のJavaScript呼び出しが行われます。

次の例は、セッターベースのAPIで固定サイズの埋め込みを使用する方法を示しています。



```html {.line-numbers}
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


